# Version Control Systems
A Version Control System (VCS) is a tool used in software development and collaborative projects to track and manage changes to source code.

Tracks and records changes to the codebase, maintaining a structured project history.
Allows multiple developers to collaborate on the same project without overwriting each other's work.
Developers access and update a central repository, where project files are stored.
Enables teams to share updates and revert to earlier versions of the project when needed.

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/800a7fd3-505e-4e0e-a005-70705907ad68" />


# Components of Version Control Systems
Version Control Systems work using a few core concepts that help teams manage code changes and collaborate efficiently.

# Repository: A central location that stores all project files along with their complete change history and metadata like author and commit message.

# Revision: A specific saved version of a file or project, identified using a unique ID such as a hash or number.

# Branch: A separate copy of the codebase used to develop features or fix bugs without affecting the main code.

# Merging: The process of combining changes from one branch into another, which may sometimes require resolving conflicts.

# Commit: A snapshot of changes made to the codebase at a specific time, used to track and manage project history.


# Types of Version Control Systems
There are three main types of Version Control Systems:

# Local Version Control Systems (Local VCS)
A Local Version Control System (LVCS) stores all project versions on a single computer and is mainly used by one user without remote collaboration.

Characteristics:

No internet or server dependency.
Useful for individual projects.
Limited to single-user environments.

# Centralized Version Control Systems
In a Centralized Version Control System, all the files and their version history are stored in a single central server. Developers connect to this server to access or modify files.

Centralized-Version-Control
Update/Checkout: A developer retrieves the latest version of the files from the central server.
Make Changes: The developer works on the files.
Commit:The developer saves (commits) the changes directly back to the central server, making them immediately available to everyone else.
Pros:

Enables collaboration among multiple developers through a central repository.
Provides visibility into project activities and changes.
Allows fine-grained access control for administrators.
Cons:

Has a single point of failure because everything depends on the central repository.
If the server goes down, developers cannot collaborate or commit changes.
3. Distributed Version Control Systems
A Distributed Version Control System allows each developer to have a local repository along with a working copy of the project. Changes made in the local repository are not automatically visible to others.

# Distributed-Version-Control
Commit: Saves changes to the local repository, visible only to the developer.
Push: Uploads committed changes to the central/shared repository so others can access them.
Pull: Downloads changes from the central repository to the local repository.
Note: DVCS uses a two-step process (commit -> push) to share changes with other developers


# Git and GitHub for DevOps

## 1. Introduction

Git and GitHub are essential tools used by developers and DevOps engineers to manage source code, track changes, collaborate with team members, and support CI/CD pipelines.

## 2. What is Git?

Git is a distributed version control system used to track changes in files and source code.

### Benefits of Git
- Tracks code changes.
- Maintains version history.
- Helps restore previous versions.
- Supports branching and merging.
- Enables multiple developers to work on the same project.

## 3. What is GitHub?

GitHub is a cloud-based platform for hosting Git repositories and collaborating on projects.

### Benefits of GitHub
- Stores repositories online.
- Enables team collaboration.
- Supports pull requests and code reviews.
- Integrates with CI/CD tools.
- Provides issue tracking and project management.

## 4. Difference Between Git and GitHub

| Git | GitHub |
|---|---|
| Version control tool | Online hosting and collaboration platform |
| Works locally on your computer | Hosts repositories remotely |
| Tracks changes and commits | Stores repositories and supports reviews |
| Supports branching and merging | Supports pull requests and team collaboration |

## 5. Why Git and GitHub Are Important in DevOps

DevOps engineers use Git and GitHub to manage:

- Application source code
- Dockerfiles
- Kubernetes YAML files
- Terraform configuration files
- Jenkins pipeline scripts
- GitHub Actions workflows
- Shell scripts and deployment configurations

### Basic DevOps Workflow

Developer → Git → GitHub → CI/CD Pipeline → Testing and Build → Deployment

Git tracks changes, GitHub hosts the repository, and CI/CD tools automate testing, building, and deployment.

## 6. Install Git

Download Git from:

https://git-scm.com/downloads

Verify the installation:

```bash
git --version
```

## 7. Configure Git

Configure your name and email before making commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Verify your configuration:

```bash
git config --global --list
```

## 8. Important Git Commands

### Initialize a Repository

```bash
git init
```

Initializes a new local Git repository.

### Check Repository Status

```bash
git status
```

Displays the status of files and changes.

### Add Files to the Staging Area

```bash
git add filename
```

Stages a specific file.

```bash
git add .
```

Stages changes in the current directory.

### Commit Changes

```bash
git commit -m "Initial commit"
```

Saves staged changes in the local repository history.

### View Commit History

```bash
git log
```

Displays commit history.

```bash
git log --oneline
```

Displays a compact commit history.

### View File Changes

```bash
git diff
```

Displays unstaged changes.

