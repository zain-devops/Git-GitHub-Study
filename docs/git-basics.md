# Lesson 1: Git Fundamentals

## 1. What is Git?

Git is a distributed version control system. It records changes to files so you can review history, compare versions, create branches, and collaborate without keeping separate copies of every version manually.

### Git vs GitHub

- **Git** is the version-control tool that runs on your computer.
- **GitHub** is a hosting and collaboration platform for Git repositories.
- You can use Git without GitHub, and Git repositories can be hosted on other services.

## 2. Core concepts

- **Working directory:** the files you are currently editing.
- **Staging area (index):** the changes selected for the next commit.
- **Commit:** a recorded snapshot with a message and identifier.
- **Repository (repo):** the project and its tracked history.
- **Branch:** a movable line of development, often used for a feature or fix.
- **Remote:** a named link to another repository, commonly called `origin`.
- **Clone:** create a local copy of a remote repository and its history.
- **Merge:** combine changes from one branch into another.
- **Pull request (PR):** a GitHub collaboration proposal to review and merge changes.

## 3. Install and configure Git

Install Git using the official instructions at https://git-scm.com/downloads, then verify:

```bash
git --version
```

Configure your commit identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
git config --list
```

The name and email are recorded in commits. Use an email appropriate for your GitHub account or a GitHub-provided private email if you prefer.

## 4. Create a repository and commit files

```bash
mkdir demo-project
cd demo-project
git init
echo "# Demo Project" > README.md
git status
git add README.md
git status
git commit -m "Add project README"
```

Typical workflow:

1. Edit files in the working directory.
2. Inspect changes with `git status` and `git diff`.
3. Stage selected changes with `git add`.
4. Record the staged snapshot with `git commit`.

Useful commands:

```bash
git status                 # Current branch and changed files
git add file.txt           # Stage one file
git add .                  # Stage changes under the current directory
git diff                   # Unstaged changes
git diff --staged          # Staged changes
git commit -m "Describe change"
git log --oneline           # Compact history
git show                    # Inspect the latest commit
```

Review carefully before using `git add .`; it may stage files you did not intend to commit.

## 5. `.gitignore`

A `.gitignore` file tells Git which untracked files or paths to ignore. Example:

```gitignore
# Environment and secrets
.env
.env.*
!.env.example
*.pem
*.key

# Dependencies and generated files
node_modules/
dist/
build/
__pycache__/
*.pyc

# Editor and OS files
.DS_Store
Thumbs.db
.vscode/
```

Ignore rules do not automatically stop tracking a file already committed. If a secret was committed, revoke/rotate it immediately; removing it in a later commit does not erase it from history.

## 6. Branching and merging

Use a branch to develop a change separately from the main line:

```bash
git switch -c feature/add-introduction
# Edit a file
git add .
git commit -m "Add introduction"
git switch main
git merge feature/add-introduction
git branch
```

Older Git versions may use `git checkout -b` to create and switch branches. Prefer `git switch` for clarity when available.

Delete a merged local branch when no longer needed:

```bash
git branch -d feature/add-introduction
```

## 7. Undoing changes carefully

Choose a command based on where the change is:

```bash
git restore file.txt          # Discard unstaged edits to this file
git restore --staged file.txt # Unstage a file; keep working-tree edits
git revert COMMIT_ID           # Create a new commit that reverses a commit
```

**Caution:** `git restore file.txt` discards uncommitted edits to that file. Avoid `git reset --hard` unless you fully understand that it can permanently discard local work.

For a local commit that has not been shared, `git commit --amend` can update the latest commit. Avoid rewriting commits already shared with others unless the team agrees.

## 8. Inspecting history

```bash
git log
git log --oneline --graph --decorate --all
git show COMMIT_ID
git diff main..feature/add-introduction
```

A commit ID identifies a particular recorded snapshot. `git diff` compares changes; `git log` shows commit history.

## 9. Common errors

- **“not a git repository”:** move into the project folder or run `git init` if this folder should become a repository.
- **Nothing to commit:** check `git status`; perhaps no tracked changes are staged.
- **Wrong author identity:** correct `git config` for future commits; old commits require rewriting to change their metadata.
- **A file is ignored:** inspect `.gitignore` and run `git check-ignore -v path/to/file`.
- **Authentication failed:** use GitHub's supported browser, credential manager, or SSH authentication flow. Account passwords are not accepted for Git HTTPS operations.
