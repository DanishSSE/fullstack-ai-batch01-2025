# GitHub Basics Guide

## What is Git and GitHub?

- **Git**: A version control system that tracks changes in your code
- **GitHub**: A cloud platform for hosting Git repositories and collaborating with others

## Initial Setup

### Install Git

#### Windows
1. Download from [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Run installer (use default settings)
3. Verify installation: `git --version`

#### macOS
```bash
# Using Homebrew
brew install git

# Or download from https://git-scm.com/download/mac
```

#### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install git
```

### Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Verify configuration
git config --list
```

### Create GitHub Account
1. Go to [https://github.com](https://github.com)
2. Click "Sign up"
3. Complete registration

### Setup SSH Keys (Recommended)

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Start SSH agent
eval "$(ssh-agent -s)"

# Add key to agent
ssh-add ~/.ssh/id_ed25519

# Copy public key (Windows)
cat ~/.ssh/id_ed25519.pub | clip

# Copy public key (macOS)
pbcopy < ~/.ssh/id_ed25519.pub

# Copy public key (Linux)
cat ~/.ssh/id_ed25519.pub
```

Add the copied key to GitHub:
1. GitHub Settings > SSH and GPG keys
2. Click "New SSH key"
3. Paste your key and save

## Basic Git Workflow

### Creating a Repository

#### On GitHub
1. Click "+" icon > "New repository"
2. Name your repository
3. Add description (optional)
4. Choose public or private
5. Initialize with README (optional)
6. Click "Create repository"

#### Locally
```bash
# Navigate to your project folder
cd your-project

# Initialize Git repository
git init

# Add files
git add .

# Make first commit
git commit -m "Initial commit"

# Connect to GitHub
git remote add origin https://github.com/yourusername/your-repo.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### The Basic Git Cycle

```bash
# 1. Check status
git status

# 2. Add changes
git add filename.txt          # Add specific file
git add .                     # Add all files

# 3. Commit changes
git commit -m "Descriptive message about changes"

# 4. Push to GitHub
git push origin main
```

### Pulling Changes

```bash
# Get latest changes from GitHub
git pull origin main
```

## Common Git Commands

### Repository Status
```bash
git status              # Check current status
git log                 # View commit history
git log --oneline       # Compact commit history
```

### Branching
```bash
git branch              # List branches
git branch feature-name # Create new branch
git checkout feature-name   # Switch to branch
git checkout -b feature-name  # Create and switch

# Modern way (Git 2.23+)
git switch feature-name     # Switch to branch
git switch -c feature-name  # Create and switch
```

### Merging
```bash
# Switch to main branch
git checkout main

# Merge feature branch
git merge feature-name

# Delete merged branch
git branch -d feature-name
```

### Undoing Changes
```bash
# Discard changes in working directory
git checkout -- filename.txt

# Unstage file
git reset HEAD filename.txt

# Undo last commit (keep changes)
git reset --soft HEAD~1

# Undo last commit (discard changes)
git reset --hard HEAD~1
```

### Viewing Changes
```bash
git diff                # Show unstaged changes
git diff --staged       # Show staged changes
git diff branch-name    # Compare with another branch
```

## Cloning Repositories

```bash
# Clone via HTTPS
git clone https://github.com/username/repo-name.git

# Clone via SSH
git clone git@github.com:username/repo-name.git

# Clone into specific folder
git clone https://github.com/username/repo-name.git my-folder
```

## .gitignore File

Create a `.gitignore` file to exclude files from Git:

```gitignore
# Dependencies
node_modules/

# Environment variables
.env

# Build outputs
dist/
build/

# IDE files
.vscode/
.idea/

# OS files
.DS_Store
Thumbs.db
```

## Commit Message Best Practices

### Format
```
Type: Brief summary (50 chars or less)

More detailed explanation if needed (wrap at 72 chars)
```

### Types
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `style:` Code formatting
- `refactor:` Code restructuring
- `test:` Adding tests
- `chore:` Maintenance tasks

### Examples
```bash
git commit -m "feat: Add user authentication"
git commit -m "fix: Resolve login button bug"
git commit -m "docs: Update README installation steps"
```

## Collaboration Workflow

### Fork and Pull Request
1. Fork repository on GitHub
2. Clone your fork locally
3. Create a feature branch
4. Make changes and commit
5. Push to your fork
6. Create Pull Request on GitHub

### Pull Request Process
```bash
# Create feature branch
git checkout -b feature/amazing-feature

# Make changes and commit
git add .
git commit -m "feat: Add amazing feature"

# Push to your fork
git push origin feature/amazing-feature

# Go to GitHub and create Pull Request
```

## Resolving Merge Conflicts

When conflicts occur:

1. Git marks conflicts in files:
```
<<<<<<< HEAD
Your changes
=======
Conflicting changes
>>>>>>> branch-name
```

2. Edit the file to resolve
3. Remove conflict markers
4. Add and commit:
```bash
git add conflicted-file.txt
git commit -m "fix: Resolve merge conflict"
```

## Useful GitHub Features

### Issues
- Track bugs and feature requests
- Reference in commits: `Fixes #123`

### Projects
- Kanban-style project management
- Organize issues and PRs

### Actions
- Automate workflows (CI/CD)
- Run tests on push/PR

### Wiki
- Project documentation
- Collaborative knowledge base

## Common Troubleshooting

### Authentication Failed
```bash
# Update remote URL to SSH
git remote set-url origin git@github.com:username/repo.git
```

### Forgot to Pull Before Push
```bash
git pull --rebase origin main
git push origin main
```

### Committed to Wrong Branch
```bash
# Save changes
git stash

# Switch to correct branch
git checkout correct-branch

# Apply changes
git stash pop
```

## Git Aliases (Optional)

Add to `~/.gitconfig`:
```ini
[alias]
    st = status
    co = checkout
    br = branch
    ci = commit
    lg = log --oneline --graph --all
    last = log -1 HEAD
```

Usage:
```bash
git st      # Instead of git status
git co main # Instead of git checkout main
```

## Resources

- [Official Git Documentation](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com)
- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Interactive Git Tutorial](https://learngitbranching.js.org/)
- [Oh My Git! (Game)](https://ohmygit.org/)

## Quick Reference

| Command | Description |
|---------|-------------|
| `git init` | Initialize repository |
| `git clone <url>` | Clone repository |
| `git status` | Check status |
| `git add <file>` | Stage changes |
| `git commit -m "msg"` | Commit changes |
| `git push` | Push to remote |
| `git pull` | Pull from remote |
| `git branch` | List branches |
| `git checkout <branch>` | Switch branch |
| `git merge <branch>` | Merge branch |
| `git log` | View history |

---

*Last updated: January 2025*
