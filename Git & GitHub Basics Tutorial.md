This guide covers the most essential Git commands you’ll need to start working with Git and GitHub:  
- **Clone**: Copy a repository from GitHub to your local machine.  
- **Commit**: Save changes in your local repository.  
- **Push**: Upload your changes to GitHub.  
- **Pull**: Download changes from GitHub to your local repository.  

---

## 1. Setup Git (First Time Only)

Before using Git, configure your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

Check configuration:

```bash
git config --list
```

---

## 2. Clone a Repository

Cloning means making a local copy of a remote repository from GitHub.

```bash
git clone https://github.com/username/repository.git
```

- **`username`**: Your GitHub username.
- **`repository`**: The name of the repository.

This will create a folder with the same name as the repository.

---

## 3. Make Changes & Stage Them

Navigate to your cloned repository:

```bash
cd repository
```

Check status of your files:

```bash
git status
```

Add files to the **staging area**:

```bash
git add file.txt
```

Add **all files**:

```bash
git add .
```

---

## 4. Commit Changes

A commit records your staged changes:

```bash
git commit -m "Your commit message"
```

Example:

```bash
git commit -m "Added new feature for login system"
```

---

## 5. Push Changes to GitHub

Push your commits to the **remote repository**:

```bash
git push origin main
```

- **`origin`**: Default name for the remote repository.
- **`main`**: Branch name (could also be `master` or another branch).

---

## 6. Pull Changes from GitHub

If someone else has updated the repository, pull their changes:

```bash
git pull origin main
```

---

## 7. Common Workflow

```bash
# Step 1: Get latest version
git pull origin main

# Step 2: Make changes

# Step 3: Stage changes
git add .

# Step 4: Commit changes
git commit -m "Describe your changes"

# Step 5: Push changes to GitHub
git push origin main
```

---

## 8. Useful Commands

- Check commit history:

```bash
git log
```

- Show changes before staging:

```bash
git diff
```

- Show changes already staged:

```bash
git diff --cached
```

- Create a new branch:

```bash
git checkout -b branch-name
```

- Switch to another branch:

```bash
git checkout branch-name
```

---

## Quick Summary

| Action | Command Example |
|--------|----------------|
| Clone repo | `git clone URL` |
| Stage changes | `git add .` |
| Commit changes | `git commit -m "message"` |
| Push changes | `git push origin main` |
| Pull changes | `git pull origin main` |
| Check status | `git status` |
| View history | `git log` |

---

✅ **Tip:** Always pull before you start working, and commit + push after making changes. This avoids conflicts and keeps your code synced.

