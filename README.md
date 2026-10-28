# Git & GitHub Study Material

A beginner-friendly, hands-on guide to learning Git and GitHub. Follow the lessons in order, run the commands in your own practice folder, and complete the exercises at the end.

## Learning outcomes

By the end, you should be able to:
- Explain the difference between Git and GitHub.
- Configure Git and create a local repository.
- Track, commit, inspect, and undo changes safely.
- Work with branches and merge changes.
- Connect a local project to GitHub and push/pull changes.
- Collaborate using issues and pull requests.
- Resolve a basic merge conflict and follow good repository practices.

## Suggested study plan

| Session | Topic | Practice |
|---|---|---|
| 1 | Git concepts and setup | Install Git; set your name and email |
| 2 | Repository, staging, commits | Create a repository and make 3 commits |
| 3 | History and undo | Inspect logs; unstage and restore a practice file |
| 4 | Branching and merging | Create a feature branch and merge it |
| 5 | GitHub and remotes | Create a GitHub repository and push your project |
| 6 | Collaboration | Open an issue and pull request; review changes |
| 7 | Conflicts and best practices | Resolve a practice merge conflict |
| 8 | Revision | Complete `docs/exercises.md` |

## Lessons

1. [Git fundamentals and commands](docs/git-basics.md)
2. [GitHub workflow](docs/github-guide.md)
3. [Exercises and revision questions](docs/exercises.md)

## Quick start

Check that Git is installed:

```bash
git --version
```

Set the author identity used in your commits (use your own details):

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
```

Create a practice repository:

```bash
mkdir git-practice
cd git-practice
git init
echo "# My Git Practice" > README.md
git status
git add README.md
git commit -m "Add initial README"
git log --oneline
```

## Important safety habits

- Never commit passwords, API keys, private keys, tokens, or production secrets.
- Check `git status` and review `git diff` before committing.
- Prefer small commits with clear messages.
- Do not use destructive commands on work you need. Learn what a command changes before running it.
- A Git commit is local until you push it to a remote such as GitHub.

## Recommended official resources

- Git documentation: https://git-scm.com/doc
- Pro Git book (free online): https://git-scm.com/book/en/v2
- GitHub Docs: https://docs.github.com/
- GitHub Skills: https://skills.github.com/

## Publishing this study material on GitHub

1. On GitHub, create a **new empty repository** named `git-github-study-material`. Do not initialize it with a README if you plan to push this folder as-is.
2. Extract this project ZIP and open a terminal in the extracted `git-github-study-material` folder.
3. Run the following commands, replacing `YOUR-USERNAME` with your GitHub username:

```bash
git init
git add .
git commit -m "Add Git and GitHub study material"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/git-github-study-material.git
git push -u origin main
```

GitHub may ask you to authenticate using a browser or credential manager. Do not put your password or token directly into the repository or command history.

If you already have a repository with files in it, review GitHub's instructions before pushing so you do not overwrite or conflict with existing work.
