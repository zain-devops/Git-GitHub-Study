# 07 — Undo Changes Safely

First run `git status`. Know whether your changes are unstaged, staged, committed locally, or already shared.

## Unstage a file but keep edits

```bash
git restore --staged README.md
```

## Discard unstaged edits in a file

```bash
git restore README.md
```

⚠️ This discards the uncommitted edits in that file. Check `git diff` first.

## Correct the latest commit

```bash
git add corrected-file.md
git commit --amend
```

Amending changes the latest commit. Avoid amending a commit that has already been shared unless you understand the impact and your team agrees.

## Revert a commit

```bash
git revert COMMIT_ID
```

This creates a new commit that reverses the selected commit's changes. It is often the safer option for already-shared history.

## Reset caution

`git reset` has several modes and changes where branch/staging pointers or contents sit. `git reset --hard` can discard local changes. Don't use it as a first troubleshooting step.

## Exercise

In a disposable repository, stage a file and unstage it. Then make an edit and restore it. Observe the difference between the two operations.
