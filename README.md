# A02

_**GitHub/Git Tutorial**_

# Part 1: Using Git and GitHub

## Introduction 
- This tutorial explains how to use **Git** and **GitHub** together to create and manage a **Repository**, track changes, and share work.
  
- **Git** is the version control system that is used to track changes made to the files.
  
- **GitHub** is the platform that allows Git work to be stored in repositories where they can be managed.

### Step 1: Create a GitHub Account 

1. Go to https://github.com/.
2. Click Sign Up in the upper right corner and create an account.
3. Verify your email address and complete.
4. Sign in to GitHub. 

### Step 2: Install Git

1. Go to https://git-scm.com/install/
2. Download and install Git for your respective operating system.
3. Open Terminal or Git Bash.
4. Verify that Git was installed by typing:
   ```
   git --version
   ```
   
### Step 3: Configure Git

1. Enter your name and email address:
   ```
   git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   ```

### Step 4: Create a Repository on Github

1. Sign in to Github.
2. Look at the upper right corner of the screen for the **+** button.
4. Select **New repository**.
5. Enter the name of the **Repository**.
6. Choose whether the **Repository** should be public or private.
7. Click **Create repository**.

### Step 5: Copy the Repository URL 

1. Open the **Repository** you just created and named.
2. Near the top of the repository page, click the **Code** button.
3. Select **HTTPS**.
4. Click the copy button next to the **Repository** URL.

The URL will follow the general format:

```
https://github.com/username/repositoryname.git
```

### Step 6: Clone the Repository 

1. Open Terminal or Git Bash.
2. Navigate to the location where you want the project stored.
3. Type:

```
git clone https://github.com/username/repository-name.git
```

4. Enter the **Repository** folder:

```
cd repositoryname
```

**Clone** creates a local copy of the **Repository** from Github.

### Step 7: Check Your Repository

Check the current status of your files:

```
git status
```

Check the **Remote** connection:

```
git remote -v
```

### Step 8: Make Changes

1. Open the files in your local **Repository**.
2. Make your changes.
3. Save the files.
4. Return to Terminal or Git Bash.

Check your changes:

```
git status
```

### Step 9: Stage Your Changes

Use `git add` to prepare changes for a **Commit**.

To stage one file:

```
git add filename
```

To stage all changed files:

```
git add .
```

Check the status again:

```
git status
```

### Step 10: Create a Commit

Create a **Commit** with a clear message explaining what you changed.

```
git commit -m "Feature: updated project files"
```

Good **Commit** messages clearly describe the task, feature, or fix.

Examples:

```
Task: Create project files
Feature: added new functionality
Fix: corrected README instructions
```

### Step 11: Push Your Changes to Github

Use **Push** to send your local commits to the **Remote** repository on Github.

```
git push
```

After the **Push** finishes:

1. Return to the Github repository page.
2. Refresh the page.
3. Your changes should now appear in the online **Repository**.

### Step 12: Create a Branch

A **Branch** allows you to work on changes separately from the main branch.

Create a new **Branch**:

```
git switch -c feature-name
```

Check your current **Branch**:

```
git branch
```

The branch with an asterisk is your current branch.

### Step 13: Push a Branch to Github

After making and committing changes on your new **Branch**, use:

```
git push -u origin feature-name
```

The new **Branch** will now appear on Github.

You can view branches using the branch dropdown near the top of the repository file list.

### Step 14: Fetch Changes

Use **Fetch** to check for changes that exist on Github without automatically combining those changes with your current branch.

```
git fetch origin
```

### Step 15: Pull Changes

Use **Pull** to download changes from Github and integrate them into your current **Branch**.

```
git pull
```

A common workflow before starting new work is:

```
git pull
```

This helps make sure your local **Repository** is up to date.

### Step 16: Merge Branches

A **Merge** combines changes from one **Branch** into another.

First switch to the branch that will receive the changes:

```
git switch main
```

Then merge the other branch:

```
git merge feature-name
```

After the **Merge**, **Push** the changes to Github:

```
git push
```

### Step 17: Resolve a Merge Conflict

A **Merge Conflict** happens when Git cannot automatically combine changes from different branches.

If a **Merge Conflict** occurs:

1. Run the **Merge**.
2. Git will identify the files with conflicts.
3. Open the affected file.
4. Look for sections marked with conflict markers.
5. Keep the correct changes and remove the conflict markers.
6. Save the file.
7. Stage the resolved file:

```
git add filename
```

8. Create a **Commit**:

```
git commit -m "Fix: resolved merge conflict"
```

9. **Push** the resolved changes:

```
git push
```

### Basic Git and Github Workflow

The normal workflow is:

```
Github Repository
       
     Clone
       
Local Repository
       
   Make changes
       
      Status
       
       Add
       
     Commit
       
      Push
       
Github Repository
```

To get changes from Github:

```
Github
   
Fetch / Pull
   
Local Repository
```

To work separately on a feature:

```
Create Branch

Make changes
      
Add
      
Commit
      
Push
      
Github
```


# Part 2: Glossary

- **Branch** - A separate line of development that allows changes to be made independently.
- **Clone** - Creates a full copy of a remote repository, downloaded onto your local computer.
- **Commit** - A saved snapshot of the changes to a respository.
- **Fetch** - Downloads information about changes from a remote repository without automatically merging them.
-  **Git** — A version control system that is used to track changes made to the files.
- **Github** — the platform that allows Git work to be stored in repositories where they can be managed. 
- **Merge** — Combines changes from different branches.
- **Merge Conflict** — Refers to a situation where Git cannot automatically combine changes from different branches.
- **Push** — Sends local commits to a remote repository.
- **Pull** — Retrieves changes from a remote repository and integrates them into the current branch.
- **Remote** — A connection to a repository stored somewhere other than the local computer, such as Github.
- **Repository** — A project location containing files and the history of changes; can be tracked by Git.

# References

1. GitHub Docs. Creating a new repository.  
   https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository

2. GitHub Docs. Cloning a repository.  
   https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository

3. GitHub Docs. Set up Git.  
   https://docs.github.com/en/get-started/git-basics/set-up-git

4. Git Documentation.  
   https://git-scm.com/docs

5. Git Documentation. git-add.  
   https://git-scm.com/docs/git-add

6. Git Documentation. git-fetch.  
   https://git-scm.com/docs/git-fetch

7. Git Documentation. git-pull.  
   https://git-scm.com/docs/git-pull

8. Git Documentation. git-push.  
   https://git-scm.com/docs/git-push

9. Git Documentation. git-merge.  
   https://git-scm.com/docs/git-merge
