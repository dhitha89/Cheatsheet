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

**Commit your changes**
git commit -m "new file added"

**Stage and Commit**
git commit -a -m "updated env"

**NOTE:**
touch new.txt
git commit -a -m "added new text file" --> wont work since new.txt file is still not tracked

**SO FOLLOW TWO STEPS:**
git add .
git commit -m"new txt file added"

**Publish your changes from local to remote repository**
git push origin main 
git push

**Sync after fork**
git pull upstream main or(git fetch upstream --> git merge upstream/main)
git push origin main
______________________________________________________________________________________________________________

# Viewing Changes

**See commit history**
git log
git diff file.txt

**Delete branch on remote**
git push origin --delete <branch-name>

**Delete branch locally**
git branch -D <branch-name>

**Removes filename from every commit,Recreates each commit again,Generates NEW commit hashes**
git filter-repo --path <filename> --invert-paths
Ex: Before filter-repo
A1 → add app.js + .env
B1 → update app.js
C1 → add README

After filter-repo
A2 → add app.js
B2 → update app.js
C2 → add README

**Unstage files**
git restore --staged file.txt

**Remove from staging and Git tracking, keep file locally.**
git rm --cached file.txt

**Unstage everything and make all files untracked.**
git rm --cached -r .

**Undo edits and restore last committed version**
git restore file.txt 
OR
git checkout file.txt

**Undo last commit, but keep files staged**
git reset --soft HEAD~1

**Undo last commit, and unstage files**
git reset --mixed HEAD~1

**Delete commit and delete changes**
git reset --hard HEAD~1

**Delete file from folder and Git (tracked removal)**
git rm 

**Replay your commits on top of another branch ex feature branch**
git switch feature
git rebase main

**Takes all commits on your feature branch and combines them into a single commit on main**
git merge --squash feature

**Grab a single specific commit from anywhere and places it onto your current branch**
git cherry-pick commit-id