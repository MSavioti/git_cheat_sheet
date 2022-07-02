# Cheat Sheet for git

## Creating or downloading a repository

**Initialize repository**

 - `git init`

**Download a remote repository**

 - `git clone [remote_repository_link]`

**Link to a remote repository**

 - `git remote add origin [remote_repository_link]`

## Checking changes in the working directory

 - `git status`

## Adding files to staging area

**Add a single file**

 - `git add [file_relative_path]`

**Add all new and modified files**

 - `git add -A`
(Or, if you at the root of your project folder)
 - `git add .`

**Add all modified files, but not new ones**

 - `git add -u`

## Deleting files

**Deletes a file on working directory**

 - `git rm [file_relative_path]`

**Deletes a file added to staging area**

 - `git rm -f [file_relative_path]`

## Committing

**Commit a file**

 - `git commit -m [file_relative_path]`

**Add all modified files to staging area and commit them (doesn't work with newly created files)**

 - `git commit -am [file_relative_path]`

**Check commit history**

 - `git log`

**Check commit history with a simplified view**

 - `git log --oneline`

**Check commit history while improving readability**

 - `git log --decorate`

**Check commit history while using ASCII elements to represent the tree**

 - `git log --graph`

**Check commit history involving a desired file**

 - `git log -- [file_relative_path]`

## Undoing actions

**Go back to a specific commit**

 - `git checkout [commit_id]`

**Discard changes in working directory (not added to staging area)**

 - `git checkout [file_or_directory]`

(Discard all changes)
 - `git checkout .`

**Removes a file from staging area**

 - `git reset HEAD [file_relative_path]`

OR

 - `git rm --cached [file_relative_path]`

**Revert the changes added in a specific commit and created a new commit**

 - `git revert[git_id]`

**Changing the message of the most recent commit**

 - `git commit --amend -m "message"`

(if original commit was pushed)
 - `git push --force origin [branchName]`

**Remove all commits after provided commit**

 - `git reset --hard [commit_id]`

**Rename a branch**

 - `git branch -m [branch_name] [new_branch_name]`

## Managing branches

**List branches ans shows current branch**

 - `git branch`

**Create a new branch**

 - `git branch [branch_name]`

**Switch to a branch**

 - `git checkout [branch_name]`

**Create a new branch and switch to it**

 - `git checkout -b [branch_name]`

**Delete a local branch**

 - `git branch -d [branch_name]`

**Delete a remote branch**

 - `git branch -D branch_name`
 - `git push origin :branch_name`

**Merge a branch into the current branch**

 - `git merge [branch_name]`

**Merge a branch into another branch**

 - `git merge [source_branch_name] [other_branch_name]`

## Interacting with a remote repository

**Save changes to a specific branch**

 - `git push origin [branch_name]`

**Save changes to a branch and track it**

 - `git push -u origin [branch name]`

**Save changes to the tracked branch**

 - `git push`

**Download changes in remote repository**

 - `git fetch [branch_name]`

**Download changes in remote repository and merge them into the local repository**

 - `git pull [branch_name]`

**Download changes from the tracked branch**

 - `git pull`

**Use rebase instead of merge while issuing pull command**

 - `git pull --rebase origin [branch_name]`

## Moving or renaming files with git

**Renaming**

 - `git mv [file_current_name] [file_new_name]`

**Moving**

 - `git mv [file_name] [directory]`

## Rebase

**Rebase flow**

On feature branch:
 - `git rebase main`

On main branch
 - `git rebase [feature_branch_name]`

**Rebase conflicts**

Continue rebase after conflicts are sorted out:
 - `git rebase --continue`

Cancel rebase operation:
 - `git rebase --abort`

**Rebase onto changes in remote repository**

 - `git pull --rebase origin [branch_name]`

## Stash

**Save (stash) work in progress**

 - `git stash`

**For stash action to include untracked files**

 - `git stash -u`

**Applying stashed work**

 - `git stash apply`

**Deleting last stash created**

 - `git stash drop`

**Apply stash while also dropping it**

 - `git stash pop`
 
## Cherry pick

**Takes commit from a branch and apply it into another branch**
 - `git cherry-pick [commit_id]`

## Tags

**Lightweight tag (name only)**

 - `git tag [tag_name]`

**Annotated tag (contains message)**

 - `git tag -a [tag_name]`

**Comparing tags**

 - `git diff [tag_name_1] [tag_name_2]`

**Tagging a specific commit**

 - `git tag [tag_name_1] [commit_id]`

**Transfer tag to another commit**

 - `git tag [tag_name] -f [commit_id]`

**Push tags to remote repository**

 - `git push [remote] [branch] tag [tag_name]`

## Make git ignore files and directories

Create a file named ".gitignore" on the root of your project

**Ignore using patterns**

 - `*.example`

**Ignore file**

 - `[file_relative_path]`

**Ignore directory**

 - `[directory_to_ignore]/`

## Setting up a alias for a command

 - `git config --global alias.[command_name] "[actual_command]"`

E.g.: `git config --global alias.history "log --oneline --decorate --graph"`
Usage: `git history`
