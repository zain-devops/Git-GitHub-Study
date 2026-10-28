# 09 — Merge Conflicts

A conflict happens when Git cannot automatically reconcile changes, often because two branches edited overlapping lines.

## Conflict markers

```text
<<<<<<< HEAD
Current branch version
=======
Incoming branch version
>>>>>>> feature-branch
```

## Resolution process

1. Run `git status`.
2. Open each conflicted file.
3. Read both versions and edit the file into the intended final result.
4. Remove the conflict markers.
5. Run tests or review the file.
6. Stage the resolved file.
7. Complete the merge commit if Git requires one.

```bash
git add path/to/file
git status
git commit
```

Do not choose a side blindly. The correct resolution may combine parts of both versions.

## Practice safely

Create two branches from the same base. Change the same line differently on each branch, commit each change, then merge one into the other. Resolve the conflict.
