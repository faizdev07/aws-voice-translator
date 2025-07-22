# Git Commands Cheat Sheet for AWS Voice Translator Project

## Basic Setup Commands

```bash
# Navigate to project directory
cd "c:\D Drive\VSCode\Voice Translator\aws-voice-translator"

# Initialize git repository
git init

# Check status of your files
git status
```

## Adding and Committing Files

```bash
# Add all files to staging
git add .

# Add specific files
git add README.md
git add screenshots/home-screen.png

# Commit your changes
git commit -m "Initial commit: AWS Voice Translator project"
```

## Connecting to GitHub

```bash
# Connect to your GitHub repository
git remote add origin https://github.com/faizdev07/aws-voice-translator.git

# Verify remote connection
git remote -v
```

## Pushing to GitHub

```bash
# Push to main branch (first time)
git push -u origin main

# If your default branch is master
git push -u origin master

# Subsequent pushes
git push
```

## Handling Errors

```bash
# If push is rejected
git pull --rebase origin main
git push origin main

# If you need to force push (use with caution)
git push -f origin main
```

## Checking Repository Status

```bash
# View commit history
git log

# View changes before committing
git diff

# Check current branch
git branch
```

## Creating and Managing Branches

```bash
# Create a new branch
git checkout -b feature/new-language-support

# Switch between branches
git checkout main

# Merge changes from another branch
git merge feature/new-language-support
```

## Updating Your Repository

```bash
# Get latest changes from GitHub
git pull

# Update specific branch
git pull origin main
```

## Quick Setup (All Commands)

```bash
# Complete setup in one go
cd "c:\D Drive\VSCode\Voice Translator\aws-voice-translator"
git init
git add .
git commit -m "Initial commit: AWS Voice Translator project"
git remote add origin https://github.com/faizdev07/aws-voice-translator.git
git push -u origin main
```