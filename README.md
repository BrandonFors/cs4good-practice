# cs4good-practice

### Step 1: Getting the Latest Code (`git pull`)

Before you start any new work, you need to make sure your local version of the project is up-to-date with the remote repository (GitHub).

```bash
# Switch to the branch you want to update (e.g., main or a parent branch)
git checkout main

# Pull the latest changes from the remote repository
git pull origin main
```

### Step 2: Save Your Work

```bash
# Stage your files for the commit. The "." adds all changed files.
git add .

# Commit the staged files with a descriptive message.
git commit -m "feat: add database parsing"
```

### Step 3: Upload Your Work

```bash
# Push your committed changes from your local branch to the remote branch
git push origin your-feature-branch-name
```

### Step 4: Merging and Handling Conflicts

```bash
# 1. Finish your work and commit final changes on your feature branch.

# 2. Switch to the parent branch (e.g., website-design)
git checkout website-design

# 3. Pull the latest updates for that parent branch
git pull origin website-design

# 4. Switch back to your feature branch
git checkout your-feature-branch-name

# 5. Merge the updated parent branch into your feature branch
git merge website-design

# 6. If a conflict occurs:
# Git will stop and tell you which file(s) have conflicts.
# Open the file in your editor. You'll see markers:

# <<<<<<< HEAD
# // Your changes
# =======
# // Incoming changes from other branch
# >>>>>>> website-design

# Resolve the conflict by manually editing the file, then delete the <<<<<<<, =======, and >>>>>>> markers.

# Save the file.

# Stage the resolved file and commit the merge
git add .
git commit -m "fix: resolve merge conflict"

# 7. Finally, push your updated, conflict-free branch to GitHub
git push origin your-feature-branch-name
```
