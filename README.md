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

- Allows specifying commits without using their long hash
- Move up 1 commit: `^`
  - `git checkout main^` => HEAD points to main's previous commit
- Move up # of commits: `~<#>`
  - `git checkout HEAD~4` => points HEAD to 4th ancestor commit after current HEAD position
- Reassign a branch to a commit with branch forcing `-f`:
  - `git branch -f branchToMove HEAD~3`

### 3. Reverse Changes

- `git reset`:
  - move branch backwards as if commit(s) never happened
  - rewrite history
  - recommended for local branches only
  - `git checkout branch && git reset HEAD^`
- `git revert`:
  - share reverted changes with others
  - adds reverting commit on top of current
  - recommended for remote branches
  - `git checkout branch && git revert HEAD`

# Moving Work Around

"I want this work here and that work there"

### 1. Cherry-pick

knowing which commit to get and their hashes

- `git cherry-pick c1 c2 c3...`:
  - copy a series of commits, then paste top of current HEAD

### 2. Interactive Rebase

not knowing which commit wanted

- `git rebase -i HEAD~<#Commits-including-HEAD>`
- `git rebase -i branchName`

# A Mixed Bag

### 1. Grab 1 commit

- `git checkout main && git cherry-pick commit#`

### 2. Juggle Commits

- reorder desired commits on top
  - `git rebase -i desiredCommitRange`
- make changes
  - `git commit --amend`
- reorder back to previous order
  - `git rebase -i desiredCommitRange`
- move main to the updated caption

  - `git rebase caption main`

- use `git cherry-pick` to avoid too much reordering
  - `git checkout main`
  - `git cherry-pick oldCommitToChange`
  - `git commit --amend`
  - `git cherry-pick latestCommit`

### 3. Git Tags

### 4. Git Describe

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
