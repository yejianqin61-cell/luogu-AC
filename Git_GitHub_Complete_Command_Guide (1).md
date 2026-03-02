# Git & GitHub Complete Command Guide

## Table of Contents

1.  Basic Concepts
2.  Repository Initialization
3.  Daily Workflow Commands
4.  Branch Management
5.  Merging & Conflict Resolution
6.  Remote Repository Operations
7.  Undo & Recovery
8.  Stash Operations
9.  Tags
10. Rebase & Advanced History Editing
11. Cherry-pick
12. Submodules
13. Configuration
14. Team Collaboration Workflows
15. Troubleshooting Scenarios
16. Dangerous Commands Warning
17. Essential Mastery Checklist

------------------------------------------------------------------------

## 1. Basic Concepts

-   Working Directory
-   Staging Area (Index)
-   Local Repository
-   Remote Repository

------------------------------------------------------------------------

## 2. Repository Initialization

### Initialize new repo

``` bash
git init
```

### Clone repository

``` bash
git clone <repo_url>
git clone -b branch_name <repo_url>
```

------------------------------------------------------------------------

## 3. Daily Workflow

``` bash
git status
git add file.txt
git add .
git commit -m "message"
git push
git pull
```

Amend last commit:

``` bash
git commit --amend
```

------------------------------------------------------------------------

## 4. Branch Management

``` bash
git branch
git branch -a
git branch dev
git checkout dev
git checkout -b dev
git switch -c dev
git branch -d dev
git branch -D dev
```

------------------------------------------------------------------------

## 5. Merge & Conflict

``` bash
git merge branch_name
git merge --no-ff branch_name
```

After resolving conflicts:

``` bash
git add .
git commit
```

------------------------------------------------------------------------

## 6. Remote Operations

``` bash
git remote -v
git remote add origin <repo_url>
git push origin main
git push -f
git fetch
git pull
```

------------------------------------------------------------------------

## 7. Undo & Recovery

Restore file:

``` bash
git restore file.txt
git checkout -- file.txt
```

Unstage:

``` bash
git reset file.txt
```

Reset commits:

``` bash
git reset --soft HEAD^
git reset --mixed HEAD^
git reset --hard HEAD^
git reset --hard commit_id
```

Safe revert:

``` bash
git revert commit_id
```

------------------------------------------------------------------------

## 8. Stash

``` bash
git stash
git stash list
git stash pop
git stash apply
git stash drop
```

------------------------------------------------------------------------

## 9. Tags

``` bash
git tag
git tag v1.0
git tag -a v1.0 -m "version 1.0"
git push origin v1.0
git push origin --tags
```

------------------------------------------------------------------------

## 10. Rebase

``` bash
git rebase main
git rebase -i HEAD~3
git rebase --abort
```

------------------------------------------------------------------------

## 11. Cherry-pick

``` bash
git cherry-pick commit_id
```

------------------------------------------------------------------------

## 12. Submodules

``` bash
git submodule add <repo_url>
git submodule update --init --recursive
```

------------------------------------------------------------------------

## 13. Configuration

``` bash
git config --list
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

------------------------------------------------------------------------

## 14. Team Workflow

### Feature Branch Flow

``` bash
git pull
git checkout -b feature_x
git commit -m "feature work"
git push origin feature_x
```

### Hotfix Flow

``` bash
git checkout main
git checkout -b hotfix
# fix bug
git commit -m "hotfix"
git merge main
```

------------------------------------------------------------------------

## 15. Troubleshooting

  Problem                Solution
  ---------------------- -------------------------
  push rejected          git pull first
  wrong commit message   git commit --amend
  want old version       git reset or git revert
  messy history          git rebase -i

------------------------------------------------------------------------

## 16. Dangerous Commands

  Command                Risk
  ---------------------- --------------------------
  git reset --hard       data loss
  git push -f            overwrite remote history
  rebase public branch   collaboration issues

------------------------------------------------------------------------

## 17. Essential Mastery

Must know deeply:

-   add / commit / push / pull
-   branch / merge
-   conflict resolution
-   reset / revert
-   rebase
-   stash

Understand that Git is fundamentally a history graph system.
