# 01 — Git and Version Control

## What is version control?

Version control records changes over time. It helps you compare revisions, recover earlier work, and understand who changed what and why.

Without version control, people often create confusing copies such as `project-final`, `project-final-v2`, and `project-final-really-final`.

## What is Git?

Git is a distributed version control system. A Git repository stores snapshots and history locally. You can commit changes without an internet connection.

## What is GitHub?

GitHub is an online platform for hosting Git repositories and collaborating through issues, pull requests, reviews, project tools and automation.

**Git is the tool; GitHub is one place to host and collaborate on Git projects.** Git can also work with other hosting services or entirely locally.

## Key terms

- **Repository:** a project and its version history.
- **Working tree:** files as they currently exist on disk.
- **Staging area/index:** selected changes for the next commit.
- **Commit:** a named snapshot of tracked project content.
- **Branch:** a movable name for a line of development.
- **Remote:** a named reference to another repository.
- **Clone:** create a local copy of a remote repository.
- **Merge:** combine changes from branches.
- **Conflict:** overlapping changes Git cannot safely combine automatically.
- **Pull request:** a platform feature to discuss, review and merge proposed changes.

## The three local areas

```text
Working tree  --git add-->  Staging area  --git commit-->  Local history
      ^                          |                              |
      |---------------- edit files -----------------------------|
```

A commit is not automatically uploaded to GitHub. `git push` sends local commits to a remote.

## When should you use Git?

Use it for source code, documentation, scripts, configuration templates and other text-based project files. Git can store binary files too, but large binaries may require additional planning.

## Check your understanding

1. Why is Git useful?
2. Is GitHub required to use Git?
3. What is the staging area?
4. What is the difference between a commit and a push?

**Answers:** See `11-REVISION/answer-key.md`.
