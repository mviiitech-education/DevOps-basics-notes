# Git and GitHub Notes

## 1. Introduction to Git

- **Git** is a distributed version control system used for tracking changes in source code.
- Allows multiple developers to collaborate efficiently.

## 2. Basic Git Commands

### **Configuration**

```sh
# Set username and email
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### **Repository Setup**

```sh
# Clone an existing repository
git clone <repository_url>
```

### **Tracking Changes**

```sh
# Check the status of the repository
git status

# Add changes to the staging area
git add <file>
git add .  # Add all changes

# Commit changes with a message
git commit -m "Commit message"
```

### **Branching and Merging**

```sh
# List all branches
git branch
git branch -a

# Create a new branch
git branch <branch_name>

# Switch to a branch
git checkout <branch_name>
git switch <branch_name>  # Alternative command

# merge latest code from different branch
# Eg. get latest code from main branch to your branch
git pull origin main
```

### **Remote Repositories**

```sh
# Add a remote repository
git remote add origin <repository_url>

# Push changes to the remote repository
git push
git push origin <branch_name> # use when branch is not created in remote

# Pull changes from the remote repository
git pull
git pull origin <branch_name> # used when want to pull from other branches (or) use when branch is not created in remote
```

### **Undoing Changes**

```sh
# Undo the last commit but keep changes staged
git reset --soft HEAD~1

# Undo the last commit and unstage changes
git reset --mixed HEAD~1

# Discard all uncommitted changes
git checkout -- .
```

## 3. Introduction to GitHub

- **GitHub** is a cloud-based hosting service for Git repositories.
- Provides collaboration features like pull requests, issues, and project boards.

### **Working with GitHub**

```sh
# Forking a repository: Create a copy under your GitHub account.
# Create a pull request: Propose changes to a repository.
# GitHub Issues: Track bugs and enhancements.
```

### **GitHub Actions (CI/CD)**

- Automates workflows for testing, deployment, and integration.

### **GitHub Security Features**

- Two-factor authentication (2FA)
- Code scanning and dependency alerts

## 4. Best Practices

- Commit often with meaningful messages.
- Use branches for feature development.
  - eg:
    - `main` ( default ) [ production ]
    - `dev` [ development ]
    - `uat` [ user acceptance testing ]
    - `e2e` [ end to end ]
- Keep repositories clean and documented.

## 5. Conclusion

- Git and GitHub are essential tools for modern software development.
- Mastering version control improves collaboration and productivity.
