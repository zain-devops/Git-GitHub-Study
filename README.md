<div align="center">

# 🚀 Git & GitHub — Complete Learning Course

### Beginner → Confident User → Team Collaboration

**A free, folder-wise, hands-on course with lessons, practical labs, projects, revision notes, and official learning resources.**

![Git](https://img.shields.io/badge/Git-Version%20Control-F05032?logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Collaboration-181717?logo=github&logoColor=white)
![Cost](https://img.shields.io/badge/Cost-Free-2ea44f)
![Format](https://img.shields.io/badge/Format-Markdown-blue)

</div>

---

## 👋 Welcome!

This repository teaches Git and GitHub from the ground up. Read the lessons in order, type the commands yourself, complete the labs, and finish the capstone project. No prior Git experience is required.

> 🎯 **End goal:** Confidently track changes, manage branches, recover from common mistakes, publish repositories, collaborate through pull requests, and understand a professional Git workflow.

## 📚 Course Contents

- [🚀 Start Here](./00-START-HERE/)
- [📘 Foundations](./01-FOUNDATIONS/)
- [⚙️ Setup](./02-SETUP/)
- [💻 Core Commands](./03-CORE-COMMANDS/)
- [↩️ Tracking and Undo](./04-TRACKING-AND-UNDO/)
- [🌿 Branching and Merging](./05-BRANCHING-AND-MERGING/)
- [☁️ GitHub Remote](./06-GITHUB-REMOTE/)
- [🤝 Collaboration](./07-COLLABORATION/)
- [🧠 Advanced Git](./08-ADVANCED-GIT/)
- [🔐 Security and Best Practices](./09-SECURITY-AND-BEST-PRACTICES/)
- [🧪 Practice Projects](./10-PROJECTS/)
- [📝 Revision and Quiz](./11-REVISION/)
- [🎥 Learning Resources](./12-RESOURCES/)
- [🌐 GitHub Pages](./13-GITHUB-PAGES/)

🚀 Git Learning Roadmap

Click any topic to jump to its learning section.

flowchart TD
    A(["🚀 Start Here"]) --> B["01 · Foundations"]
    B --> C["02 · Setup"]
    C --> D["03 · Core Commands"]
    D --> E["04 · Tracking & Undo"]
    E --> F["05 · Branching & Merging"]
    F --> G["06 · GitHub Remote"]
    G --> H["07 · Collaboration"]
    H --> I["08 · Advanced Git"]
    I --> J["09 · Security & Best Practices"]
    J --> K["10 · Projects & Capstone"]
    K --> L["11 · Revision"]
    L --> M(["🏁 Finish · GitHub Pages"])

    click A "#start-here" "Start learning"
    click B "#01-foundations" "Learn foundations"
    click C "#02-setup" "Set up Git"
    click D "#03-core-commands" "Learn core commands"
    click E "#04-tracking-and-undo" "Track changes and undo"
    click F "#05-branching-and-merging" "Learn branches"
    click G "#06-github-remote" "Connect to GitHub"
    click H "#07-collaboration" "Collaborate"
    click I "#08-advanced-git" "Advanced Git"
    click J "#09-security-and-best-practices" "Git security"
    click K "#10-projects-and-capstone" "Build projects"
    click L "#11-revision" "Revise Git"
    click M "#github-pages-optional" "Publish your project"

    style A fill:#16a34a,color:#fff,stroke:#166534
    style B fill:#dbeafe,color:#1e3a8a,stroke:#2563eb
    style C fill:#fef3c7,color:#78350f,stroke:#d97706
    style D fill:#fce7f3,color:#831843,stroke:#db2777
    style E fill:#ede9fe,color:#4c1d95,stroke:#7c3aed
    style F fill:#cffafe,color:#164e63,stroke:#0891b2
    style G fill:#fee2e2,color:#7f1d1d,stroke:#dc2626
    style H fill:#d1fae5,color:#064e3b,stroke:#059669
    style I fill:#dbeafe,color:#1e40af,stroke:#1d4ed8
    style J fill:#fef3c7,color:#92400e,stroke:#b45309
    style K fill:#fce7f3,color:#9d174d,stroke:#be185d
    style L fill:#ede9fe,color:#5b21b6,stroke:#6d28d9
    style M fill:#16a34a,color:#fff,stroke:#166534

## 🎬 Start with these free videos and courses

**Official GitHub video**
- [A brief introduction to Git for beginners — GitHub](https://www.youtube.com/watch?v=r8jQ9hVA2qs)
- [GitHub for Beginners video series — official learning resources](https://docs.github.com/en/get-started/start-your-journey/git-and-github-learning-resources)

**Official Git video library**
- [Git project video library](https://git-scm.com/videos)
- [Pro Git book — free online](https://git-scm.com/book/en/v2)

**Official hands-on training**
- [GitHub Skills — free interactive courses](https://skills.github.com/)
- [GitHub learning resources](https://docs.github.com/en/get-started/start-your-journey/git-and-github-learning-resources)
- [GitHub Docs](https://docs.github.com/)

**Optional long-form third-party video**
- [Git and GitHub Tutorial for Beginners — Kevin Stratvert](https://www.youtube.com/watch?v=tRZGeaHPoaw)  
  This is a community tutorial, not an official GitHub video.

## 📅 Suggested 30-day plan

| Days | Focus | Outcome |
|---|---|---|
| 1–2 | Foundations | Explain Git, GitHub and repositories |
| 3–4 | Setup | Install and configure Git |
| 5–8 | Core commands | Create commits and inspect history |
| 9–11 | Tracking and undo | Ignore files and safely reverse changes |
| 12–15 | Branching | Branch, merge and resolve conflicts |
| 16–19 | GitHub remote | Clone, push, fetch and pull |
| 20–23 | Collaboration | Issues, pull requests and reviews |
| 24–26 | Advanced Git | Stash, rebase, tags and reflog |
| 27–29 | Projects | Finish labs and capstone |
| 30 | Revision | Quiz yourself and explain the workflow |

## ⚡ First practice session

After installing Git, open a terminal and run:

```bash
git --version
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main

mkdir git-practice
cd git-practice
git init
echo "# My Git Practice" > README.md
git status
git add README.md
git commit -m "Add first README"
git log --oneline
```

Use your own name and email. These commands create a practice repository on your computer; they do not publish anything online.

## 🛡️ Course rules for safe practice

- Never commit passwords, access tokens, private keys, or production secrets.
- Review `git status` and `git diff` before committing.
- Practise destructive commands only in a disposable repository.
- Use meaningful commit messages.
- Keep work in feature branches when appropriate.
- A commit is local until pushed to a remote repository.
- If a secret is accidentally committed, revoke or rotate it immediately; deleting it in a later commit is not enough.

## 🚀 Upload this course to your GitHub

1. Create an **empty** repository named `git-github-complete-course` at [github.com/new](https://github.com/new).
2. Extract this ZIP archive.
3. Open a terminal in the extracted `git-github-complete-course` folder.
4. Run the commands below, replacing `YOUR-USERNAME` with your GitHub username.

```bash
git init
git add .
git commit -m "Add complete Git and GitHub learning course"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/git-github-complete-course.git
git push -u origin main
```

If you already configured `origin`, inspect it with `git remote -v` rather than adding it again. Authenticate using GitHub's supported browser, credential manager, or SSH flow. Do not paste passwords or tokens into these study files.

## 🏁 Completion checklist

- [ ] I can explain Git vs GitHub.
- [ ] I can create a repo and make commits.
- [ ] I can read diffs and commit history.
- [ ] I can use `.gitignore` safely.
- [ ] I can branch, merge and resolve a conflict.
- [ ] I can clone, push, fetch and pull.
- [ ] I can open and review a pull request.
- [ ] I understand how to prevent and respond to secret leaks.
- [ ] I completed at least two practice projects.
- [ ] I can explain the workflow without copying commands blindly.

<div align="center">

**Learn → Practise → Commit → Collaborate → Repeat** 💻

</div>
