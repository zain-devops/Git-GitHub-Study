# 11 — Fetch, Pull and Push

```bash
git fetch origin
git pull
git push
```

- **fetch:** downloads remote updates and updates remote-tracking references; it does not normally merge into your current branch.
- **pull:** fetches and integrates remote updates into the current branch. Exact behavior depends on Git configuration.
- **push:** sends local commits to a remote branch.

## Typical workflow

1. Check `git status` and your current branch.
2. Synchronize with the team's agreed workflow.
3. Create a feature branch.
4. Make focused changes and commit them.
5. Push the branch.
6. Open a pull request.
7. Review and merge according to the team's process.

If a push is rejected, don't force-push blindly. Fetch remote updates, inspect the history, and decide how to integrate the changes.

Official reference: https://docs.github.com/en/get-started/using-git/about-git
