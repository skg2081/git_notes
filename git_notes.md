**********************
GIT CHEAT SHEET
**********************
======
Basic Git Commands
======================
======
Configuration
-------------
Set user name:
git config --global user.name "Your Name"

Set user email:
git config --global user.email "your.email@example.com"

Repository Initialization
-------------------------
Initialize a new Git repository(this runs one time in a project):
git init  

Using gitignore
----------------------
Create .gitignore file 
win: echo. > .gitignore
lin: touch > .gitignore

Just add the file or folder name in .gitignore file to untrack.

Cloning
-------
Clone an existing repository:
git clone <repository_url>

Staging and Committing
----------------------
Check the status of your working directory:
git status

Add a file to the staging area:
git add <file>

Add all files to the staging area:
git add .

Commit staged changes:
git commit -m "Commit message"

Branching and Merging
---------------------
List all branches:
git branch

Create a new branch:
git branch <branch_name>

Switch to a branch:
git checkout <branch_name>

Create and switch to a new branch:
git checkout -b <branch_name>

Merge a branch into the current branch(you should be on the branch in which you want to merge the "branch_name"):
git merge <branch_name>

Going on some previous commit:
git checkout SHA_Value_of_commit

Returning at master after above:
git checkout master

Remote Repositories
-------------------
Add a remote repository:
git remote add <remote_name> <remote_url>

List remote repositories:
git remote -v

Fetch changes from a remote repository:
git fetch <remote_name>

Push changes to a remote repository:
git push <remote_name> <branch_name>

Pull changes from a remote repository:
git pull <remote_name> <branch_name>

Viewing History
---------------
Show commit history:
git log

Show a summarized commit history:
git log --oneline

Show changes in each commit:
git log -p

Add vs code as default editor in Git:
git config --global core.editor "code --wait"

Undoing Changes
---------------
Unstage a file:
git reset <file>

Revert changes in the working directory:
git checkout -- <file>

Amend the last commit:
git commit --amend -m "New commit message"

Stashing
--------
Stash changes:
git stash

Apply stashed changes:
git stash apply

List stashed changes:
git stash list

Use a stash and dropping at the same point(unstashing stash@{0}):
git stash pop stash@{0}

Stash changes(stashing the untracked files nad add a message):
git stash save -u "message"

Tags
----
Create a new tag:
git tag <tag_name>

Push tags to remote repository:
git push <remote_name> --tags

Git Ignore
----------
Create a `.gitignore` file:
# Example .gitignore content
*.log
*.tmp
node_modules/

======================
Example Workflow
======================
1. Initialize a repository:
   git init

2. Clone a repository:
   git clone <repository_url>

3. Create a new branch:
   git checkout -b feature_branch

4. Make changes and stage them:
   git add .

5. Commit changes:
   git commit -m "Add new feature"

6. Push changes to the remote repository:
   git push origin feature_branch

7. Create a pull request on GitHub/GitLab/Bitbucket.

8. Merge the pull request (usually done on the platform's web interface).

9. Pull the latest changes:
   git pull origin main

10. Delete the feature branch locally and remotely:
    git branch -d feature_branch
    git push origin --delete feature_branch