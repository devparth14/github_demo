# 📚 COMPLETE GIT & GITHUB REFERENCE GUIDE
### By devparth14 | Created: January 3, 2026

---

## 🎯 WHAT IS GIT & GITHUB?

**Git** = Version control software on your computer (tracks changes)  
**GitHub** = Online platform to store and share your code (like Google Drive for code)

---

## ⚙️ INITIAL SETUP (ONE-TIME ONLY)

### 1. Install Git
- Download from: https://git-scm.com/download/win
- Run installer with default settings
- Restart VS Code after installation

### 2. Configure Git (Set Your Identity)
```bash
git config --global user.name "devparth14"
git config --global user.email "dev.parth.m@gmail.com"
```

### 3. Verify Configuration
```bash
git config --global user.name
git config --global user.email
```

---

## 🚀 STARTING A NEW PROJECT

### Step 1: Initialize Repository
```bash
git init
```
**What it does:** Creates `.git` folder, turns folder into a Git repository

### Step 2: Check Status
```bash
git status
```
**What it does:** Shows which files are tracked, modified, or staged

### Step 3: Stage Files (Select files to save)
```bash
git add filename.html          # Add specific file
git add file1.html file2.css   # Add multiple files
git add .                      # Add ALL files in folder
```
**What it does:** Prepares files for commit (staging area)

### Step 4: Commit (Save Snapshot)
```bash
git commit -m "Your descriptive message here"
```
**What it does:** Saves a snapshot with a message describing changes

### Step 5: View History
```bash
git log                        # Full history
git log --oneline              # Compact view
```
**What it does:** Shows all commits with author, date, and messages

---

## 🌐 CONNECTING TO GITHUB

### Step 1: Create Repository on GitHub
1. Go to: https://github.com/new
2. Enter repository name (e.g., `github_demo`)
3. Keep it Public
4. DO NOT add README (if you already have files)
5. Click "Create repository"

### Step 2: Connect Local Repo to GitHub
```bash
git remote add origin https://github.com/devparth14/github_demo.git
```
**What it does:** Links your local folder to GitHub repository

### Step 3: Rename Branch (Optional but Recommended)
```bash
git branch -M main
```
**What it does:** Renames default branch from "master" to "main"

### Step 4: Push to GitHub (Upload Code)
```bash
git push -u origin main
```
**What it does:** Uploads your commits to GitHub  
**-u flag:** Remembers the connection (next time just use `git push`)

---

## 📝 DAILY WORKFLOW

After making changes to your files:

```bash
# 1. Check what changed
git status

# 2. Stage your changes
git add .

# 3. Commit with message
git commit -m "Describe what you changed"

# 4. Push to GitHub
git push
```

---

## 🔍 USEFUL COMMANDS

### Check Remote URL
```bash
git remote -v
```

### View Differences (What Changed?)
```bash
git diff                       # Changes not staged
git diff --staged              # Changes staged for commit
```

### Undo Staging (Before Commit)
```bash
git reset filename.html        # Unstage specific file
git reset                      # Unstage all files
```

### View Commit Details
```bash
git show                       # Show last commit
git show a2f15c1               # Show specific commit
```

### Create .gitignore File
Create a file named `.gitignore` to exclude files from Git:
```
node_modules/
.env
.DS_Store
.history/
*.log
```

---

## 🌿 BRANCHING (ADVANCED)

### Create New Branch
```bash
git branch feature-name        # Create branch
git checkout feature-name      # Switch to branch
# OR combine both:
git checkout -b feature-name   # Create and switch
```

### List Branches
```bash
git branch                     # Local branches
git branch -a                  # All branches (including remote)
```

### Merge Branch
```bash
git checkout main              # Switch to main
git merge feature-name         # Merge feature into main
```

### Delete Branch
```bash
git branch -d feature-name     # Delete local branch
```

---

## 🆘 COMMON PROBLEMS & SOLUTIONS

### Problem: "Git is not recognized"
**Solution:** Install Git and restart VS Code

### Problem: "Permission denied (publickey)"
**Solution:** Use HTTPS URL instead of SSH, or set up SSH keys

### Problem: Committed wrong files
**Solution (before push):**
```bash
git reset --soft HEAD~1        # Undo last commit, keep changes
```

### Problem: Want to undo last commit completely
```bash
git reset --hard HEAD~1        # WARNING: Deletes changes!
```

### Problem: Forgot to add file to commit
```bash
git add forgotten-file.html
git commit --amend --no-edit
```

---

## 📊 OUR PROJECT HISTORY

### Commit 1 - Initial Setup
```
Date: January 3, 2026
Files: index.html, style.css
Message: "Initial commit: Added homepage with HTML and CSS"
```

---

## 🎓 KEY CONCEPTS

### Working Directory
Your actual project files on your computer

### Staging Area (Index)
Files ready to be committed (after `git add`)

### Repository (Local)
Your commit history stored in `.git` folder

### Remote Repository
Your code on GitHub (after `git push`)

### Commit
A snapshot of your project at a specific time

### Branch
A separate version of your code (parallel development)

### HEAD
Pointer to your current commit/branch location

---

## 🔗 IMPORTANT LINKS

- GitHub Repository: https://github.com/devparth14/github_demo
- Git Documentation: https://git-scm.com/doc
- GitHub Guides: https://guides.github.com

---

## 💡 BEST PRACTICES

1. **Commit Often** - Small, frequent commits are better than large ones
2. **Write Clear Messages** - Describe WHAT and WHY you changed
3. **Test Before Commit** - Make sure your code works
4. **Use .gitignore** - Don't commit unnecessary files
5. **Pull Before Push** - Always get latest changes first: `git pull`
6. **Review Changes** - Use `git status` and `git diff` before committing

---

## ✅ COMMIT MESSAGE EXAMPLES

```bash
git commit -m "Added contact form to homepage"
git commit -m "Fixed navigation menu bug"
git commit -m "Updated README with installation steps"
git commit -m "Removed unused CSS styles"
git commit -m "Initial project setup"
```

---

## 🎯 QUICK REFERENCE CARD

| Command | Purpose |
|---------|---------|
| `git init` | Start new repository |
| `git status` | Check current state |
| `git add .` | Stage all changes |
| `git commit -m "msg"` | Save snapshot |
| `git push` | Upload to GitHub |
| `git pull` | Download from GitHub |
| `git log` | View history |
| `git diff` | See changes |
| `git branch` | List branches |
| `git checkout` | Switch branches |

---

**📌 Remember:** Practice makes perfect! The more you use Git, the more natural it becomes.

**🚀 Keep Learning:** Git has many advanced features - explore them as you grow!

---

*This reference guide is for personal use by devparth14*  
*Last Updated: January 3, 2026*
