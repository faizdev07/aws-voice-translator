# GitHub Repository Setup - Step by Step Guide

This guide provides detailed instructions for creating a GitHub repository for your AWS Voice Translator project, including all necessary Git commands.

## Prerequisites

1. Install Git on your computer if not already installed
   - Windows: Download from https://git-scm.com/download/win
   - Mac: `brew install git`
   - Linux: `sudo apt-get install git`

2. Create a GitHub account if you don't have one at https://github.com/

## Step 1: Create a New Repository on GitHub

1. Log in to your GitHub account
2. Click the "+" icon in the top right corner, then select "New repository"
3. Enter repository details:
   - Repository name: `aws-voice-translator`
   - Description: "Real-time voice translation web application built with AWS AI services"
   - Visibility: Public
   - Initialize with a README: No (we'll push our own)
   - Add .gitignore: No (we'll create our own)
   - Choose a license: No (we'll add our own)
4. Click "Create repository"

## Step 2: Prepare Your Local Project

1. Open Command Prompt or Terminal
2. Navigate to your project folder:
   ```bash
   cd "c:\D Drive\VSCode\Voice Translator\aws-voice-translator"
   ```

3. Create necessary folders if they don't exist:
   ```bash
   mkdir -p screenshots frontend backend
   ```

4. Copy your files to the appropriate folders:
   - Copy HTML, CSS, JS files to the frontend folder
   - Copy Lambda function to the backend folder
   - Save screenshots to the screenshots folder

## Step 3: Initialize Git Repository

1. Initialize a new Git repository:
   ```bash
   git init
   ```

2. Create a .gitignore file:
   ```bash
   echo "# Ignore OS files" > .gitignore
   echo ".DS_Store" >> .gitignore
   echo "Thumbs.db" >> .gitignore
   echo "# Ignore environment files" >> .gitignore
   echo ".env" >> .gitignore
   echo "# Ignore node modules" >> .gitignore
   echo "node_modules/" >> .gitignore
   ```

## Step 4: Add and Commit Files

1. Add all files to staging:
   ```bash
   git add .
   ```

2. Commit the files:
   ```bash
   git commit -m "Initial commit: AWS Voice Translator project"
   ```

## Step 5: Connect to GitHub and Push

1. Connect your local repository to GitHub:
   ```bash
   git remote add origin https://github.com/faizdev07/aws-voice-translator.git
   ```

2. Push your code to GitHub:
   ```bash
   git push -u origin main
   ```
   
   Note: If your default branch is "master" instead of "main", use:
   ```bash
   git push -u origin master
   ```

3. Enter your GitHub username and password when prompted
   - Note: If you have 2FA enabled, you'll need to use a personal access token instead of your password

## Step 6: Verify Repository

1. Go to `https://github.com/faizdev07/aws-voice-translator`
2. Verify that all your files have been uploaded correctly
3. Check that screenshots are displaying properly in the README

## Step 7: Update Repository Settings (Optional)

1. Click on "Settings" in your repository
2. Scroll down to "GitHub Pages"
3. Select "main" branch as source
4. Click "Save"
5. Your project will be available at `https://faizdev07.github.io/aws-voice-translator/`

## Common Issues and Solutions

### Authentication Failed
If you see "Authentication failed", create a personal access token:
1. Go to GitHub → Settings → Developer settings → Personal access tokens
2. Generate a new token with "repo" permissions
3. Use this token instead of your password

### Push Rejected
If your push is rejected with "failed to push some refs":
```bash
git pull --rebase origin main
git push origin main
```

### Large Files
If you have files over 100MB:
1. Add them to .gitignore
2. Consider using Git LFS for large files

## Final Steps

1. Share your repository link on LinkedIn using the template in PUBLISHING.md
2. Respond to any issues or pull requests that come in
3. Keep your repository updated with any future changes to your project