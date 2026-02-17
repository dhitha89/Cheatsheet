# Git Commands

## Setup and Config Commands

**Intialize a new project with git**
git init

**Copy a remote repository to local**
git clone https://repolink.git

**Create a new branch and switch to it**
git checkout -b newbranch
git switch -c new-branch

**Switch to an existing branch**
git checkout newbranch
git switch branch-name


**Pull a new branch created on Github repo to local**
git fetch

**Set email for this project only**
git config user.email

**Set email for all projects**
git config --global user.email
Note: Local config overrides global
____________________________________________________________________________________________________________

## Basic Workflow

**Stage files**
git add file.txt

**Unstage files**
git rm --cached file.txt
or
git restore --staged file.txt

**Remove all files from staging (before initial commit)**
git rm --cached -r .

**Commit your changes**
git commit -m "new file added"

**Publish your changes from local to remote repository**
git push origin main 
git push

______________________________________________________________________________________________________________

# Viewing Changes

**See commit history**
git log
git diff file.txt


