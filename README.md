\# TASK 4: Version-Controlled DevOps Project with Git



\## 1. Project Title



\*\*Build a Version-Controlled DevOps Project with Git\*\*



\---



\## 2. Objective



The objective of this task is to manage a DevOps project using Git and GitHub version-control best practices.



This project demonstrates:



\* Git repository initialization

\* GitHub repository management

\* Branching

\* Feature development

\* Pull Requests

\* Merging

\* Git commits

\* `.gitignore`

\* Git tags

\* Git stash

\* Markdown documentation

\* Git workflow



\---



\## 3. Tools Used



\* Git

\* GitHub

\* PowerShell

\* Markdown



\---



\# 4. Project Structure



```text

task-4-git-devops-project/

│

├── app/

│   └── app.txt

│

├── screenshots/

│   ├── 01-repository.png

│   ├── 02-branches.png

│   ├── 03-feature-to-dev-pr.png

│   ├── 04-dev-to-main-pr.png

│   └── 05-tag.png

│

├── .gitignore

└── README.md

```



\---



\# 5. Git Branching Strategy



This project uses three branches:



```text

feature

&#x20;  ↓

&#x20; dev

&#x20;  ↓

&#x20;main

```



\### main



The `main` branch contains the stable version of the project.



\### dev



The `dev` branch is used for development and integration before changes are moved to `main`.



\### feature



The `feature` branch is used to develop a particular feature or change without directly modifying the stable branch.



\---



\# 6. Step-by-Step Implementation



\## Step 1: Create the Project Folder



Create a project folder:



```powershell

cd C:\\Users\\ittth

mkdir task-4-git-devops-project

cd task-4-git-devops-project

```



\### Why?



A separate project folder keeps all files related to this DevOps task organized in one location.



\---



\# Step 2: Create the Application Folder



```powershell

mkdir app

"Task 4 DevOps Git Project" | Out-File app\\app.txt

```



\### Why?



The task is mainly about Git and GitHub. A simple project file gives Git some project content to track and version.



\---



\# Step 3: Initialize Git



```powershell

git init

```



Check the repository:



```powershell

git status

```



\### Why?



`git init` converts the normal project directory into a Git repository.



Git creates a hidden `.git` directory that stores Git's version-control information.



\---



\# Step 4: Configure Git Username and Email



```powershell

git config --global user.name "Your Name"

git config --global user.email "your-email@example.com"

```



Check the configuration:



```powershell

git config --global --list

```



\### Why?



Git records the author of every commit. The username and email identify who created the commit.



\---



\# Step 5: Create .gitignore



Create a `.gitignore` file and add:



```text

.env

\*.log

node\_modules/

.vscode/

.idea/

.DS\_Store

```



\### Why?



`.gitignore` tells Git which files should not be tracked.



For example, `.env` files may contain passwords, API keys, or other sensitive information.



`node\_modules/` contains installed dependencies and normally should not be committed.



`.gitignore` helps prevent unnecessary or sensitive files from being pushed to GitHub.



\---



\# Step 6: Create the README



This README documents the complete project, including the objective, tools, Git commands, workflow, branches, Pull Requests, `.gitignore`, tags, stash, and interview questions.



\### Why?



A README explains the project to anyone who visits the GitHub repository.



\---



\# Step 7: Check Git Status



```powershell

git status

```



\### Why?



`git status` shows:



\* Current branch

\* Modified files

\* Untracked files

\* Staged files

\* Changes ready for commit



It is one of the most commonly used Git commands.



\---



\# Step 8: Stage the Files



```powershell

git add .

```



Then:



```powershell

git status

```



\### Why?



`git add` moves changes from the working directory into the Git staging area.



The basic Git process is:



```text

Working Directory

&#x20;      ↓

&#x20;   git add

&#x20;      ↓

Staging Area

&#x20;      ↓

&#x20; git commit

&#x20;      ↓

Git Repository

```



\---



\# Step 9: Create the First Commit



```powershell

git commit -m "Initial project setup"

```



Check the commit:



```powershell

git log --oneline

```



\### Why?



A commit creates a saved snapshot/version of the project.



The commit message explains what was changed.



\---



\# Step 10: Rename the Main Branch



```powershell

git branch -M main

```



Check:



```powershell

git branch

```



Expected:



```text

\* main

```



\### Why?



`main` is used as the stable branch of the project.



\---



\# Step 11: Create the GitHub Repository



Create a new GitHub repository named:



```text

task-4-git-devops-project

```



