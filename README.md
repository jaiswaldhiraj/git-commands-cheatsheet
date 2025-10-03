# 📌 Git Commands Cheat Sheet

A quick reference guide for the most commonly used Git commands.

---

## ⚙️ Configure Name and Email
Set the identity of the user making commits.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## 🆕 Git Init
Initialize a new Git repository in your project.

```bash
git init
```

---

## ➕ Git Add (Staging Files)
Add files to the staging area.

```bash
git add <file_name>   # Add a single file
git add .             # Add all files
```

---

## 📋 Git Status
Check the current state of the repository.

```bash
git status         # Show status of files
git status -s      # Short format (M = modified, A = added, ?? = untracked)
```

---

## 💾 Git Commit
Save staged changes to the local repository.

```bash
git commit -m "Commit message"                  # Commit staged changes
git commit -m "Title" -m "Detailed description" # Commit with subject & body
git commit -a -m "Commit message"               # Commit tracked files without 'git add'
```

---

## 🔄 Git Checkout (Undo Changes / Switch Branches)
Discard changes or switch branches.

```bash
git checkout <file_name>    # Undo changes in a file
git checkout -f             # Undo all changes
git checkout <branch_name>  # Switch to another branch
```

---

## 📜 Git Log (View History)
View commit history.

```bash
git log                       # Full commit history
git log --oneline             # Compact view
git log -p -<n>               # Show last <n> commits with diffs
```

---

## 🆚 Git Diff (Compare Changes)
Compare changes in files.

```bash
git diff             # Show changes not staged
git diff --staged    # Show changes between staging area and last commit
```

---

## 🗑️ Git Remove
Remove files from repository or staging.

```bash
git rm --cached <file>   # Remove from staging area only
git rm <file>            # Remove from working directory and staging
```

---

## 🚫 Git Ignore
Ignore specific files or directories.

```bash
touch .gitignore   # Create .gitignore file
```
Inside `.gitignore`, list files/folders to ignore (e.g., `node_modules/`, `*.log`).

---

## 🌿 Git Branch
Work with multiple branches.

```bash
git branch <branch_name>       # Create a new branch
git checkout <branch_name>     # Switch to branch
git checkout -b <branch_name>  # Create and switch in one step
git branch                     # List all branches
git merge <branch_name>        # Merge branch into current branch
```

---

## 🔗 Git Remote
Link your local repo with a remote repository.

```bash
git remote add origin <url>   # Add remote repository
git remote -v                 # Show remotes
```

---

## 📥 Git Clone
Clone a remote repository.

```bash
git clone <url>
```

---

## 📤 Git Push
Upload local commits to remote repository.

```bash
git push origin <branch_name>    # Push branch to remote
git push -u origin <branch_name> # Push and set upstream branch
```

---

## 📥 Git Pull & Fetch
Download changes from remote repository.

```bash
git pull         # Fetch and merge changes from remote
git fetch        # Fetch changes (does not merge)
git merge        # Merge fetched changes
```

---

## 🔄 Git Reset (Undo Commits)
Undo commits in history.

```bash
git reset --soft HEAD~1   # Undo last commit but keep changes staged
git reset --mixed HEAD~1  # Undo last commit and unstage changes
git reset --hard HEAD~1   # Undo last commit and discard changes
```

---

## 🧹 Git Clean
Remove untracked files/directories.

```bash
git clean -f    # Remove untracked files
git clean -fd   # Remove untracked files and directories
```

---

## 🏷️ Git Tag
Mark a specific commit as important (like versioning).

```bash
git tag v1.0                  # Create lightweight tag
git tag -a v1.0 -m "Version"  # Create annotated tag
git push origin v1.0          # Push tag to remote
```

---

# ⚡ Advanced Git Commands

## 📦 Git Stash
Save uncommitted changes temporarily.

```bash
git stash          # Stash current changes
git stash list     # List stashes
git stash apply    # Apply last stash
git stash pop      # Apply and remove last stash
```

---

## 🔀 Git Rebase
Reapply commits on top of another branch.

```bash
git rebase <branch>      # Rebase current branch onto <branch>
git rebase -i HEAD~3     # Interactive rebase last 3 commits
```

---

## 🎯 Git Cherry-pick
Apply a specific commit from another branch.

```bash
git cherry-pick <commit_hash>
```

---

## ⏪ Git Reflog
Show history of all actions (useful for recovery).

```bash
git reflog
```

---

## 🔎 Git Blame
See who modified each line of a file.

```bash
git blame <file>
```

---

## 🔍 Git Show
Show details of a commit.

```bash
git show <commit_hash>
```

---

# ✅ Quick Workflow Example

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <repo_url>
git push -u origin main
```

---

# 📖 Notes
- **Staging Area** = Temporary storage for changes before commit.
- **Commit** = Save snapshot in local Git repository.
- **Remote** = Online repo (like GitHub, GitLab, Bitbucket).