## 9. Create a GitHub Repository

1. Open https://github.com
2. Sign in to your account.
3. Click the **+** menu and select **New repository**.
4. Enter a repository name.
5. Select Public or Private.
6. Create the repository.

## 10. Push Local Code to GitHub

### Step 1: Create a Project Folder

```bash
mkdir devops-git-demo
cd devops-git-demo
```

### Step 2: Initialize Git

```bash
git init
```

### Step 3: Create a README File

```bash
echo "# My DevOps Project" > README.md
```

### Step 4: Stage and Commit

```bash
git add README.md
git commit -m "Add README file"
```

### Step 5: Connect to GitHub

Replace the URL with your actual GitHub repository URL.

```bash
git remote add origin https://github.com/YOUR-USERNAME/devops-git-demo.git
```

Check the remote:

```bash
git remote -v
```

### Step 6: Push to GitHub

```bash
git branch -M main
git push -u origin main
```

Your local project is now available in your GitHub repository.

## 11. Clone an Existing Repository

Use `git clone` to copy an existing remote repository to your computer.

```bash
git clone https://github.com/OWNER/REPOSITORY.git
```

Move into the cloned project:

```bash
cd REPOSITORY
```

## 12. Pull Changes from GitHub

```bash
git pull
```

Fetches and integrates changes from the configured remote branch.

## 13. Push New Changes

Whenever you modify tracked project files, you can use:

```bash
git status
git add .
git commit -m "Update project files"
git push
```

Remember:

- `git add` stages changes.
- `git commit` saves changes locally.
- `git push` sends committed changes to GitHub.

## 14. Git Branching

A branch allows developers to work on a feature independently of the main branch.

### Create a Branch

```bash
git branch feature-1
```

### Create and Switch to a Branch

```bash
git switch -c feature-1
```

### List Branches

```bash
git branch
```

### Switch to the Main Branch

```bash
git switch main
```

### Merge a Branch

Switch to the branch that should receive the changes, then run:

```bash
git merge feature-1
```

### Push a Feature Branch

```bash
git push -u origin feature-1
```

## 15. Pull Requests

A pull request (PR) is used to propose changes from one branch to another.

Typical workflow:

1. Create a feature branch.
2. Make changes to the project.
3. Commit and push the changes.
4. Open a pull request on GitHub.
5. Review and test the changes.
6. Merge the approved pull request.

Pull requests help teams review code before merging changes into the main branch.

## 16. Git Remote Commands

Display configured remotes:

```bash
git remote -v
```

Add a remote repository:

```bash
git remote add origin REPOSITORY_URL
```

Change the remote URL:

```bash
git remote set-url origin REPOSITORY_URL
```

## 17. Delete or Restore Changes

Discard unstaged changes in a file:

```bash
git restore filename
```

Remove a tracked file and stage the removal:

```bash
git rm filename
```

**Warning:** These commands can discard work or remove files. Review your changes before running them.

## 18. The .gitignore File

The `.gitignore` file tells Git which untracked files to ignore.

Example:

```gitignore
*.log
.env
__pycache__/
*.tfstate
*.tfstate.*
```

Never commit passwords, access tokens, private keys, or other secrets to a repository.

## 19. Common Git Commands Summary

| Command | Purpose |
|---|---|
| `git init` | Initialize a repository |
| `git clone URL` | Clone a repository |
| `git status` | Check file status |
| `git add .` | Stage changes |
| `git commit -m "message"` | Commit changes |
| `git log --oneline` | View commit history |
| `git diff` | View unstaged changes |
| `git branch` | List branches |
| `git switch -c branch-name` | Create and switch branches |
| `git merge branch-name` | Merge a branch |
| `git fetch` | Download remote updates |
| `git pull` | Fetch and integrate remote changes |
| `git push` | Upload local commits |
| `git remote -v` | Display remote URLs |
| `git restore filename` | Discard unstaged file changes |

## 20. Hands-On Practice

Complete the following tasks:

1. Install Git on your laptop.
2. Configure your Git username and email.
3. Create a GitHub repository named `devops-practice`.
4. Create a local project folder.
5. Initialize the Git repository.
6. Create a `README.md` file.
7. Stage and commit the file.
8. Connect your local repository to GitHub.
9. Push the project to GitHub.
10. Create a feature branch.
11. Make another change and commit it.
12. Push the feature branch and open a pull request.

## 21. Interview Questions

1. What is Git?
2. What is GitHub?
3. What is the difference between Git and GitHub?
4. What is a repository?
5. What is the difference between `git add` and `git commit`?
6. What is the difference between `git commit` and `git push`?
7. What is the difference between `git fetch` and `git pull`?
8. What is branching in Git?
9. What is a pull request?
10. What is a merge conflict?
11. What is the purpose of `.gitignore`?
12. How are Git and GitHub used in DevOps CI/CD pipelines?

