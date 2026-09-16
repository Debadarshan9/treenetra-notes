# Date: 8-Sept-2026

### **VCS**

&rarr; It is known as `Version control system`.

&rarr; It is a system used to track changes in files and maintain different versions of a project.

&rarr; It helps us

1. Track to change a file
2. See what changes were made
3. When changes were made
4. Restore an older version
5. Manage multiple versions of a project

### **VCS Types**

### **LVCS**

&rarr; It is known as `Local Version Control System`.

&rarr; In LVCS different versions of files are maintained in `local computer` itself.

### **Limitation**

The history is mainly available on our local machine, so collaboration and sharing are limited.

### **CVCS**

&rarr; It is knows ans `Centralized Version Control System`.

&rarr; In CVCS the project repository and version history are maintained on `one central server`.

### **Limitation**

If the central server is unavailable developers may not be able to perform many version control operations.

### **DVCS**

&rarr; It is known as `Distributed Version Control System`.

&rarr; In DVCS every developer generally has a `local copy of the repository`, including its history.

### **Git**

&rarr; It is a DVCS used to track changes, source code or files.

&rarr; It allows us

1. Track changes
2. Create branches
3. Commit changes
4. Merge changes
5. Work with remote repo

### **Github**

&rarr; It is a cloud based platoform for hosting git repositories and collaborating with other developers.

We can use github

1. Store our git repository online
2. Colloborate with team members
3. Review code
4. Create pull requests

**_NOTe: git = DVCS tool and Github = Online platform that host git repositories_**

### **Git Repository**

A git repository(repo) is a project folder that git used to track and manage versions of files.

### **Local Repo and Remote Repo**

&rarr; It is the git repo stored in our own computer.

&rarr; It is the git repo stored on a remote server or platform such as github.

| Local Repo                         | Remote Repo                       |
| ---------------------------------- | --------------------------------- |
| Stored on our computer             | Stored on a remote server         |
| We work with is directly           | Used for sharing or collaboration |
| `git commit` saves changes locally | `git push` uploads commits        |
| Can work `without internet`        | Usually accessed `over a network` |
| created with `git init`            | can be hosted on github           |

# Date: 9-Sept-2026

**`git init`** &rarr; It creates a hidden .git directory to track changes and version.

**`git add filename`** &rarr; Stages a specific file, so it can be included in the next commit.

**`git add .`** &rarr; Stages all new and modified file in the current directory and its sub directories.

**`git status`** &rarr; It shows the current status of the git repository including untracked, modified and staged files.

**`git rm --cached filename`** &rarr; It is used to untrack the track file.

**`git checkout -b branchName` or `git switch -c branchName`** &rarr; It is used to create and switch to a new branch.

**`git commit -m "message"`** &rarr; It is used to save changes.

# Date: 10-Sept-2026

### **What is PR**

&rarr; It is known as pull request

&rarr; It is a request to merge the changes from one branch to another branch

### **Why do we use PR**

&rarr; Code review before merging

&rarr; Team members can check the changes

&rarr; Discuss or request modifications

&rarr; Maintain code quality

### **What is merge conflict**

A merge conflict happens when git finds that 2 branches have made different changes to the same part of a file and git can't automatically decide which change should be kept

# Date: 11-Sept-2026

### **What is git merge**

It combine the changes from one branch to another branch

```
git merge feature
```

**`git rebase`** &rarr; It moves your branch commits, so they are based on the latest commit of another branch.

**`git cherry-pick`** &rarr; It copies a specific commit from another branch into current branch.

**`git log --oneline`** &rarr; It displays the git commit history in one line format.

**`git stash`** &rarr; It temporarily stores our uncommited changes, so we can work on a clean working directory without commiting those changes.

**`git stash pop`** &rarr; It brings our changes back which are in stash container

**`git pull`** &rarr; It is used to get the latest changes from a remote repository and update our current local branch

**`git clone`** &rarr; It is used to copy a remote git repository to our local computer

### **How to resolve merge conflict**
