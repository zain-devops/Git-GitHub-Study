# ⚡ Git Cheat Sheet

## Setup and start

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git init
git clone URL
```

## Inspect

```bash
git status
git diff
git diff --staged
git log --oneline --graph --decorate --all
git show HEAD
```

## Stage and commit

```bash
git add FILE
git add .
git restore --staged FILE
git commit -m "Describe the change"
git commit --amend
```

## Branches

```bash
git branch
git switch -c feature/name
git switch main
git merge feature/name
git branch -d feature/name
```

## Remote workflow

```bash
git remote -v
git remote add origin URL
git fetch origin
git pull
git push -u origin main
```

## Recovery / intermediate

```bash
git restore FILE
git revert COMMIT_ID
git stash push -m "WIP"
git stash list
git stash pop
git reflog
```

⚠️ `git restore FILE` can discard uncommitted edits. `git reset --hard` can discard local work. Understand the effects before using destructive commands.
