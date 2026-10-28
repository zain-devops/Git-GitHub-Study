# 08 — Branches

Branches let you work on features or fixes separately from the main development line.

```bash
git branch
git switch -c feature/add-about-page
```

Make a change, then:

```bash
git status
git add .
git commit -m "Add about page"
git switch main
git merge feature/add-about-page
git branch -d feature/add-about-page
```

If the default branch is named something other than `main`, switch to the correct branch. Confirm with `git branch`.

## Naming examples

- `feature/user-profile`
- `fix/login-validation`
- `docs/installation-guide`

Use names your team understands. Branch names and rules vary by project.
