# Lab 01 — Complete Git Basics (Theory + Practicals)

## Objective
Build complete, hands-on Git fundamentals for day-to-day engineering work:
- create and initialize repositories,
- track and commit changes correctly,
- work safely with branches,
- inspect history,
- collaborate with remotes and pull requests,
- recover from common mistakes.

This lab is tool-agnostic for Git and maps cleanly to Azure Repos workflows.

## Prerequisites
- Git installed (`git --version`)
- A terminal (Bash, Zsh, PowerShell, or Git Bash)
- A code editor
- Optional for remote practice: Azure DevOps/GitHub/GitLab repository access

## Git Mental Model (Quick Theory)
Git has three core local areas:

1. **Working Directory** → where you edit files
2. **Staging Area (Index)** → where you prepare selected changes
3. **Local Repository (.git)** → where commits are stored

A commit is a snapshot with history metadata (author, time, message, parent commit).

## Architecture Diagram
```text
                    (optional)
            +----------------------+
            |  Remote repository   |
            | (Azure Repos origin) |
            +----------+-----------+
                       ^   push/pull/fetch
                       |
+----------------------+---------------------+
|              Local machine                |
|                                            |
|  Working Directory --> Staging --> Commits |
|    (edit files)        (index)   (.git)    |
+--------------------------------------------+
```

## Part A — Setup and First Repository

### 1) Configure identity (one-time)
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global init.defaultBranch main
```

### 2) Create a sample project from scratch
```bash
mkdir git-practice-app
cd git-practice-app

git init

echo "# Git Practice App" > README.md
mkdir -p src docs tests
cat > src/app.py <<'PY'
print("hello git")
PY

git status
git add README.md src/app.py
git commit -m "Initialize sample project structure"
```

### 3) Add useful ignore rules
```bash
cat > .gitignore <<'EOF_IGNORE'
__pycache__/
*.pyc
.env
.vscode/
.DS_Store
EOF_IGNORE

git add .gitignore
git commit -m "Add base .gitignore"
```

## Part B — Core Daily Commands

### 1) Inspect state and differences
```bash
git status
git diff
git diff --staged
```

### 2) Stage with control
```bash
git add src/app.py
git add -p            # interactive hunk staging
```

### 3) Commit best practices
```bash
git commit -m "Add greeting output to app"
```

Use commit messages in imperative style:
- `Add user login endpoint`
- `Fix null check in parser`
- `Refactor billing service module`

### 4) Read history
```bash
git log --oneline --graph --decorate -n 20
git show <commit_sha>
```

## Part C — Branching and Merge Flow

### 1) Create a feature branch
```bash
git checkout -b feature/add-version-endpoint
```

### 2) Make a change and commit
```bash
echo 'print("v1.0.0")' >> src/app.py
git add src/app.py
git commit -m "Add version output"
```

### 3) Return to main and merge
```bash
git checkout main
git merge feature/add-version-endpoint
```

### Branching Diagram
```text
main:    A-----B---------E
               \       /
feature:        C-----D
```

## Part D — Remote Collaboration (Azure Repos style)

### 1) Connect remote and push
```bash
git remote add origin <azure-repos-url>
git push -u origin main
```

### 2) Typical feature workflow
```bash
git checkout -b feature/invoice-upload
# make edits
git add .
git commit -m "Implement invoice upload placeholder"
git push -u origin feature/invoice-upload
```

Then open a Pull Request: `feature/invoice-upload` → `main`.

### 3) Sync frequently
```bash
git fetch origin
git pull --rebase origin main
```

## Part E — Undo and Recovery (Most Important Practicals)

### 1) Unstage files (keep file changes)
```bash
git restore --staged <file>
```

### 2) Discard local working change
```bash
git restore <file>
```

### 3) Amend last commit message/content
```bash
git commit --amend
```

### 4) Recover using reflog
```bash
git reflog
git checkout <reflog_commit_sha>
```

### 5) Reset modes (use carefully)
```bash
git reset --soft <commit_sha>   # move HEAD, keep staged changes
git reset --mixed <commit_sha>  # default, unstage changes
git reset --hard <commit_sha>   # destructive to local changes
```

## Part F — Merge Conflict Practice

1. Create branch A and modify same line in `README.md`.
2. Create branch B from main and modify same line differently.
3. Merge A into main, then merge B into main.
4. Resolve conflict markers manually:
   - `<<<<<<<`
   - `=======`
   - `>>>>>>>`
5. Finalize:
```bash
git add README.md
git commit -m "Resolve README merge conflict"
```

## Validation Checklist
Run these commands and verify outputs:

```bash
git status
git branch -vv
git log --oneline --graph --decorate -n 15
git remote -v
```

Expected:
- Clean working tree after commits (`nothing to commit, working tree clean`)
- Feature branches visible with tracking info
- Commit graph shows branch/merge flow
- `origin` configured correctly

## Troubleshooting
- **Authentication failed on push**: refresh PAT/token or re-login to Azure DevOps.
- **Rejected push (non-fast-forward)**: `git pull --rebase origin <branch>` then push.
- **Wrong file committed**: `git restore --staged <file>` and recommit.
- **Accidentally deleted commit**: use `git reflog` to locate and recover.

## Complete Practice Assignment
Complete all tasks below in order:

1. Initialize `git-practice-app` and create 3 commits.
2. Create `feature/readme-update` branch and add project usage docs.
3. Create `feature/test-scaffold` branch and add `tests/test_app.py`.
4. Merge both branches into `main`.
5. Push all branches to remote.
6. Raise at least one PR and complete review flow.
7. Intentionally create one merge conflict and resolve it.
8. Demonstrate one recovery action using `git reflog`.

## Solution Standard (Lab Completion Criteria)
A complete solution means:
1. Repository has meaningful commit history (minimum 6 commits).
2. At least two feature branches were created and merged.
3. Remote branch tracking is set (`-u origin <branch>` used).
4. One pull request flow completed.
5. One merge conflict resolved and committed.
6. One undo/recovery command demonstrated with notes.
