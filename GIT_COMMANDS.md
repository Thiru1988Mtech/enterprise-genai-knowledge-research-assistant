# Git Commands Reference
## Enterprise GenAI Knowledge & Research Assistant

This file records the Git commands used during this project,
what each command does, and why we used it.

---

# 1. Project Git Setup

## 1.1 Check Git Installation

### Command

git --version

### What it does

Displays the installed Git version.

### Why we used it

To verify that Git is installed and available before starting
version control for the project.

### Result

Git version 2.55.0.windows.1

---

# 2. Initialize Git Repository

## 2.1 Create Local Git Repository

### Command

git init

### What it does

Creates a new `.git` directory inside the project folder.

### Why we used it

To convert our project folder into a Git repository so Git
can track changes and maintain project history.

### Project

Enterprise GenAI Knowledge & Research Assistant

### Local Path

D:\Enterprise GenAI Knowledge & Research Assistant

---

# 3. Git Safe Directory

## 3.1 Configure Safe Directory

### Command

git config --global --add safe.directory "D:/Enterprise GenAI Knowledge & Research Assistant"

### What it does

Tells Git that this project directory is trusted.

### Why we used it

Git reported a "dubious ownership" warning for the D: drive
directory. We explicitly marked this project directory as safe.

---

# 4. Check Repository Status

## 4.1 Check Git Status

### Command

git status

### What it does

Shows the current state of the Git repository.

It can show:

- Untracked files
- Modified files
- Staged files
- Current branch
- Commit status
- Synchronization with the remote repository

### Why we used it

We use `git status` frequently to understand what is happening
before performing Git operations.

---

# 5. Connect GitHub Repository

## 5.1 Add GitHub Remote

### Command

git remote add origin "https://github.com/Thiru1988Mtech/enterprise-genai-knowledge-research-assistant.git"

### What it does

Connects the local Git repository to the GitHub repository.

### Why we used it

Our local project needs a remote GitHub repository where the
project history can be stored and shared.

### Remote Name

origin

### GitHub Repository

enterprise-genai-knowledge-research-assistant

---

# 6. Verify GitHub Remote

## 6.1 Check Remote

### Command

git remote -v

### What it does

Displays the configured remote repository URLs.

### Why we used it

To verify that the local project is connected to the correct
GitHub repository before pushing code.

---

# 7. Python Virtual Environment

## 7.1 Create Virtual Environment

### Command

py -3.11 -m venv .venv

### What it does

Creates an isolated Python virtual environment named `.venv`.

### Why we used it

The project uses Python 3.11.

A virtual environment keeps this project's Python packages
separate from other Python projects on the computer.

### Important

`.venv` must NOT be committed to Git.

It is therefore included in `.gitignore`.

---

# 8. Git Ignore

## 8.1 .gitignore

### File

.gitignore

### What it does

Tells Git which files and folders should not be tracked.

### Why we used it

Some files are local-only or may contain sensitive information.

Examples:

- `.venv/`
- `.env`
- `.env.*`
- `__pycache__/`
- `.vscode/`

This prevents unnecessary files and secrets from being committed.

---

# 9. Project Documentation

## 9.1 README.md

### File

README.md

### What it does

Provides the main documentation/front page of the GitHub project.

### Why we created it

Anyone opening the repository should understand:

- What the project is
- Main architecture
- Technology stack
- Project lifecycle

---

# 10. Project Progress Tracking

## 10.1 PROGRESS.md

### File

PROGRESS.md

### What it does

Tracks project implementation and learning progress.

### Why we created it

This is our master project tracker.

It helps us understand:

- What has been completed
- Current phase
- Next phase
- Learning progress
- Important project decisions

---

# 11. Git Command Learning Reference

## 11.1 GIT_COMMANDS.md

### File

GIT_COMMANDS.md

### What it does

Stores the Git commands used throughout this project.

### Why we created it

We want to learn Git while building the project.

Whenever we learn a new Git command, we will add it here so
the commands can be reused in future projects.

---

# 12. Untracked Files

## 12.1 Meaning of Untracked

Example:

git status

Output:

Untracked files:
    .gitignore
    README.md
    PROGRESS.md

### What it means

Git has detected the files, but Git is not tracking them yet.

### Why this happens

The files were newly created.

Git does not automatically include new files in a commit.

---

# 13. Stage Files

## 13.1 git add

### Command

git add <file>

### What it does

Moves a file into the staging area.

### Why we used it

We need to explicitly tell Git which files should be included
in the next commit.

### Example

git add .gitignore README.md PROGRESS.md

### Git Flow

Untracked
    ↓
git add
    ↓
Staged

---

# 14. Staged Files

## 14.1 Meaning of Staged

Example:

Changes to be committed:

    new file: .gitignore
    new file: PROGRESS.md
    new file: README.md

### What it means

Git has prepared these files for the next commit.

### Why staging is useful

It gives us an opportunity to review and select exactly what
should be included in the next commit.

---

# 15. Create Commit

## 15.1 git commit

### Command

git commit -m "Initial project setup"

### What it does

Creates a permanent checkpoint in the local Git history.

### Why we used it

We completed the initial project setup and wanted to create
the first version of the project history.

### Commit

Initial project setup

### Git Flow

Staged
    ↓
git commit
    ↓
Local Git History

---

# 16. Push to GitHub

## 16.1 git push

### Command

git push -u origin master

### What it does

Uploads the local commit to the GitHub repository.

### Why we used it

The commit existed locally, but we also wanted the project
history to exist on GitHub.

### Meaning

origin

    → GitHub remote repository

master

    → Local branch being pushed

-u

    → Sets origin/master as the upstream branch

---

# 17. Verify Synchronization

## 17.1 git status

### Command

git status

### Result

On branch master

Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean

### What it means

Our local project and GitHub repository are synchronized.

### Important Concept

"working tree clean"

means there are no uncommitted changes.

---

# 18. Git Workflow Learned So Far

Our current basic Git workflow is:

Create / Modify File
        ↓
git status
        ↓
git add
        ↓
Staged
        ↓
git commit
        ↓
Local Git History
        ↓
git push
        ↓
GitHub
        ↓
git status
        ↓
Verify

---

# 19. Commands Used in This Project So Far

| Command | Purpose |
|---|---|
| git --version | Verify Git installation |
| git init | Initialize Git repository |
| git config --global --add safe.directory | Trust project directory |
| git status | Check repository state |
| git remote add origin | Connect GitHub repository |
| git remote -v | Verify GitHub remote |
| git add | Stage files |
| git commit | Create local checkpoint |
| git push | Upload commits to GitHub |

---

# 20. Project Git Status

## Current Branch

master

## Remote

origin

## GitHub Repository

enterprise-genai-knowledge-research-assistant

## Current State

Local repository synchronized with GitHub.

## First Commit

Initial project setup

---

# 21. Future Git Commands

As the project develops, we will add and learn commands such as:

- git log
- git diff
- git branch
- git switch
- git merge
- git pull
- git fetch
- git restore
- git reset
- git clone
- git tag
- git stash

Each command will be added with:

1. Command
2. What it does
3. Why we use it
4. Example from this project