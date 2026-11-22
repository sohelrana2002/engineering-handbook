# Git Basics

Git is a distributed version control system (DVCS) used to track changes in source code, manage project history, and support collaboration among developers.

It allows developers to work independently, maintain different versions of a project, and integrate changes safely.

## Table of Contents

- [1. What is Version Control?](#1-what-is-version-control)
- [2. What is Git?](#2-what-is-git)
- [3. Git vs GitHub](#3-git-vs-github)
- [4. Why Use Git?](#4-why-use-git)
- [5. Git Architecture](#5-git-architecture)
- [6. Git Repository](#6-git-repository)
- [7. Git Areas](#7-git-areas)
- [8. Git File Lifecycle](#8-git-file-lifecycle)
- [9. Basic Git Workflow](#9-basic-git-workflow)
- [10. Important Git Terminology](#10-important-git-terminology)
- [11. Git Installation](#11-git-installation)
- [12. Initial Git Configuration](#12-initial-git-configuration)
- [13. Initialize a Repository](#13-initialize-a-repository)
- [14. Clone an Existing Repository](#14-clone-an-existing-repository)
- [15. First Commit](#15-first-commit)
- [16. Push Changes to GitHub](#16-push-changes-to-github)
- [17. Best Practices](#17-best-practices)
- [References](#references)

---

## 1. What is Version Control?

Version Control is a system that records changes made to files over time. It allows developers to track modifications, restore previous versions, and collaborate without losing existing work.

### Types of Version Control Systems

1. **Local Version Control System (LVCS):** Tracks file changes locally on a single machine.
2. **Centralized Version Control System (CVCS):** Stores project history on a central server shared by multiple developers.
3. **Distributed Version Control System (DVCS):** Every developer maintains a local copy of the repository and its version history.

Git is a Distributed Version Control System (DVCS).

## 2. What is Git?

Git is a free and open-source distributed version control system designed to handle projects of different sizes efficiently.

It tracks changes using commits, allowing developers to maintain a complete history of their work.

### Key Features

- Distributed version control.
- Branching and merging.
- Lightweight and fast operations.
- Commit history tracking.
- Local development without an internet connection.
- Collaboration across multiple developers.
- Ability to restore previous project states.

## 3. Git vs GitHub

Git and GitHub are related but serve different purposes.

| Git                          | GitHub                                     |
| ---------------------------- | ------------------------------------------ |
| Version control system       | Cloud-based development platform           |
| Installed locally            | Accessed through web or Git clients        |
| Tracks file changes          | Hosts Git repositories                     |
| Manages commits and branches | Provides Pull Requests and code reviews    |
| Works offline                | Requires internet for remote collaboration |
| Open-source software         | GitHub is a hosted platform                |

Other Git hosting platforms include GitLab, Bitbucket, and Codeberg.

## 4. Why Use Git?

Git helps developers:

- Track every meaningful change in a project.
- Collaborate with multiple developers.
- Create isolated development branches.
- Review code before integration.
- Revert unwanted changes.
- Maintain project history.
- Manage releases and production code safely.

## 5. Git Architecture

Git manages project changes through different areas.

### Git Architecture Overview

```text
        Working Directory
                |
                | git add
                v
         Staging Area
                |
                | git commit
                v
        Local Repository
                |
                | git push
                v
        Remote Repository
             (GitHub)
```

### Components

**Working Directory**

The directory containing the project files where developers create, modify, and delete files.

**Staging Area (Index)**

An intermediate area where changes are prepared before creating a commit.

**Local Repository**

Stores committed snapshots and project history on the developer's machine.

**Remote Repository**

A repository hosted on a remote platform such as GitHub, allowing developers to share and synchronize project changes.

## 6. Git Repository

A Git repository is a project directory managed by Git.

It contains project files and a hidden `.git` directory that stores repository metadata, configuration, references, and object data.

### Types of Repositories

1. **Local Repository:** A repository stored on your local machine.
2. **Remote Repository:** A repository hosted on a remote server or platform.

## 7. Git Areas

Git uses three primary areas to manage changes.

| Area              | Purpose                    |
| ----------------- | -------------------------- |
| Working Directory | Modify project files       |
| Staging Area      | Prepare changes for commit |
| Repository        | Store committed changes    |

The remote repository is an additional collaboration destination.

## 8. Git File Lifecycle

Git tracks files through different states.

### File States

- **Untracked:** A new file that Git is not tracking.
- **Unmodified:** A tracked file with no changes since its last commit.
- **Modified:** A tracked file that has been changed.
- **Staged:** Changes selected for the next commit.

### Lifecycle Diagram

```text
       Untracked
           |
           | git add
           v
         Staged
           |
           | git commit
           v
       Unmodified
           |
           | Modify file
           v
        Modified
           |
           | git add
           v
         Staged
```

## 9. Basic Git Workflow

A typical Git development workflow follows these steps:

1. Create or clone a repository.
2. Make changes to project files.
3. Check the current repository status.
4. Stage the required changes.
5. Commit the staged changes.
6. Push commits to the remote repository.

Example:

```bash
git status
git add .
git commit -m "feat: add user authentication"
git push origin main
```

Note: The example uses `main` as the target branch. In a team workflow, push to the appropriate feature or development branch.

## 10. Important Git Terminology

| Term           | Explanation                                                |
| -------------- | ---------------------------------------------------------- |
| Repository     | A project managed by Git                                   |
| Commit         | A recorded snapshot of staged changes                      |
| Branch         | An independent line of development                         |
| Merge          | Integrating changes from one branch into another           |
| Clone          | Creating a local copy of a remote repository               |
| Fork           | Creating your own GitHub-hosted copy of another repository |
| Pull           | Fetching and integrating remote changes                    |
| Fetch          | Downloading remote updates without integrating them        |
| Push           | Uploading local commits to a remote repository             |
| HEAD           | Reference to the currently checked-out commit              |
| Remote         | A reference to another repository                          |
| Merge Conflict | A situation where Git cannot automatically combine changes |
| Staging        | Preparing changes for the next commit                      |
| Working Tree   | The current checked-out project files                      |

## 11. Git Installation

Download Git from the official website:

https://git-scm.com/

Verify installation:

```bash
git --version
```

Expected output (version may differ):

```text
git version 2.x.x
```

## 12. Initial Git Configuration

Configure your Git identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Check configuration:

```bash
git config --global --list
```

### Configuration Levels

| Level      | Scope                         |
| ---------- | ----------------------------- |
| `--system` | All users on the system       |
| `--global` | Current operating system user |
| `--local`  | Current repository only       |

Local configuration overrides global configuration, and global configuration overrides system configuration.

## 13. Initialize a Repository

Navigate to your project directory:

```bash
cd my-project
```

Initialize Git:

```bash
git init
```

This creates a `.git` directory and initializes a new local repository.

Check repository status:

```bash
git status
```

## 14. Clone an Existing Repository

To download an existing remote repository:

```bash
git clone https://github.com/username/repository.git
```

Navigate into the cloned repository:

```bash
cd repository
```

Git automatically configures the original repository as the default remote named `origin`.

## 15. First Commit

Create a file:

```bash
touch README.md
```

Stage the file:

```bash
git add README.md
```

Create a commit:

```bash
git commit -m "docs: add project README"
```

Verify commit history:

```bash
git log
```

## 16. Push Changes to GitHub

If you have already created a remote GitHub repository, connect it:

```bash
git remote add origin https://github.com/username/repository.git
```

Check remote configuration:

```bash
git remote -v
```

Set the default branch to `main` if needed:

```bash
git branch -M main
```

Push the branch:

```bash
git push -u origin main
```

The `-u` option sets the upstream tracking relationship, making subsequent pushes easier.

## 17. Best Practices

- Write meaningful commit messages.
- Commit small and logically related changes.
- Use `.gitignore` to exclude unnecessary files.
- Never commit secrets, API keys, or credentials.
- Create branches for isolated development tasks.
- Review changes before committing.
- Pull or fetch remote changes regularly.
- Avoid rewriting shared branch history without coordination.
- Keep your repository history understandable.
- Use Pull Requests for collaborative code integration.

## References

- [Official Git Documentation](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/en/v2)
- [GitHub Documentation](https://docs.github.com/en)
- [Git Reference](https://git-scm.com/docs)
