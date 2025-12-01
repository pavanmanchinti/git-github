# 📘 Git & GitHub Setup Guide & Complete Developer Reference

## 🔹 What is Git?
Git is a distributed version control system that helps track source code changes and supports team collaboration.

## 🔹 What is GitHub?
GitHub is a cloud-based platform that provides distributed version control and source code management (SCM) using Git. It enables code collaboration, automation, and project management.

---

## 🧩 Popular Communication Tools
These tools are often used alongside GitHub:
- Microsoft Teams
- Slack
- Skype for Business
- Discord
- Google Chat

---

## 🗄️ Source Code Management (SCM) Tools
- Git
- GitHub
- GitLab
- Bitbucket
- Azure Repos

---

## ⚙️ Install & Setup Git
### Check Git Version
```
git --version
```

### Set Username & Email
```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 📁 Creating a Project & Initializing a Repository
### Create Directory
```
mkdir project-name
cd project-name
```
### Initialize Git
```
git init
```

---

## 🧱 Git File States (Important Lifecycle)
- Untracked
- Modified
- Staged
- Committed

---

## 📄 Creating & Managing Files (Working Directory Operations)
```
touch file1.txt
vi demo.txt
cat > dockerfile
```
### View Status
```
git status
```

---

## 📌 Staging, Restoring & Committing Changes
### Add Files
```
git add file.py
git add *.txt
git add .
```
### Remove from Staging
```
git reset filename
```
### Restore File
```
git restore filename
```
### Commit
```
git commit -m "Meaningful commit message"
git commit -am "Quick commit"
```

---

## 🔍 Viewing Git History & File Changes
```
git log
git log -2
git log --oneline
git show --pretty="" --name-only
```

---

## 🌿 Branching, Switching & Managing Versions
```
git branch dev
git checkout dev
git checkout -b staging
git branch -m old new
```

---

## ⚔️ Merging, Conflicts & Resolution Guide
### Merge
```
git checkout main
git merge dev
```
### Conflict Example
```
<<<<<<< HEAD
Your code
=======
Incoming code
>>>>>>> dev
```
### Resolve
- Remove conflict markers
- Keep correct content
- Save file
```
git commit -am "Resolved merge conflict"
```

---

## 🌐 Remote Repositories (GitHub Integration)
```
git remote add origin https://github.com/user/repo.git
git remote -v
```

---

## 🚀 Push, Pull & Fetch (Remote Operations)
```
git push origin main
git pull
git fetch
```

---

## 🧹 Cleaning, Undoing & Resetting Changes
```
git clean -n
git clean -f
git reset --soft HEAD~1
git reset --hard HEAD~1
```

---

## 🧾 Quick Git Cheat Sheet (Instant Reference)
```
git init
git clone <repo>
git status
git add .
git commit -m "message"
git push origin main
git pull
git branch
git checkout -b newbranch
git merge dev
git log --oneline
git diff
git reset
git restore