Do not create another README, `.gitignore`, or license on GitHub because these files are already created locally.



\---



\# Step 12: Connect the Local Repository to GitHub



Use the GitHub repository URL:



```powershell

git remote add origin https://github.com/YOUR\_USERNAME/task-4-git-devops-project.git

```



Check:



```powershell

git remote -v

```



\### Why?



The `origin` remote connects the local Git repository to the GitHub repository.



\---



\# Step 13: Push Main to GitHub



```powershell

git push -u origin main

```



\### Why?



`git push` uploads local commits and branches to GitHub.



The `-u` option sets the upstream relationship between the local and remote branch.



\---



\# Step 14: Create the Development Branch



```powershell

git switch -c dev

```



Check:



```powershell

git branch

```



Push it:



```powershell

git push -u origin dev

```



\### Why?



The `dev` branch is used for development and integration before changes are released to `main`.



\---



\# Step 15: Create the Feature Branch



From `dev`:



```powershell

git switch -c feature

```



Check:



```powershell

git branch

```



Push:



```powershell

git push -u origin feature

```



\### Why?



A feature branch isolates feature development from the stable branch.



This allows developers to work without directly changing `main`.



\---



\# Step 16: Make a Change in the Feature Branch



Open:



```powershell

notepad app\\app.txt

```



Add:



```text

Task 4 DevOps Git Project



Feature branch development completed.



Git and GitHub version control workflow demonstrated.

```



Save the file.



Check:



```powershell

git status

```



\### Why?



This demonstrates how a developer makes a change inside a feature branch.



\---



\# Step 17: Commit the Feature Change



```powershell

git add app/app.txt

git commit -m "Add feature branch documentation"

```



Check:



```powershell

git log --oneline

```



Push:



```powershell

git push

```



\### Why?



The change is saved as a separate commit and uploaded to the feature branch on GitHub.



\---



\# Step 18: Create a Pull Request from Feature to Dev



On GitHub:



```text

base: dev

compare: feature

```



Create the Pull Request.



Suggested title:



```text

Add feature branch changes

```



Suggested description:



```text

This pull request adds the changes developed in the feature branch.



Changes:

\- Updated project file

\- Demonstrated feature branch workflow

\- Prepared changes for dev branch

```



\### Why?



A Pull Request allows changes to be reviewed before they are merged into another branch.



Workflow:



```text

feature

&#x20;  ↓

Pull Request

&#x20;  ↓

dev

```



\---



\# Step 19: Merge Feature into Dev



After reviewing the Pull Request:



1\. Click \*\*Merge pull request\*\*

2\. Click \*\*Confirm merge\*\*



The feature changes are now part of `dev`.



\### Why?



The feature has been reviewed and integrated into the development branch.



\---



\# Step 20: Update the Local Dev Branch



```powershell

git switch dev

git pull origin dev

```



\### Why?



The merge happened on GitHub, so `git pull` downloads the latest `dev` changes to the local computer.



\---



\# Step 21: Create Pull Request from Dev to Main



On GitHub create another Pull Request:



```text

base: main

compare: dev

```



Suggested title:



```text

Release project to main

```



Suggested description:



```text

This pull request promotes the tested development changes into the main branch.



The project contains:

\- Git workflow

\- Branching

\- Feature development

\- Pull Request workflow

\- Documentation

\- .gitignore

```



\### Why?



This demonstrates promotion of development changes into the stable `main` branch.



Workflow:



```text

feature

&#x20;  ↓

dev

&#x20;  ↓

main

```



\---



\# Step 22: Merge Dev into Main



On GitHub:



1\. Review the Pull Request

2\. Click \*\*Merge pull request\*\*

3\. Click \*\*Confirm merge\*\*



\### Why?



The development version is now promoted to the stable `main` branch.



\---



\# Step 23: Update Local Main



```powershell

git switch main

git pull origin main

```



Check history:



```powershell

git log --oneline --graph --all

```



\### Why?



This downloads the latest version of `main` and allows us to view the complete branch and commit history.



\---



\# Step 24: Create a Git Tag



Create version `v1.0.0`:



```powershell

git tag -a v1.0.0 -m "Task 4 version 1.0.0"

```



Check:



```powershell

git tag

```



Push:



```powershell

git push origin v1.0.0

```



\### Why?



A Git tag identifies an important version of the project.



For example:



```text

v1.0.0

```



can represent the first completed version of the project.



\---



\# Step 25: Verify the Tag on GitHub



Go to GitHub:



```text

Code → Tags

```



Verify:



```text

v1.0.0

```



