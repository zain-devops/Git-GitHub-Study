# Exercises and Revision Questions

Complete the tasks in order. Use a disposable practice repository so you can safely experiment.

## Beginner exercises

- [ ] Install Git and display its version.
- [ ] Configure your Git name and email.
- [ ] Create a folder named `git-lab` and initialize it as a repository.
- [ ] Add a `README.md`, stage it, and make the first commit.
- [ ] Edit the README and inspect the result with `git diff`.
- [ ] Stage the change and inspect it with `git diff --staged`.
- [ ] Make two more commits with clear messages.
- [ ] Display a compact commit history.

## Intermediate exercises

- [ ] Create a branch named `feature/about`.
- [ ] Add an `about.md` file and commit it on that branch.
- [ ] Merge the feature branch into `main`.
- [ ] Create a `.gitignore` file and ignore a practice file such as `notes.tmp`.
- [ ] Unstage a staged file without discarding its edits.
- [ ] Clone your GitHub repository into a second directory.
- [ ] Make a change, commit it, and push it to GitHub.

## Collaboration exercises

- [ ] Create a GitHub issue describing a documentation improvement.
- [ ] Create a feature branch and push it to GitHub.
- [ ] Open a pull request and write a useful summary.
- [ ] Review the diff before merging.
- [ ] Practice a merge conflict in a disposable repository and resolve it.

## Revision questions

1. What problem does version control solve?
2. What is the difference between Git and GitHub?
3. What is the difference between the working directory, staging area, and repository history?
4. What does `git add` do?
5. What information does a commit contain?
6. Why should feature work happen on a branch?
7. What is the difference between `git fetch` and `git pull`?
8. What does `git push` do?
9. What is a remote named `origin`?
10. What is a pull request used for?
11. How do you unstage a file while keeping its edits?
12. Why is `git restore` potentially destructive?
13. What should you do if you accidentally commit an API key?
14. What causes a merge conflict?
15. Why should you review `git diff` before committing?

## Answer key

1. It records changes, supports comparison and recovery, and enables collaboration.
2. Git is the version-control tool; GitHub hosts Git repositories and provides collaboration features.
3. The working directory holds current edits; the staging area selects changes for the next commit; history stores committed snapshots.
4. It stages selected content for the next commit.
5. A snapshot of project content, metadata such as author/date, a message, and a parent relationship.
6. It isolates work and makes review and integration easier.
7. `fetch` downloads remote information; `pull` fetches and integrates changes into the current branch.
8. It sends local commits to a remote repository.
9. It is a conventional name for a remote repository.
10. To propose, discuss, review, and merge changes on GitHub.
11. Use `git restore --staged FILE`.
12. It discards uncommitted edits in the selected file.
13. Revoke or rotate the key immediately, remove it from the code, and follow the platform/team process for any history cleanup.
14. Git cannot automatically reconcile overlapping changes.
15. To catch unintended changes, sensitive data, or mistakes before recording them.
