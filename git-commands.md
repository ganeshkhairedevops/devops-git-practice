# Git Commands Reference

## 🔹 Setup & Config

### git --version
Shows installed Git version.  
Example:
git --version

### git config --global user.name
Sets your global username  
Example:
git config --global user.name "ganeshkhairedevops"

### git config --global user.email
Sets your global email  
Example:
git config --global user.email "ganeshkhaire14@gmail.com"

---

## 🔹 Basic Workflow

### git init
Initializes a new Git repository  
Example:
git init

### git add
Stages files for commit  
Example:
git add git-commands.md

### git commit
Creates a snapshot of staged changes  
Example:
git commit -m "Add initial git commands reference"

---

## 🔹 Viewing Changes

### git status
Shows working directory status  
Example:
git status

### git log
Shows commit history  
Example:
git log

### git log --oneline
Shows compact commit history  
Example:
git log --oneline

### git diff
Shows changes between commits  
Example:
git diff

---
## 🔹 Push Local Repository to GitHub

This guide explains how to push an existing local Git repository to GitHub.
### Step 1: Create a Repository on GitHub
Go to https://github.com

Click New Repository

Enter repository name

Do NOT initialize with README

Click Create Repository

### Step 2: Add Remote Repository
Copy your repository URL from GitHub and run:
```bash
git remote add origin https://github.com/ganeshkhairedevops/devops-git-practice.git
```
Verify remote:
```bash
git remote -v
```
### Step 3: Push to GitHub
If using main branch:
```bash
git branch -M main
git push -u origin main
```
If using master branch:
```bash
git push -u origin master
```
### Authentication (Important)

Personal Access Token (HTTPS)
- Username: Your GitHub username
- Password: Use your Personal Access Token

Create token:

GitHub → Settings → Developer Settings → Personal Access Tokens

copy token and add in url and change your git repo 
```bash
git remote set-url origin https://ghp_Xxxxxxxxxxxxxxxxxxx17298@github.com/ganeshkhairedevops/devops-git-practice.git
```

Push again:
```bash
git push -u origin master
```
---

## 🔹 Branching

### git branch
Lists all branches  
Example:
git branch

### git branch <name>
Creates a new branch  
Example:
git branch feature-1

### git switch <branch>
Switches branches  
Example:
git switch main
git checkout branchname

### git switch -c <name>
Creates and switches to a branch  
Example:
git switch -c feature-2

### git branch -d <branch>
Deletes a branch  
Example:
git branch -d feature-2

---
## Advanced Git
Create branch from main
git switch main
git switch -c feature-login

---

## 🔹 Remote Repository

### git remote -v
Shows connected remotes  
Example:
git remote -v

### git remote add origin <url>
Adds remote repository  
Example:
git remote add origin https://github.com/ganeshkhairedevops/devops-git-practice.git

### git push -u origin <branch>
Pushes branch and sets upstream  
Example:
git push -u origin main

### git fetch
Downloads changes without merging  
Example:
git fetch origin

### git pull
Fetch + merge  
Example:
git pull origin main

---
## 🔀 Merge

### git merge
Merges another branch into current branch  
Example:
git merge feature-login

### git merge --squash
Squashes all commits into one before merging  
Example:
git merge --squash feature-profile
git commit -m "Add profile feature (squashed)"

---
## 🔄 Rebase

### git rebase
Reapplies commits on top of another branch  
Example:
git rebase main

### git rebase --continue
Continues rebase after resolving conflicts  
Example:
git rebase --continue

### git rebase --abort
Cancels rebase and restores state  
Example:
git rebase --abort

### git rebase --skip
Skips problematic commit during rebase  
Example:
git rebase --skip

---
## 🧨 Conflict Handling

During a conflict, Git shows:

<<<<<<< HEAD
Your current branch changes
=======
Incoming branch changes
>>>>>>> branch-name

Resolve manually, then:

git add <file>

git commit

---
## 👜 Stash

### git stash
Temporarily saves uncommitted changes  
Example:
git stash

### git stash push -m
Stash with message  
Example:
git stash push -m "WIP dashboard UI"

### git stash list
Lists stashes  
Example:
git stash list

### git stash pop
Applies and removes latest stash  
Example:
git stash pop

### git stash apply
Applies stash but keeps it saved  
Example:
git stash apply stash@{0}

---
## 🍒 Cherry Pick

### git cherry-pick
Applies specific commit to current branch  
Example:
git cherry-pick 1a2b3c4

---

## 🔹 Undoing Changes

### git reset --soft
Moves HEAD but keeps changes staged  
Example:
git reset --soft HEAD~1

### git reset --mixed
Moves HEAD and unstages changes  
Example:
git reset --mixed HEAD~1

### git reset --hard
Moves HEAD and deletes changes  
Example:
git reset --hard HEAD~1

### git revert
Creates a new commit that undoes a previous commit  
Example:
git revert <commit-hash>

### git reflog
Shows all HEAD movements (recovery tool)  
Example:
git reflog

🔥 This document is continuously updated as part of DevOps 90-Day Learning.
