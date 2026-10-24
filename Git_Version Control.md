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

---

**Conclusion**

Git helps us track and manage code changes, while GitHub allows us to host repositories and collaborate with others. Both are fundamental tools for modern software development and DevOps practices.
