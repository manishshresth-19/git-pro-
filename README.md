# Git Cheat Sheet 🚀

A **practical, enterprise-ready Git cheat sheet** you can directly add to any `README.md` or documentation.

---

## 🔹 Git Setup
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

---

## 🔹 Repository Basics
```bash
git init                 # Initialize repo
git clone <repo-url>     # Clone repository
git status               # Check repo status
```

---

## 🔹 Staging & Committing
```bash
git add file.txt         # Stage a file
git add .                # Stage all changes
git commit -m "message"  # Commit changes
git commit --amend       # Edit last commit
```

### Conventional Commit Example
```bash
git commit -m "feat(auth): add Google login"
```

---

## 🔹 Branching
```bash
git branch               # List branches
git branch new-branch    # Create branch
git checkout branch      # Switch branch
git switch branch        # Modern switch
git checkout -b branch   # Create + switch
```

### Rename Branch
```bash
git branch -m old new
```

---

## 🔹 Remote Repositories
```bash
git remote -v            # Show remotes
git fetch --all          # Fetch all branches
git pull                 # Fetch + merge
git push origin branch   # Push branch
```

---

## 🔹 Fixing & Undoing

### Undo last commit (keep changes)
```bash
git reset --soft HEAD~1
```

### Undo last commit (delete changes ⚠️)
```bash
git reset --hard HEAD~1
```

### Safe undo after push
```bash
git revert HEAD
```

---

## 🔹 Working with Files

### Restore file
```bash
git restore file.txt
```

### Get file from another branch
```bash
git checkout develop -- file.txt
```

### File history
```bash
git log -- file.txt
```

---

## 🔹 Viewing History (Changelog)
```bash
git log
git log --oneline
git log --graph --all --decorate
```

### Between versions
```bash
git log v1.0.0..v1.1.0
```

---

## 🔹 Merging & Rebasing

### Merge
```bash
git merge branch-name
```

### Rebase
```bash
git rebase main
```

---

## 🔹 Stash (Temporary Save)
```bash
git stash
git stash list
git stash pop
```

---

## 🔹 Tags (Releases)
```bash
git tag v1.0.0
git tag
git push origin v1.0.0
```

---

## 🔹 Git Flow Branch Naming
```text
main           → production
develop        → integration
feature/login  → new feature
bugfix/ui-fix  → bug fix
release/1.0.0  → release prep
hotfix/crash   → production fix
```

---

## 🔹 Best Practices ✅
- Use **Conventional Commits**
- Never work directly on `main`
- Use `git fetch --all` regularly
- Use `git revert` on shared branches
- Keep commits small and meaningful

---

## 🔹 One-Line Survival Commands
```bash
git status
git add .
git commit -m "fix: bug"
git pull
git push
```

---

📌 **Tip**: This cheat sheet is suitable for **students, teams, and enterprise projects**.