\### Why?



This provides evidence that the project has a version tag.



\---



\# Step 26: Demonstrate Git Stash



Modify:



```powershell

notepad app\\app.txt

```



Add a temporary change:



```text

Temporary change for stash demonstration.

```



Save.



Check:



```powershell

git status

```



Temporarily store the change:



```powershell

git stash

```



Check:



```powershell

git status

```



View the stash:



```powershell

git stash list

```



Restore the change:



```powershell

git stash pop

```



\### Why?



`git stash` temporarily stores uncommitted changes.



It is useful when you are working on one task but need to temporarily switch to another task.



Example:



```text

Working on Feature A

&#x20;      ↓

Urgent work arrives

&#x20;      ↓

git stash

&#x20;      ↓

Work on another task

&#x20;      ↓

Return to Feature A

&#x20;      ↓

git stash pop

```



\---



\# Step 27: Test .gitignore



Create a temporary log file:



```powershell

"test log" | Out-File test.log

```



Check:



```powershell

git status

```



Because `.gitignore` contains:



```text

\*.log

```



Git should not show `test.log` as an untracked file.



Delete the test file:



```powershell

Remove-Item test.log

```



\### Why?



This verifies that `.gitignore` is working correctly.



\---



\# 28. Important Git Commands and Their Purpose



| Command                   | Purpose                                |

| ------------------------- | -------------------------------------- |

| `git init`                | Initializes a Git repository           |

| `git status`              | Shows repository status                |

| `git add .`               | Stages all changes                     |

| `git add <file>`          | Stages a specific file                 |

| `git commit -m "message"` | Saves changes as a commit              |

| `git log`                 | Shows commit history                   |

| `git log --oneline`       | Shows compact commit history           |

| `git branch`              | Lists branches                         |

| `git switch -c dev`       | Creates and switches to a branch       |

| `git switch main`         | Switches to main                       |

| `git push`                | Uploads changes to GitHub              |

| `git pull`                | Downloads latest changes               |

| `git remote -v`           | Shows remote repositories              |

| `git merge`               | Combines branch changes                |

| `git tag`                 | Lists or creates tags                  |

| `git stash`               | Temporarily stores uncommitted changes |

| `git stash pop`           | Restores stashed changes               |



\---



\# 29. Git Working Areas



Git can be understood using three main areas:



```text

Working Directory

&#x20;      │

&#x20;      │ git add

&#x20;      ↓

Staging Area

&#x20;      │

&#x20;      │ git commit

&#x20;      ↓

Local Git Repository

&#x20;      │

&#x20;      │ git push

&#x20;      ↓

GitHub Remote Repository

```



\### Working Directory



The files you are currently working on.



\### Staging Area



Files selected for the next commit.



\### Local Repository



Commits stored on your computer.



\### Remote Repository



The Git repository stored on GitHub.



\---



\# 30. Complete Git Workflow Used in This Task



```text

Create Project

&#x20;     ↓

git init

&#x20;     ↓

Create Files

&#x20;     ↓

git add

&#x20;     ↓

git commit

&#x20;     ↓

Push to GitHub

&#x20;     ↓

Create dev branch

&#x20;     ↓

Create feature branch

&#x20;     ↓

Develop Feature

&#x20;     ↓

Commit Changes

&#x20;     ↓

Push Feature

&#x20;     ↓

Pull Request

&#x20;     ↓

feature → dev

&#x20;     ↓

Testing / Review

&#x20;     ↓

Pull Request

&#x20;     ↓

dev → main

&#x20;     ↓

Release

&#x20;     ↓

Create v1.0.0 Tag

```



\---



\# 31. Screenshots



The following screenshots should be included in the repository to demonstrate the completed task:



\### Screenshot 1 — GitHub Repository



Shows:



\* Repository name

\* README.md

\* `.gitignore`

\* Project files



\### Screenshot 2 — Branches



Shows:



```text

main

dev

feature

```



\### Screenshot 3 — Feature to Dev Pull Request



Shows:



```text

feature → dev

```



\### Screenshot 4 — Dev to Main Pull Request



Shows:



```text

dev → main

```



\### Screenshot 5 — Git Tag



Shows:



```text

v1.0.0

```



\---



\# 32. Final Verification Commands



Check the current status:



```powershell

git status

```



Expected:



```text

nothing to commit, working tree clean

```



Check branches:



```powershell

git branch -a

```



Expected branches:



```text

main

dev

feature

```



Check tags:



```powershell

git tag

```



Expected:



```text

v1.0.0

```



