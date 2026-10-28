# 03 — Install and Configure Git

## Install

Download Git from the official site: https://git-scm.com/downloads

- **Windows:** use the official Git for Windows installer; Git Bash is included.
- **macOS:** follow the official installer guidance or use the available system package option.
- **Ubuntu/Debian:** `sudo apt update && sudo apt install git`
- **Other Linux distributions:** use the distribution's package manager.

Verify installation:

```bash
git --version
```

## Configure your identity

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
git config --list
```

Replace the sample details. The name and email are recorded in commits. You may use a GitHub-provided private email if you don't want to expose your personal email publicly.

## Configuration levels

- `--system`: system-wide settings, where supported and permitted.
- `--global`: your user account's settings.
- `--local`: the current repository's settings.

A repository-specific setting can override a global setting.

```bash
git config --global --get user.name
git config --local --list
```

## Terminal basics

| Command | Purpose |
|---|---|
| `pwd` | Show current directory on macOS/Linux/Git Bash |
| `ls` | List files on macOS/Linux/Git Bash |
| `cd folder-name` | Enter a folder |
| `cd ..` | Move to parent directory |
| `mkdir project` | Create a folder |
| `git help status` | Read command help |

Windows PowerShell also supports `cd`, `mkdir`, and `dir`; shell commands vary, while Git commands are generally the same.

## Exercise

1. Install Git.
2. Print the installed version.
3. Configure your name and email.
4. Check the settings.
5. Create a new folder for the rest of the course.
