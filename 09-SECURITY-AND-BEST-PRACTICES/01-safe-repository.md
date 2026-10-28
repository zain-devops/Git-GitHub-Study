# 14 — Security and Professional Habits

## Never commit secrets

Examples include:
- Passwords
- API keys and access tokens
- Private SSH keys
- Production credentials
- Real `.env` files containing secrets

Use environment variables or a suitable secrets manager for application secrets. Commit a safe `.env.example` only when it contains placeholders rather than real credentials.

## If a secret is committed

1. Revoke or rotate it immediately.
2. Check logs and usage for possible misuse.
3. Remove it from the current code.
4. Follow the repository host/team process for history cleanup if required.
5. Notify the appropriate owner or security contact.

Removing a secret from the latest file does not remove it from earlier commits.

## Good workflow habits

- Review `git status` and `git diff` before staging.
- Review `git diff --staged` before committing.
- Make focused commits with meaningful messages.
- Use feature branches and pull requests when appropriate.
- Protect important branches in team repositories.
- Keep a backup of important work outside of risky experiments.
- Do not force-push shared branches without coordination.
- Check licenses before reusing third-party code or assets.

## Before pushing checklist

- [ ] Correct repository and branch?
- [ ] No secrets or private data?
- [ ] No unnecessary generated files?
- [ ] Diff reviewed?
- [ ] Commit message clear?
- [ ] Tests or checks run where relevant?
