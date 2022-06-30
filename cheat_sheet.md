# Cheat Sheet for git

## Initialize repository

`git init`

## Link a remote repository

``

## Checking changes in the working directory

`git status`

## Adding files to staging area

### Add a single file

`git add [file_relative_path]`

### Add all modified files

`git add .`

## Removing files

### Removes (deletes) a file on working directory

`git rm [file_relative_path]`

### Removes (deletes) a file added to staging area

`git rm -f [file_relative_path]`

## Committing changes

### Commit a file

`git commit -m [file_relative_path]`

### Add all modified files to staging area and commit them (doesn't work with newly created files)

`git commit -am [file_relative_path]`

### Check commit history

`git log`

### Check commit history with a simplified view

`git log --oneline`

## Undoing actions

### Go back to a specific commit

`git checkout [commit_id]`

### Removes a file from staging area

`git rm --cached [file_relative_path]`

### Revert the changes added in a specific commit and created a new commit

`git revert[git_id]`

### Changing the message of the most recent commit

`git commit --amend -m "message"`

(if original commit was pushed)
`git push --force origin [branchName]`

### Remove all commits after provided commit

`git reset --hard [commit_id]`

## Managing branches

### List branches ans shows current branch

`git branch`

### Create a new branch

`git branch [branch_name]`

### Switch to a branch

`git checkout [branch_name]`

### Create a new branch and switch to it

`git checkout -b [branch_name]`

### Delete a local branch

`git branch -d [branch_name]`

### Delete a remote branch

`git branch -D branch_name`
`git push origin :branch_name`

### Merge a branch into the current branch

`git merge [branch_name]`

### Merge a branch into another branch

`git merge [source_branch_name] [other_branch_name]`

## Interacting with a remote repository

### Save changes to a specific branch

`git push origin [branch_name]`

### Save changes to a branch and track it

`git push -u origin [branch name]`

### Save changes to the tracked branch

`git push`

### Download changes in remote repository

`git fetch [branch_name]`

### Download changes in remote repository and merge them into the local repository

`git pull [branch_name]`

### Download changes from the tracked branch

`git pull`

## Make git ignore files and directories

Create a file named ".gitignore" on the root of your project

### Ignore extensions

`*.file_extension`

### Ignore file

`file/path.file_extension`

### Ignore directory

`directory/`

### Ignore subdirectory

`/subdirectory/`

### Ignore files and directories with a specific pattern

`*pattern*`
