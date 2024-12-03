
---

# **Git Quick Reference Guide**

## **Basic Setup**
1. **Check Git Version:**  
   ```bash
   git --version
   ```
   Confirms the installed Git version.

2. **Set Global User Details:**  
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
   These details are added to every commit you make.

---

## **Repository Basics**
1. **Initialize a New Repository:**  
   ```bash
   git init
   ```
   Creates a new Git repository in the current directory.

2. **Clone an Existing Repository:**  
   ```bash
   git clone <repository-url>
   ```
   Downloads a remote repository to your local machine.

3. **Check Repository Status:**  
   ```bash
   git status
   ```
   Displays the state of your working directory and staging area.

4. **Stage Changes for Commit:**  
   ```bash
   git add <filename>       # Stages a specific file  
   git add .                # Stages all files in the current directory
   ```

5. **Commit Staged Changes:**  
   ```bash
   git commit -m "Meaningful commit message"
   ```

6. **View Differences Before Committing:**  
   ```bash
   git diff
   ```
   Shows changes made in the working directory compared to the staging area.

---

## **Lifecycle of Changes**
1. **Clone a Repository:**  
   ```bash
   git clone <repository-url>
   ```
   Downloads the repository to your system.
   
2. **Make Changes in Files:** Edit files in your working directory.
   
3. **Stage Changes:**  
   ```bash
   git add <filename>
   ```
   Prepares the changes for the next commit.

4. **Commit Changes:**  
   ```bash
   git commit -m "Descriptive message about changes"
   ```

---

## **Viewing Repository History**
1. **Show Commit Logs:**  
   ```bash
   git log
   ```
   Displays the commit history with details like commit ID, author, and date.

2. **Filter Logs:**  
   ```bash
   git log -3            # Shows the last 3 commits  
   git log --oneline     # Shows a summary of commits (one-line format)  
   git log --stat        # Lists files modified in each commit  
   git log -p            # Shows detailed differences in commits  
   ```

3. **Inspect a Specific Commit:**  
   ```bash
   git show <commit-id>
   ```
   Displays details of a specific commit, including changes made.

---

## **Branching, Tagging, and Merging**
### **Branching**
1. **View Branches:**  
   ```bash
   git branch
   ```
   Displays a list of branches; the current branch is highlighted.

2. **Create a New Branch:**  
   ```bash
   git branch <branch-name>
   ```
   Creates a new branch from the current branch.

3. **Switch to a Branch:**  
   ```bash
   git checkout <branch-name>
   ```

4. **Create and Switch to a New Branch:**  
   ```bash
   git checkout -b <branch-name>
   ```

### **Committing and Merging**
1. **Add and Commit in a Single Command:**  
   ```bash
   git commit -am "Commit message"
   ```

2. **Merge Branch into Current Branch:**  
   ```bash
   git merge <branch-name>
   ```

3. **Resolve Merge Conflicts:**  
   - Fix conflicts manually by editing files.
   - Stage the resolved files, then commit.  
     OR  
   - Abort the merge process:  
     ```bash
     git merge --abort
     ```

4. **Delete a Branch:**  
   ```bash
   git branch -d <branch-name>
   ```

### **Tagging**
1. **Create a Tag:**  
   ```bash
   git tag -a <tag-name> <commit-id> -m "Tag description"
   ```

2. **Delete a Tag:**  
   ```bash
   git tag -d <tag-name>
   ```

### **Stashing**
1. **Stash Uncommitted Changes:**  
   ```bash
   git stash
   ```
   Temporarily saves changes and cleans the working directory.

2. **View Stashed Changes:**  
   ```bash
   git stash list
   ```

3. **Apply Stashed Changes:**  
   ```bash
   git stash apply
   ```

---

## **Undoing Changes**
1. **Amend the Last Commit:**  
   ```bash
   git commit --amend
   ```
   Updates the last commit with new changes.

2. **Revert a Commit:**  
   ```bash
   git revert <commit-id>
   ```
   Creates a new commit that undoes changes from a specific commit.

3. **Reset to a Previous Commit:**  
   ```bash
   git reset [--soft | --mixed | --hard] <commit-id>
   ```
   - **--soft:** Keeps changes staged for commit.  
   - **--mixed:** Keeps changes in the working directory but unstages them.  
   - **--hard:** Discards all local changes.

---

## **Special Commands**
1. **Ignore Files:**  
   - Create a `.gitignore` file to exclude files and directories from being tracked.
   - Example `.gitignore` entry:  
     ```
     *.log
     /node_modules/
     secret.txt
     ```

2. **Restore a File to the Last Commit:**  
   ```bash
   git restore <filename>
   ```
   Reverts the file to its last committed state.

---


### **Pushing a Commit to GitHub**

1. **Setup Git (Local):**
   ```bash
   git config --global user.name "hitesh7424"
   git config --global user.email "hitesh164722@gmail.com"
   ```

2. **Prepare Repository:**
   - **On GitHub:** Create an empty repository (no README or `.gitignore`).
   - **On Local:**  
     ```bash
     git init               # Initialize local repo
     git add .              # Stage all files
     git commit -m "Initial commit"  # Commit changes
     git remote add origin <repository-url>  # Link GitHub repo
     ```

3. **Push to GitHub:**
   ```bash
   git push -u origin master
   ```
   - Enter your **GitHub username**: `hitesh7424`
   - Enter your **Personal Access Token (PAT)** as the password.

4. **PAT Setup (if needed):**
   - Go to GitHub **Settings > Developer Settings > Personal Access Tokens**.
   - Generate a new token with `repo` scope and use it instead of your GitHub password.

5. **Verify Push:**  
   Check your GitHub repository for the uploaded files and commit. 

--- 
**Tip:** Use `git remote -v` to verify the remote URL if you encounter issues.
