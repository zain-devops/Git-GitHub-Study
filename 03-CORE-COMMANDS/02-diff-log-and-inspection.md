# 05 — Inspect Changes and History

```bash
git status
git diff
git diff --staged
git log
git log --oneline
git log --oneline --graph --decorate --all
git show HEAD
git show COMMIT_ID
```

- `status`: what is modified, staged, untracked, or ignored.
- `diff`: unstaged changes.
- `diff --staged`: changes staged for the next commit.
- `log`: commit history.
- `show`: details of a commit or object.

## Why inspect before committing?

Reviewing the diff can catch accidental files, debugging output, credentials, unrelated edits and incomplete work.

## Exercise

Make two commits, then use `git log --oneline --graph` and `git show` to inspect them. Predict which files are included in each commit before running the commands.