## 22. Official Documentation

- Git: https://git-scm.com/doc
- GitHub Docs: https://docs.github.com
- GitHub Hello World: https://docs.github.com/en/get-started/using-github/hello-world

# Git Introduction

Git is a distributed version control system (VCS) used to track changes in source code during software development. It helps developers collaborate, manage different versions of code, and roll back to previous states if needed.

Multiple developers can work together and merge changes easily.
Revert to previous versions whenever needed.
Develop features separately and merge them safely.
Each developer has a full copy of the repo.
Stores snapshots of the entire tree and optimizes storage internally using compression and delta encoding.
Core Concepts of Git
Before using Git, it is important to understand some of its core concepts. These concepts will help you get started and make it easier to work with Git in real-world scenarios.

1. Repositories
A repository (or repo) is a storage space where your project files and their history are kept. There are two types of repositories in Git:


Local Repository: A copy of the project on your local machine.
Remote Repository: A version of the project hosted on a server, often on platforms like GitHub, GitLab, or Bitbucket.
local_respository

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/9b2d86ec-2d15-443c-ac7f-4071f0a12e60" />

2. Commits
A commit is a snapshot of your project at a specific point in time. Each commit has a unique identifier (hash) and includes a message describing the changes made. Commits allow you to track and review the history of your project.

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/4d2d569d-01b9-40b5-bd32-218c7c852c47" />


3. Branches
Branches allow developers to work on separate tasks without affecting the main codebase. Common branch types include:

Main (or Master) Branch: The stable version of the project, usually production-ready.
Feature Branch: Used for developing new features or bug fixes.
git_branch
Branches

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/05757302-d75e-4863-b419-e57d93c62feb" />

4. Merging
Merging is the process of integrating changes from one branch into another. It allows you to combine the work done in different branches and resolve any conflicts that arise.

git_merging
Merging

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/83fd4119-b13c-47c0-822b-02f377bb5a3a" />

5. Cloning
Cloning a repository means creating a local copy of a remote repository. This copy includes all files, branches, and commit history.

GitClone0
Cloning
<img width="738" height="145" alt="image" src="https://github.com/user-attachments/assets/77bc37dd-ade4-4b50-be29-618692f7f4f6" />

6. Pull and Push
Git pull Fetches updates from the remote repository and integrates them into your local repository.
Git push Sends your local changes to the remote repository, making them available to others.
commit
Pull and Push

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/9e747213-7b28-4558-a6e7-652589414c71" />

The Three States (The Staging Area)
In Git, your files can be in one of three main states. Understanding this is key to understanding how Git works:

# Working Directory: This is your project folder with all the files you are currently working on. Any changes you make here are not yet tracked by Git.
# Staging Area (or Index): This is an intermediate area where you list the specific changes you want to include in your next "snapshot" or commit. You use the git add command to move changes from your working directory to the staging area.
# Repository (.git directory): This is where Git permanently stores the snapshots (commits) of your project. You use the git commit command to save the staged changes into the repository.
Git Workflow

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/7008dcc9-ceed-4720-8b9d-1d1be32034ab" />


# Git History
Git was created by Linus Torvalds in 2005 to manage the development of the Linux kernel.
It was designed to be fast, distributed, and reliable for managing large software projects.
Over time, Git became one of the most widely used version control systems in software development.
Today, it is commonly used with platforms like GitHub, GitLab, and Bitbucket for collaboration and code management.
For more details about the history and evolution of Git, you can refer here.

# Git Hosting
Git Hosting stores your Git repositories on a remote server, enabling collaboration, backup, pull requests, CI/CD, and even website hosting, while Git manages changes locally.

# GitHub
GitHub is a cloud-based Git hosting platform owned by Microsoft, popular for open-source projects and beginner developers. It provides a complete environment for version control, collaboration, and deployment.

Unlimited public and private repositories
Pull requests and code reviews for team collaboration
GitHub Pages for hosting static websites
Automation and CI/CD with GitHub Actions
# GitLab
GitLab is a complete DevOps platform offering Git repository hosting along with built-in CI/CD, issue tracking, and project management tools. It is ideal for teams and enterprises looking to automate workflows and manage code efficiently.

Public and private repositories
Built-in CI/CD pipelines for automation
Issue tracking and project management
Option for self-hosting for full control and privacy.
# Bitbucket
Bitbucket is a Git hosting platform by Atlassian, designed for private repositories and team collaboration. It is ideal for small teams or companies seeking a secure environment with tight integration to project management tools.

Private and public repositories
Bitbucket Pipelines for CI/CD automation
Integration with Jira and Trello
Secure and collaborative environment for teams.

---

**Conclusion**

Git helps us track and manage code changes, while GitHub allows us to host repositories and collaborate with others. Both are fundamental tools for modern software development and DevOps practices.