Check commit history:



```powershell

git log --oneline --graph --all

```



\---



\# 33. Git vs GitHub



\## Git



Git is a distributed version-control system.



It runs on the local computer and tracks changes in files.



\## GitHub



GitHub is a cloud platform for hosting Git repositories and collaborating with other developers.



Git and GitHub are different:



```text

Git = Version Control Tool



GitHub = Remote Repository + Collaboration Platform

```



\---



\# 34. Interview Questions and Answers



\## 1. What is Git?



Git is a distributed version-control system used to track changes in source code and manage different versions of a project.



\---



\## 2. What is the difference between merge and rebase?



\### Merge



Merge combines the histories of two branches and can create a merge commit.



Example:



```text

feature

&#x20;  ↓

&#x20; merge

&#x20;  ↓

&#x20;dev

```



\### Rebase



Rebase moves or replays commits onto another base commit and can create a more linear history.



\---



\## 3. What is a Pull Request?



A Pull Request is a request to merge changes from one branch into another branch.



In this project:



```text

feature → dev

dev → main

```



Pull Requests allow changes to be reviewed before merging.



\---



\## 4. How do you resolve merge conflicts?



First check the status:



```powershell

git status

```



Open the conflicted file and identify conflict markers:



```text

<<<<<<<

Your changes

=======

Other changes

>>>>>>>

```



Choose or combine the correct changes.



Then:



```powershell

git add .

git commit -m "Resolve merge conflict"

```



The exact final command can differ depending on whether the conflict occurred during a merge or rebase.



\---



\## 5. What are Git tags?



Git tags are named references used to identify specific commits.



Example:



```text

v1.0.0

```



They are commonly used to mark releases or important project versions.



\---



\## 6. What is Git workflow?



Git workflow is the process used to manage changes using Git.



The workflow used in this project is:



```text

feature

&#x20;  ↓

Pull Request

&#x20;  ↓

dev

&#x20;  ↓

Pull Request

&#x20;  ↓

main

```



\---



\## 7. Explain git stash.



`git stash` temporarily stores uncommitted changes.



It is useful when you need to temporarily change branches or work on another task without committing incomplete changes.



To restore the changes:



```powershell

git stash pop

```



\---



\## 8. What is the use of .gitignore?



`.gitignore` specifies files and directories that Git should not track.



Examples:



```text

.env

\*.log

node\_modules/

```



It helps prevent sensitive, temporary, generated, or unnecessary files from being committed.



\---



\# 35. Final Project Outcome



This project demonstrates a basic version-control workflow using Git and GitHub.



The following concepts were implemented:



\* Git repository initialization

\* GitHub repository

\* Git commits

\* `main` branch

\* `dev` branch

\* `feature` branch

\* Feature development

\* Pull Requests

\* Branch merging

\* `.gitignore`

\* Git tags

\* Git stash

\* Markdown documentation

\* Git workflow

\* Screenshots

\* Version `v1.0.0`



The final workflow is:



```text

&#x20;                GitHub

&#x20;                   │

&#x20;                 main

&#x20;                   ↑

&#x20;              Pull Request

&#x20;                   ↑

&#x20;                  dev

&#x20;                   ↑

&#x20;              Pull Request

&#x20;                   ↑

&#x20;               feature

```



\---



\# 36. Conclusion



The Task 4 project demonstrates how Git and GitHub can be used to manage a DevOps project using version-control best practices.



The project uses branches to isolate development, commits to maintain project history, Pull Requests for controlled merging, `.gitignore` to prevent unwanted files from being tracked, tags to identify versions, and Markdown documentation to describe the work.



The completed project demonstrates the fundamental Git workflow required for a DevOps environment.



\---



\# 37. Task Completion Checklist



\*  Git repository initialized

\*  GitHub repository created

\*  `main` branch created

\*  `dev` branch created

\*  `feature` branch created

\*  Project files added

\*  Git commits created

\*  Feature branch developed

\*  Feature → dev Pull Request

\*  Dev → main Pull Request

\*  Pull Requests merged

\*  README.md created

\*  .gitignore created

\*  Git tag `v1.0.0` created

\*  Git stash demonstrated

\*  Markdown documentation included

\*  Screenshots included

\*  Project pushed to GitHub



\---



\## Final GitHub Repository



\*\*Repository:\*\* `task-4-git-devops-project`



\*\*GitHub URL:\*\* Add your actual GitHub repository link here after creating the repository.



\*\*Submission:\*\* Submit the GitHub repository link according to the internship task submission instructions.



