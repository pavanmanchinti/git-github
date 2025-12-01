📘 Git & GitHub Full Course – Complete Beginner to Advanced Guide
1. 📌 Introduction to Git & GitHub
What is Git?

Git is a distributed version control system used to track code changes and collaborate efficiently.

What is GitHub?

GitHub is a cloud-based hosting platform for Git repositories.

Features of GitHub

Source Code Management

Collaboration Tools

GitHub Actions

CI/CD

Pull Requests & Code Reviews

2. 🛠️ Install & Setup
Check Git Version
git --version
git -v

Set Username & Email
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

3. 📁 Creating Projects
Create a Directory
mkdir git-practice
cd git-practice

Initialize Git Repository
git init


This creates the hidden .git folder.

4. 🧱 Git Essentials
Basic Git Lifecycle
Working Directory → Staging Area → Local Repo → Remote Repo

Four File States in Git

Untracked

Modified

Staged

Committed

5. 📄 Creating & Managing Files
Create Files
touch file1.txt
vi demo.txt
cat > dockerfile

View Status
git status

6. 📌 Staging, Restoring & Committing
Add Files to Staging
Command	Explanation
git add file.py	Add one file
git add *.txt	Add all .txt files
git add *	Add all except hidden files
git add .	Add everything including hidden files
Remove from Staging
git reset filename

Restore File
git restore filename

Commit Changes
git commit -m "Meaningful commit message"
git commit -am "Quick commit for modified files"

7. 🔍 Viewing History & Logs
Basic Logs
git log
git log -2
git log --oneline

View Files Changed in a Commit
git show --pretty="" --name-only

8. 🌿 Branching & Switching
Create Branch
git branch dev

Switch Branch
git checkout dev

Create + Switch
git checkout -b staging

Rename Branch
git branch -m old new

9. ⚔️ Merge & Conflict Resolution
Merge Branch
git checkout master
git merge dev

Example Conflict
<<<<<<< HEAD
content from current branch
=======
content from merged branch
>>>>>>> branchname

Steps to Fix Conflict

Open file

Remove conflict markers

Keep correct content

Commit fix

git commit -am "resolved merge conflict"

10. 🌐 Remote Repositories
Add Remote
git remote add origin https://github.com/user/repo.git

Show Remotes
git remote -v

11. 🚀 Push, Pull & Fetch
Push Code
git push origin master
git push origin dev
git push origin --all

Pull Updates
git pull
git pull origin dev

Fetch Without Merge
git fetch

12. 🧹 Cleaning & Resetting
Clean Untracked Files
git clean -n
git clean -f

Reset Last Commit
git reset --soft HEAD~1
git reset --hard HEAD~1

13. ⏩ Useful Git Shortcuts
Command	Meaning
git log --oneline	Compact history
git add -p	Add chunks interactively
git diff --name-only	Only show filenames
git show HEAD	Show last commit
14. 🏆 Git Best Practices (DevOps Standards)

Commit frequently

Use meaningful commit messages

Never push to main/master directly

Enable branch protection

Use Pull Requests (PRs)

Merge only after review

Use .gitignore for sensitive files

Use feature branches

Perform periodic cleanup

15. ❓ Git Interview Questions (DevOps)

Difference between Git and GitHub?

Explain git fetch vs git pull.

What is a merge conflict?

Purpose of .gitignore?

Explain HEAD, staging area, working tree.

What is detached HEAD?

Rebase vs merge?

16. 🧾 Quick Git Cheat Sheet
git init
git clone <repo>
git status
git add .
git commit -m "message"
git push origin master
git pull
git branch
git checkout -b newbranch
git merge dev
git log --oneline
git diff
git reset
git restore
