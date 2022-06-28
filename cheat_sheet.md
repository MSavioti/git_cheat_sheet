# Cheat Sheet for git

## Initialize repository

`git init`

## Checking changes in the working directory

`git status`

## Adding files to staging area

### Add a single file

`git add [file_relative_path]`

### Add all modified files

`git add .`

## Removing files

### Removes a file from staging area

`git rm --cached [file_relative_path]`

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

## Undoing actions

### Go back to a specific commit

`git checkout [commit_id]`

### Revert to a specific commit and created a new commit

``

## Managing branches

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
