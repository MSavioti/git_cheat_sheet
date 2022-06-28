# Cheat Sheet for git

## Initialize repository

```git init```

## Checking changes in the working directory

```git status```

## Adding files to staging area

### Add a single file

```git add {file_relative_path}```

### Add all modified files

```git add .```

## Removing files

### Removes a file from staging area

```git rm --cached {file_relative_path}```

### Removes (deletes) a file on working directory

```git rm {file_relative_path}```

### Removes (deletes) a file added to staging area

```git rm -f {file_relative_path}```

## Committing changes

### Commit a file

```git commit -m {file_relative_path}```

### Add all modified files to staging area and commit them (doesn't work with newly created files)

```git commit -am {file_relative_path}```

### Check commit history

```git log```
