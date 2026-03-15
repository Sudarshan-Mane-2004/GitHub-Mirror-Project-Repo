# Git & GitLab – Complete DevOps Guide

## Project Overview

This repository provides a comprehensive introduction to **Git and GitLab**, covering the essential concepts, commands, workflows, and advanced features such as **branching strategies, CI/CD pipelines, and repository mirroring**.

This guide is designed for **students, beginners, and DevOps engineers** who want to understand version control and collaborative development using Git and GitLab.

---

# Table of Contents

1. Introduction to Version Control
2. What is Git?
3. What is GitLab?
4. Git vs GitLab
5. Git Installation
6. Git Configuration
7. Git Repository Lifecycle
8. Essential Git Commands
9. Branching Strategy
10. Git Workflow
11. SSH Authentication
12. Merge Requests
13. Git Tags & Releases
14. GitLab CI/CD
15. Mirror Repository
16. Best Practices
17. Conclusion

---

# 1. Introduction to Version Control

Version control systems (VCS) help developers track and manage changes to source code. It enables teams to collaborate efficiently and maintain a history of code changes.

Benefits include:

* Tracking code history
* Collaboration among developers
* Reverting to previous versions
* Managing multiple development branches
* Maintaining code stability

---

# 2. What is Git?

Git is a **distributed version control system (DVCS)** created by **Linus Torvalds in 2005**. It allows developers to track changes and collaborate efficiently.

### Key Features

* Distributed architecture
* Fast performance
* Strong data integrity
* Powerful branching and merging
* Open-source and widely adopted

### Git Architecture

Git uses three main areas:

Working Directory → Staging Area → Local Repository

---

# 3. What is GitLab?

GitLab is a **web-based platform for hosting Git repositories** with additional DevOps features.

GitLab provides:

* Repository hosting
* Continuous Integration / Continuous Deployment (CI/CD)
* Issue tracking
* Code review system
* Project management tools
* Security scanning
* DevOps lifecycle management

---

# 4. Git vs GitLab

| Feature       | Git                    | GitLab                          |
| ------------- | ---------------------- | ------------------------------- |
| Type          | Version Control System | Git Repository Hosting Platform |
| Usage         | Tracks code changes    | Manages repositories online     |
| Interface     | Command Line           | Web Interface                   |
| Collaboration | Local collaboration    | Online collaboration            |

---

# 5. Git Installation

Download Git from:

https://git-scm.com/

Verify installation:

```bash
git --version
```

---

# 6. Git Configuration

Configure Git username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Check configuration:

```bash
git config --list
```

---

# 7. Git Repository Lifecycle

Typical lifecycle of a Git repository:

1. Initialize repository
2. Add files
3. Commit changes
4. Create branches
5. Push to remote repository
6. Collaborate using merge requests

---

# 8. Essential Git Commands

### Initialize Repository

```bash
git init
```

### Clone Repository

```bash
git clone <repository-url>
```

Example:

```bash
git clone https://gitlab.com/username/project.git
```

### Check Repository Status

```bash
git status
```

### Add Files

```bash
git add filename
```

Add all files:

```bash
git add .
```

### Commit Changes

```bash
git commit -m "commit message"
```

### Push Changes

```bash
git push origin main
```

### Pull Changes

```bash
git pull origin main
```

### View Commit History

```bash
git log
```

---

# 9. Git Branching Strategy

Branches allow developers to work on new features without affecting the main code.

Common branch types:

* **main / master** → production-ready code
* **develop** → integration branch
* **feature branches** → new features
* **hotfix branches** → urgent fixes

Create a branch:

```bash
git branch feature-login
```

Switch branch:

```bash
git checkout feature-login
```

Create and switch branch:

```bash
git checkout -b feature-login
```

Merge branch:

```bash
git merge feature-login
```

---

# 10. Git Workflow

Typical Git workflow used in teams:

1. Clone the repository
2. Create a feature branch
3. Make code changes
4. Add and commit changes
5. Push branch to GitLab
6. Create a **Merge Request**
7. Code review
8. Merge into main branch

---

# 11. SSH Authentication with GitLab

Generate SSH key:

```bash
ssh-keygen -t rsa
```

View public key:

```bash
cat ~/.ssh/id_rsa.pub
```

Add the key to GitLab:

Profile → Preferences → SSH Keys

Test connection:

```bash
ssh -T git@gitlab.com
```

---

# 12. Merge Requests

Merge Requests (MR) allow developers to review code before merging changes.

Benefits:

* Code review
* Discussion and feedback
* Automated testing
* Controlled merging

---

# 13. Git Tags and Releases

Tags are used to mark specific versions of software.

Create tag:

```bash
git tag v1.0
```

Push tag:

```bash
git push origin v1.0
```

---

# 14. GitLab CI/CD

GitLab CI/CD automates the process of building, testing, and deploying applications.

Pipeline configuration file:

```
.gitlab-ci.yml
```

Example pipeline:

```yaml
stages:
  - build
  - test

build_job:
  stage: build
  script:
    - echo "Building application"

test_job:
  stage: test
  script:
    - echo "Running tests"
```

---

# 15. Mirror Repository

A **Mirror Repository** is an exact copy of another repository that automatically synchronizes changes.

### Why Use Repository Mirroring?

* Backup repositories
* Migration between Git platforms
* Synchronizing GitHub and GitLab
* Disaster recovery

---

## Types of Repository Mirroring

### Push Mirroring

Changes from **GitLab are pushed to another repository** automatically.

Example:

GitLab → GitHub

---

### Pull Mirroring

GitLab **pulls updates from another repository**.

Example:

GitHub → GitLab

---

## Steps to Configure Mirroring

1. Open GitLab project
2. Navigate to **Settings**
3. Click **Repository**
4. Locate **Mirroring repositories**
5. Add repository URL
6. Select **Push** or **Pull**
7. Save configuration

---

# 16. Best Practices

* Use meaningful commit messages
* Keep commits small and focused
* Use branches for feature development
* Pull latest changes before pushing
* Review code before merging
* Use `.gitignore` for unnecessary files

---

# 17. Conclusion

Git and GitLab are essential tools for modern software development and DevOps practices. They enable efficient collaboration, maintain version history, and automate development workflows through CI/CD.

Understanding Git commands, branching strategies, and GitLab features such as repository mirroring will help developers manage projects efficiently and maintain high-quality code.

---

⭐ If you found this repository helpful, feel free to contribute or improve the documentation.
