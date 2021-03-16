# GIT REVIEW MAIN

# Intro

### 1. Git Commits

- `git commit -m "commit message"`

### 2. Branch

Branch early, branch often:

- `git checkout -b branchName`

### 3. Merge

Branching and Merging:

- `git checkout branch1`
- `git commit`
- `git checkout branch2`
- `git commit`
- `git merge branch1`: merge branch 1 into current branch2

### 4. Rebase

Rebase: copy sets of commits, paste elsewhere
=> linear commit sequence:

- `git checkout bugFix`
- `git commit`
- `git checkout main`
- `git commit`
- `git checkout bugFix`
- `git rebase main` => rebase `bugFix` onto `main`

# Ramping Up

Moving around git commits

### 1. Detach HEAD

- HEAD: usually points to most recent commit
- Detaching HEAD: attach HEAD to a commit, instead of branch
- `HEAD -> main -> C1` becomes `HEAD -> C1`

### 2. Relative Refs

### 3. Reverse Changes

# Moving Work Around

### Cherry-pick

### Interactive Rebase

# A Mixed Bag

### Grab 1 commit

### Juggle Commits

### Juggle Commits

### Git Tags

### Git Describe

# Advanced Topics

### Rebase

### Multiple Parents

### Branch Spaghetti

# GIT REVIEW REMOTE

# Push & Pull -- Git Remotes

### Clone

### Remote Branches

### Git Fetch

### Git Pull

### Git Push

### Diverged History

### Locked Master

# Advanced Git Remotes

### Push Master

### Merge with Remote

### Merge with Remote

### Remote Tracking

### Push Arguments

### Fetch Arguments

### Source of Nothing

### Pull Arguments
