# 13 — Intermediate Git Tools

Learn these after you are comfortable with commits, branches and merges.

## Stash temporary work

```bash
git stash push -m "Work in progress"
git stash list
git stash pop
```

A stash is temporary local storage, not a backup strategy.

## Tags

```bash
git tag
git tag -a v1.0.0 -m "First stable release"
git show v1.0.0
git push origin v1.0.0
```

Tags can identify releases or important points in history.

## Rebase

```bash
git fetch origin
git switch feature/my-change
git rebase origin/main
```

Rebase replays commits onto a new base and rewrites commit identities. If conflicts occur, resolve them and use `git rebase --continue`, or use `git rebase --abort` to stop the rebase. Avoid rebasing shared commits unless the team agrees.

## Cherry-pick

```bash
git cherry-pick COMMIT_ID
```

This applies the changes from a selected commit onto the current branch as a new commit. Check that this is the right way to bring the change over; it can duplicate work if used carelessly.

## Reflog

```bash
git reflog
```

The reflog records recent movements of local references and can help locate commits after certain mistakes. It is not a permanent backup, and entries can expire.

## Learn more

- https://git-scm.com/docs
- https://git-scm.com/book/en/v2
