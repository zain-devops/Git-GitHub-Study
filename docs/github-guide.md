# Lesson 2: GitHub Workflow

## 1. What is GitHub?

GitHub hosts Git repositories and adds collaboration features such as issues, pull requests, code review, project discussions, releases, and automation with GitHub Actions.

## 2. Create a repository on GitHub

1. Sign in at https://github.com/.
2. Select **New repository**.
3. Enter a repository name and description.
4. Choose **Public** or **Private**.
5. For the simplest first push from an existing local project, create it empty (do not add a README, license, or `.gitignore` on the website).
6. Copy the repository's HTTPS or SSH URL.

Public repositories can be viewed by anyone. Never publish secrets or confidential files, even in a repository you later intend to make private.

## 3. Push an existing local repository

From the root of your project:

```bash
git status
git add .
git commit -m "Add project files"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/REPOSITORY-NAME.git
git remote -v
git push -u origin main
```

If `origin` already exists, inspect it with `git remote -v`; update it with `git remote set-url origin URL` only if that is the intended destination.

## 4. Clone an existing repository

```bash
git clone https://github.com/OWNER/REPOSITORY.git
cd REPOSITORY
```

Cloning downloads the repository and its history and configures a remote, usually named `origin`.

## 5. Fetch, pull, and push

```bash
git fetch origin
git pull
git push
```

- `fetch` downloads remote updates without merging them into your current branch.
- `pull` fetches and integrates remote updates into the current branch (the exact integration behavior depends on configuration).
- `push` sends local commits to a remote branch.

Before starting work, check your branch and synchronize with the team's agreed workflow.

## 6. Use a feature branch and pull request

```bash
git switch -c feature/update-docs
# Make changes
git add .
git commit -m "Improve documentation"
git push -u origin feature/update-docs
```

Then on GitHub:

1. Open the repository.
2. Choose **Compare & pull request** (or open a new pull request).
3. Explain what changed and why.
4. Review the diff and checks.
5. Request review if working with a team.
6. Merge when approved and checks pass.
7. Delete the remote feature branch if it is no longer needed.

A pull request is a GitHub collaboration feature; it is not a Git command.

## 7. Resolve a merge conflict

A conflict occurs when Git cannot automatically combine overlapping edits.

1. Run `git status` to find conflicted files.
2. Open each file and look for markers like these:

```text
<<<<<<< HEAD
Your current-branch version
=======
Incoming-branch version
>>>>>>> feature-branch
```

3. Edit the file so it contains the intended final content, and remove the markers.
4. Test the result.
5. Stage the resolved file and commit:

```bash
git add path/to/conflicted-file
git commit
```

Do not blindly choose one side. Read both versions and decide what the final content should be.

## 8. Issues, releases, and README

- **Issues:** track bugs, tasks, questions, and enhancements.
- **Pull requests:** discuss and review proposed changes.
- **Releases:** publish a named version and release notes.
- **README.md:** explain what the project is, how to use it, and how to contribute.
- **LICENSE:** state the terms under which others may use the work.

## 9. Good repository practices

- Write descriptive commit messages, such as `Add Git branching examples`.
- Keep commits focused and reasonably small.
- Use branches for work in progress.
- Review pull-request diffs before merging.
- Add a README, `.gitignore`, and suitable license.
- Protect important branches when working as a team.
- Never commit credentials, private keys, tokens, or real `.env` files.
- Use GitHub's documentation for current authentication and security guidance.

## 10. Official learning resources

- GitHub Docs: https://docs.github.com/
- GitHub Skills: https://skills.github.com/
- Connecting to GitHub with SSH: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
- About pull requests: https://docs.github.com/en/pull-requests
