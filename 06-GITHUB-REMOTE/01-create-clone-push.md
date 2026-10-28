# 10 — Create a GitHub Repository and Push

## Create a remote repository

1. Sign in at https://github.com/.
2. Select **New repository**.
3. Choose a repository name and visibility.
4. For the simplest first push of an existing local project, create an empty repository without a README, license or `.gitignore`.
5. Copy the HTTPS or SSH URL.

Public repositories can be viewed by anyone. Do not publish confidential files or secrets.

## Push an existing local repository

From your project folder:

```bash
git status
git add .
git commit -m "Add initial project files"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git remote -v
git push -u origin main
```

Replace the placeholders with your details. If there is nothing new to commit, don't create an unnecessary commit.

If `origin` already exists, inspect it with `git remote -v`. Use `git remote set-url origin URL` only when you intend to change that destination.

## Clone an existing repository

```bash
git clone https://github.com/OWNER/REPOSITORY.git
cd REPOSITORY
```

Cloning downloads the repository and its history.

## Authentication

Use GitHub's supported browser sign-in, credential manager, or SSH setup. Do not put account passwords or access tokens in scripts, command examples, or repository files.

Official help: https://docs.github.com/en/authentication
