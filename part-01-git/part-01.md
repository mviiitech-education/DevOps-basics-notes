# Git and GitHub Notes

## 1. Introduction to Git
Git is a distributed version control system (VCS) that helps developers track changes in their code, collaborate with teams, and manage project versions efficiently.

### **Key Features of Git:**
- Distributed system: Every developer has a complete copy of the repository.
- Branching and Merging: Create branches to work on features separately and merge them later.
- Lightweight and Fast: Efficient storage and processing of data.
- Supports non-linear development.
- Strong security: Uses SHA-1 hashing to ensure data integrity.

## 2. Installing and Configuring Git
### **Installation:**
- **Windows:** Download from [git-scm.com](https://git-scm.com/) and install.
- **Mac:** Install using Homebrew: `brew install git`
- **Linux:** Install using package manager:
  - Debian/Ubuntu: `sudo apt install git`
  - Fedora: `sudo dnf install git`
  - Arch: `sudo pacman -S git`

### **Basic Configuration:**
```sh
# Set user name and email
$ git config --global user.name "Your Name"
$ git config --global user.email "your.email@example.com"

# Check configuration
$ git config --list
```

## 3. Git Basics
### **Initializing a Repository**
```sh
$ git init
```
This creates a `.git` directory, which stores all version control data.

### **Cloning a Repository**
```sh
$ git clone <repository-url>
```
Downloads an existing repository and its history.

### **Staging and Committing Changes**
```sh
$ git add <file>    # Stage a specific file
$ git add .         # Stage all changes
$ git commit -m "Commit message"  # Commit changes
```

### **Checking Repository Status**
```sh
$ git status
```
Shows modified, staged, and untracked files.

### **Viewing Commit History**
```sh
$ git log
```
Lists all past commits with details.

## 4. Branching and Merging
### **Creating and Switching Branches**
```sh
$ git branch feature-branch  # Create a new branch
$ git checkout feature-branch  # Switch to the new branch
# Or use:
$ git switch feature-branch
```

### **Merging Branches**
```sh
$ git checkout main
$ git merge feature-branch
```

### **Deleting a Branch**
```sh
$ git branch -d feature-branch
```

## 5. Working with Remote Repositories
### **Adding a Remote Repository**
```sh
$ git remote add origin <repository-url>
```

### **Pushing Changes**
```sh
$ git push origin main
```
Uploads committed changes to a remote repository.

### **Pulling Changes**
```sh
$ git pull origin main
```
Fetches and merges changes from a remote repository.

### **Fetching Changes Without Merging**
```sh
$ git fetch origin
```
Retrieves updates but does not merge them automatically.

## 6. GitHub Basics
GitHub is a cloud-based platform for hosting Git repositories with additional collaboration features.

### **Creating a Repository on GitHub**
1. Log in to GitHub.
2. Click **New Repository**.
3. Choose a name and initialize with a README (optional).
4. Click **Create Repository**.

### **Connecting Local Repository to GitHub**
```sh
$ git remote add origin <repository-url>
$ git push -u origin main
```

### **Forking a Repository**
- Forking creates a copy of someone else’s repository under your GitHub account.
- Used for contributing to open-source projects.

### **Pull Requests (PRs)**
1. Make changes in a forked repository.
2. Push changes to a new branch.
3. Navigate to GitHub and click **New Pull Request**.
4. Provide a description and submit for review.

### **Managing Issues**
- Issues help track bugs, feature requests, and tasks.
- Create issues with titles, descriptions, and labels.
- Assign issues to team members.

## 7. Advanced Git Features
### **Rebasing**
```sh
$ git rebase main
```
Moves the current branch’s commits on top of another branch’s commits.

### **Cherry-Picking**
```sh
$ git cherry-pick <commit-hash>
```
Applies a specific commit from one branch to another.

### **Stashing Changes**
```sh
$ git stash  # Save changes without committing
$ git stash pop  # Apply saved changes
```
Useful when switching branches without committing changes.

### **Git Tags**
```sh
$ git tag v1.0  # Create a tag
$ git push origin v1.0  # Push the tag to remote
```
Tags are used for marking versions.

## 8. Best Practices for Git and GitHub
- Write meaningful commit messages.
- Keep commits small and focused.
- Use `.gitignore` to avoid tracking unnecessary files.
- Regularly pull from remote repositories to stay updated.
- Use feature branches for new development.
- Review and test changes before merging.

## 9. Troubleshooting Common Issues
### **Undo Last Commit**
```sh
$ git reset --soft HEAD~1  # Undo commit but keep changes
$ git reset --hard HEAD~1  # Undo commit and discard changes
```

### **Fixing Merge Conflicts**
1. Open conflicting file(s).
2. Resolve conflicts manually.
3. Use `git add` to stage fixed files.
4. Commit the resolved changes.

### **Recovering Deleted Branch**

$ git reflog  # Find the branch reference
$ git checkout -b branch-name <commit-hash>


## 10. Conclusion
Git and GitHub are powerful tools for version control and collaboration. Mastering them enables developers to efficiently manage code, collaborate in teams, and contribute to open-source projects.

