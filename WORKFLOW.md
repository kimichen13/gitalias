# Git Workflow Guide

A comprehensive guide for daily Git operations using our custom aliases.

---

## 📋 Quick Reference

Most frequently used commands:
```bash
git get     # Update your branch (fetch + pull + update submodules)
git ss      # Quick status check
git aa      # Stage all changes
git cm      # Commit with message
git push1   # Push to remote
```

---

## 🌅 Daily Workflow

### 1. Starting Your Day

Always begin with:
```bash
git get     # Sync your repository with remote
```

### 2. Feature Development

#### A. Starting New Work

For Jira tasks:
```bash
git jira feature PROJ-123 add-login-page
# Creates: feature/PROJ-123-add-login-page
```

For general features:
```bash
git topic-begin feature/add-dark-mode
```

#### B. During Development

Monitor your changes:
```bash
git ss          # Quick status
git d           # Review changes
```

Save your work:
```bash
# Regular commits
git aa && git cm    # Stage and commit

# Quick saves
git wip            # Save as Work-In-Progress
git snapshot       # Stash while keeping changes
```

Stay in sync:
```bash
git get           # Pull updates
git push1         # Push your changes
```

---

## 🔍 Code Review Process

### 1. Pre-PR Checklist

```bash
# Update your branch
git get
git jira-rebase   # For Jira branches

# Review changes
git ss            # Check status
git d             # Review diff
git lg            # Check commit history

# Quality checks
git bvv          # Check branch status
git ll           # Review commit details

# Final verification
git lo           # Check for WIP commits
git pushy        # Safe force-push if needed
```

### 2. Review Guidelines

✅ **Quality Checklist:**
- [ ] No WIP commits remain
- [ ] Commit messages follow conventions
- [ ] All changes are intentional
- [ ] No untracked files left behind
- [ ] Branch is up to date with base

---

## 🚨 Handling Interruptions

### Urgent Bug Fix Process

1. **Save Current Work:**
```bash
git wip              # Save as WIP
# OR
git snapshot         # Flexible stash
```

2. **Switch Context:**
```bash
git current-branch   # Note your position
git o $(git default-branch)
git get             # Update base
```

3. **Fix Bug:**
```bash
# Create bug branch
git jira hotfix BUG-123 fix-login-crash
# OR
git topic-begin hotfix/fix-login-crash

# Fix and publish
git aa && git cm    # Stage and commit
git push1          # Push changes
git topic-end      # Complete fix
```

4. **Resume Feature Work:**
```bash
git o <original-branch>   # Return to feature
git get                  # Get latest changes
git unwip               # Restore WIP (if used)
```

---

## 🔄 Common Operations

### Undo Changes
```bash
git unadd         # Unstage changes
git uncommit      # Undo last commit
git reset-commit  # Soft reset commit
```

### Emergency Backup
```bash
git panic         # Create backup tarball
git snapshot      # Quick save changes
```

### Status Checks
```bash
git bv            # Branch details
git who           # Contributor stats
git lg            # Commit graph
```

---

## ✨ Best Practices

1. 🔄 **Stay Updated**
   - Start each day with `git get`
   - Sync frequently with base branch

2. 📝 **Clean Commits**
   - Write clear commit messages
   - Make small, focused changes
   - Follow commit message format

3. 🛡️ **Work Protection**
   - Use `git wip` for work in progress
   - Create `git snapshot` before risky changes
   - Regular pushes with `git push1`

4. 🌿 **Branch Management**
   - Use proper branch naming
   - Clean up after completing work
   - Keep history clean and logical

---

## 📝 Commit Message Format

```
<type>(<scope>): <description>

Examples:
feat(auth): add password reset functionality
fix(ui): resolve button alignment issues
docs(api): update endpoint documentation
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting
- `refactor`: Code restructuring
- `test`: Adding tests
- `chore`: Maintenance

---

## 🆘 Need Help?

```bash
git aliases    # List all available commands
```

For more details, check the original [GitAlias](https://github.com/GitAlias/gitalias) project.
