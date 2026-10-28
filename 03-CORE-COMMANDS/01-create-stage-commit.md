# 04 — Create, Stage and Commit

## Create a repository

```bash
mkdir hello-git
cd hello-git
git init
```

`git init` creates a repository in the current folder. If your shell doesn't support `mkdir` in that form, create the folder with your file manager and open a terminal inside it.

## Add a file and commit it

```bash
echo "# Hello Git" > README.md
git status
git add README.md
git status
git commit -m "Add initial README"
git log --oneline
```

## Understand the workflow

1. **Edit:** change files in the working tree.
2. **Inspect:** use `git status` and `git diff`.
3. **Stage:** use `git add` for the changes you want in the next commit.
4. **Commit:** save a checkpoint using `git commit`.

## Important commands

```bash
git status
git add README.md
git add .
git diff
git diff --staged
git commit -m "Add project introduction"
git log --oneline
git show
```

`git add .` stages changes under the current directory. Always review what is staged before committing.

## Good commit messages

Good:
- `Add installation instructions`
- `Fix typo in setup guide`
- `Document branch workflow`

Avoid vague messages such as `stuff`, `update`, or `final`.

## Exercise

Create `about.md`, stage it, commit it, edit it again, compare unstaged and staged differences, and create another commit.
