# 06 — Ignore Generated and Private Files

Create a `.gitignore` file in the repository root.

```gitignore
# Environment files and secrets
.env
.env.*
!.env.example
*.pem
*.key

# Dependencies and build output
node_modules/
dist/
build/
__pycache__/
*.pyc

# Editor and operating system files
.vscode/
.idea/
.DS_Store
Thumbs.db

# Temporary files
*.tmp
*.swp
```

These are examples. Choose rules appropriate for your actual project.

Check whether a path is ignored:

```bash
git check-ignore -v path/to/file
```

**Important:** `.gitignore` normally affects untracked files. It does not automatically stop tracking a file already committed. If you accidentally commit a secret, revoke or rotate it immediately. Deleting it in a later commit does not erase it from history.

To stop tracking a file but keep it locally:

```bash
git rm --cached path/to/file
```

Review the staged result before committing.
