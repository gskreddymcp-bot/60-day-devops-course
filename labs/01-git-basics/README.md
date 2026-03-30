# Lab 01 — Git Basics for Azure Repos

## Objective
Set up an engineer-grade Git workflow: clone, branch, commit, push, PR.

## Prerequisites
- Git installed
- Azure DevOps project with Repos enabled
- Permission to create branches and PRs

## Architecture
Developer workstation -> Azure Repos (remote origin) -> Pull Request review flow.

## Commands
```bash
# clone repository
git clone <azure-repos-url>
cd <repo>

# create feature branch
git checkout -b feature/invoice-upload

# make a change and commit
echo "pipeline placeholder" > notes.txt
git add notes.txt
git commit -m "Add notes placeholder for invoice service"

# push branch
git push -u origin feature/invoice-upload
```

## Validation
```bash
# verify branch and tracking
git branch -vv

# verify commit history
git log --oneline -n 5

# verify remote
git remote -v
```
Expected:
- Current branch is `feature/invoice-upload`
- Latest commit visible in log
- Remote points to Azure Repos URL

## Troubleshooting
- Auth failures: reconfigure PAT/Entra login for Azure DevOps.
- Push rejected: pull latest target branch and rebase.
- PR blocked: satisfy branch policy checks (reviewers/build validation).

## Assignment
Create a PR from `feature/invoice-upload` to `main` with:
- meaningful title
- work item link
- one reviewer
- completed PR template

## Solution
A complete solution means:
1. branch pushed to Azure Repos,
2. PR created and linked to a Boards item,
3. branch policy checks passed.
