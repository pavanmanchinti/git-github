1. Creating a Project Directory
Command
mkdir git-practice
cd git-practice/
ls -ltrh

Explanation

Creates a folder, moves into it, and lists all files in long format.

2. Checking Git Version
Command
git --version
git -v

Explanation

These commands display the installed Git version.

Sample Output

git version 2.42.0.windows.1

3. Initializing Git
Command
git init
ls -ltrha

Explanation

Initializes a new Git repository and shows hidden files including .git.

4. Creating Files
Commands
touch jenkins.txt
vi jenkins.txt
vi demo.txt
cat > dockerfile
cat > python.py

Explanation

Creates files and opens them for editing.
cat > file overwrites content until you press CTRL + D.

5. Checking File Status
Command
git status

Explanation

Shows which files are untracked, staged, or modified.

Sample Output

Untracked files:
  python.py
  jenkins.txt
  demo.txt

6. Adding Files to Staging Area
Commands
git add python.py
git add *.txt
git add .

Explanation
Command	Description
git add python.py	Adds only the file python.py
git add *.txt	Adds all .txt files
git add *	Adds all files in the directory except dotfiles
git add .	Adds all files including hidden files
7. Removing a File from Staging
Command
git reset demo.txt

Explanation

Moves demo.txt back to the working area (unstaged).

8. Restore a File
Command
git restore demo.txt

Explanation

Restores demo.txt to the last committed version.

9. Committing Changes
Commands
git commit -m "Add files from staging area to local repo"
git commit -am "feat: commit new changes"
git commit -am 'fix docker file'

Explanation

Saves your changes into the repository with a message.

10. Viewing Commit Logs
Commands
git log
git log -2
git log -n 2

Explanation

Shows commit history.

11. Viewing Changed Files in a Commit
Commands
git log --pretty="" --name-only
git show --pretty="" --name-only <commit-id>

Explanation

Shows filenames modified in commits.

Difference: Git Log vs Git Show
Git Log

Shows a list of commits.

Displays commit messages, authors, and timestamps.

Does NOT show changes by default.

Git Show

Shows the details of a single commit.

Displays diffs, file changes, insertions, and deletions.

Example

git show 94c30fefa5a19df2f7ab226905852f706b7b3dcb

Difference: git restore vs git checkout file
git restore

Modern command (recommended).

Restores file to last commit.

Does not switch branches.

git checkout file

Older command.

Can restore files.

Can also switch branches (confusing for beginners).

12. Adding Remote Repositories
Commands
git remote add origin https://github.com/pavanmanchinti/git-github.git
git remote -v

13. Pushing to Remote
Commands
git push origin master
git push jio master
git push jio dev
git push jio --all

Explanation

Uploads your local commits to GitHub.

14. Cleaning Untracked Files
git clean -n
git clean -f


-n = show what will be deleted (safe)

-f = force delete untracked files

15. Resetting Files
git reset deploy.yml
git reset jenkins.yml
git reset

16. Creating Branches
Commands
git branch
git branch dev
git checkout dev
git checkout -b stag
git checkout -b prod

17. Checking Differences Between Branches
git diff master dev
git diff --name-only master dev

18. Pushing a Branch
git push jio dev

19. Pulling Updates
git pull
git pull jio dev

MERGE CONFLICT PRACTICE
Step 1 — Edit same file in both branches
vi jenkins.txt
git commit -am "merge conflict"

Step 2 — Switch to other branch
git checkout dev
vi jenkins.txt
git commit -m "merge conflict"

Step 3 — Merge branches
git merge master


A conflict appears inside the file:

<<<<<<< HEAD
content from dev
=======
content from master
>>>>>>> master

Step 4 — Resolve it

Open file → remove conflict markers → keep correct content.

Step 5 — Commit merge
git commit -am "solve merge conflict"
git push jio dev

20. Deleting Branches
git branch -d prod
git branch -d stag

21. Renaming Branches
git branch -m dev development

22. Counting Branches
Local Branch Count
git branch | wc -l

Remote Branch Count
git branch -r | wc -l

23. Removing Remote Branch
git push jio :dev

24. Viewing Entire History
history
clear

Summary of Important Differences
Git Add . vs *
Command	Meaning
git add .	Adds all changes including hidden files (.env, .gitignore).
git add *	Adds all non-hidden files (skips dotfiles).
git add *.py	Adds all Python files only.
Git Log vs Git Show
Command	Purpose
git log	Shows commit history.
git show <commit>	Shows details and diffs of one commit.
Git Restore vs Git Checkout
Command	Purpose
git restore <file>	Restores file to last commit.
git checkout <branch>	Switches branches.
git checkout <file>	Restores file (old method).
