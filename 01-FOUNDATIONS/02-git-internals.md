# 02 — How Git Thinks

## Snapshot model

Git commits represent snapshots of project content plus metadata and parent relationships. Git efficiently reuses stored content; it is not simply a folder of full copies of every version.

## Commit history

Each commit has an identifier, author information, timestamp, message, and parent commit(s). Most ordinary commits have one parent; a merge commit may have multiple parents.

## HEAD

`HEAD` normally points to the current branch (or a specific commit in detached-HEAD mode). Switching branches changes what commit your working tree is based on.

```bash
git status
git log --oneline --decorate --graph --all
git show HEAD
```

## Local and remote

- Local branch: a branch in your local repository.
- Remote-tracking branch: your local record of a branch on a remote, such as `origin/main`.
- Remote: a configured connection/name, often `origin`.

`git fetch` updates remote-tracking information. It does not normally merge those changes into your current branch.

## Why commits matter

Commits provide checkpoints. A clear history makes debugging, review, and rollback easier. Commit small, coherent changes with accurate messages.
