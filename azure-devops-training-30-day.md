# Azure DevOps 30-Day Training Plan (Day-wise Tasks + Step-by-Step Labs)

This plan is designed for **30 days** of instructor-led or self-paced learning. Each day includes:
- **Priority basics** (concepts first, then tooling)
- **Clear step-by-step tasks**
- **Practice labs** in the same repo and in Azure

> **Suggested daily time:** 90–120 minutes (45–60 min learning + 45–60 min practice)

---

## Day 1 — Orientation + DevOps Fundamentals (Priority Basics)
**Goals:** Understand DevOps, lifecycle, and toolchain map.

**Learn**
1. What is DevOps? Culture, CALMS, CI/CD, DevSecOps.
2. Lifecycle stages: Plan → Code → Build → Test → Release → Deploy → Operate → Monitor.
3. Tooling overview: Azure DevOps, Git/GitHub, Azure, Linux, Dev tools.

**Practice (Steps)**
1. Create a student folder for notes: `notes/day-01.md`.
2. Write definitions for DevOps, CI, CD, and IaC.
3. Draw a lifecycle flow diagram in Markdown (ASCII ok).

---

## Day 2 — Git Basics I (Priority Basics)
**Goals:** Understand repositories, commits, status, logs.

**Learn**
1. Git vs GitHub vs Azure DevOps Repos.
2. Working directory, staging area, commit history.

**Practice (Steps)**
1. Initialize a repo: `git init`.
2. Add a file: `echo "Hello DevOps" > hello.txt`.
3. Stage/commit:
   - `git add hello.txt`
   - `git commit -m "Add hello file"`
4. View history: `git log --oneline`.

---

## Day 3 — Git Basics II
**Goals:** Branching, merging, conflicts.

**Practice (Steps)**
1. Create branch: `git checkout -b feature/day3`.
2. Edit `hello.txt`, commit.
3. Switch back: `git checkout main`.
4. Merge: `git merge feature/day3`.
5. Simulate conflict: edit same line in two branches, merge and resolve.

---

## Day 4 — GitHub Basics
**Goals:** Understand GitHub workflow.

**Practice (Steps)**
1. Create GitHub account (if not already).
2. Create repo and add README.
3. Push local repo:
   - `git remote add origin <url>`
   - `git push -u origin main`
4. Create a branch, push, open a Pull Request.

---

## Day 5 — Azure DevOps Basics (Overview)
**Goals:** Understand Azure DevOps Services components.

**Learn**
1. Azure DevOps: Boards, Repos, Pipelines, Test Plans, Artifacts.
2. Org/Project structure.

**Practice (Steps)**
1. Create Azure DevOps organization.
2. Create project: `DevOps-Training`.
3. Explore project settings.

---

## Day 6 — Azure DevOps Repos
**Practice (Steps)**
1. Create a repo in Azure DevOps.
2. Clone locally.
3. Add a sample file and push.
4. Create branch policy (require PR).

---

## Day 7 — Azure Boards
**Practice (Steps)**
1. Create Epic → Feature → User Story → Task.
2. Assign to yourself, set iteration.
3. Use Kanban board to move cards.

---

## Day 8 — Linux Basics I
**Goals:** Filesystem, navigation, permissions.

**Practice (Steps)**
1. Commands: `pwd`, `ls`, `cd`.
2. Create directories/files: `mkdir`, `touch`.
3. Permissions: `chmod`, `chown`.

---

## Day 9 — Linux Basics II
**Goals:** Process and service basics.

**Practice (Steps)**
1. View processes: `ps`, `top`.
2. Kill a process: `kill`.
3. Check services: `systemctl status <service>`.

---

## Day 10 — Development Tools
**Goals:** Editors, CLI, packaging.

**Practice (Steps)**
1. Install VS Code.
2. Configure Git in VS Code.
3. Use CLI: `az`, `git`, `kubectl` (install only).

---

## Day 11 — Azure Infra Basics I
**Goals:** Azure subscriptions, resource groups.

**Practice (Steps)**
1. Create resource group: `rg-devops-training`.
2. List resources with `az group list`.

---

## Day 12 — Azure Infra Basics II
**Goals:** Compute, Storage, Networking.

**Practice (Steps)**
1. Create Storage Account.
2. Create Virtual Network + Subnet.
3. Create VM (Linux).

---

## Day 13 — Azure Infra Basics III
**Goals:** Monitoring and cost basics.

**Practice (Steps)**
1. Enable Azure Monitor on VM.
2. Set a budget in Cost Management.

---

## Day 14 — Git Advanced
**Goals:** Tags, rebase, stash.

**Practice (Steps)**
1. Create tags: `git tag v1.0`.
2. Stash changes: `git stash`, `git stash pop`.
3. Rebase feature branch onto main.

---

## Day 15 — Azure Pipelines Basics
**Goals:** CI pipeline introduction.

**Practice (Steps)**
1. Create pipeline from YAML.
2. Build a simple app (or echo command).
3. Run pipeline, review logs.

---

## Day 16 — CI with GitHub Actions
**Goals:** Compare Azure Pipelines with GitHub Actions.

**Practice (Steps)**
1. Create `.github/workflows/ci.yml`.
2. Simple build/test (echo ok).
3. Push and verify run.

---

## Day 17 — Test Automation Basics
**Goals:** Unit vs integration tests.

**Practice (Steps)**
1. Add a small test for sample code.
2. Run tests locally.
3. Integrate into pipeline.

---

## Day 18 — Azure Artifacts
**Goals:** Understand package management.

**Practice (Steps)**
1. Create a feed.
2. Publish a package.
3. Consume package in pipeline.

---

## Day 19 — Linux for DevOps
**Goals:** Logs, cron, networking tools.

**Practice (Steps)**
1. View logs: `journalctl`.
2. Create a cron job.
3. Use `curl`, `wget`, `ss`.

---

## Day 20 — Azure DevOps Releases
**Goals:** Classic release pipelines and environments.

**Practice (Steps)**
1. Create a Release pipeline.
2. Add dev stage and deploy a sample artifact.
3. Add approvals.

---

## Day 21 — IaC Basics (ARM/Bicep or Terraform)
**Goals:** Infrastructure as Code.

**Practice (Steps)**
1. Write a simple Bicep/Terraform template.
2. Deploy to a resource group.
3. Destroy resources.

---

## Day 22 — Security Basics
**Goals:** DevSecOps and Azure security basics.

**Practice (Steps)**
1. Set RBAC role for a user.
2. Enable MFA.
3. Scan pipeline for vulnerabilities.

---

## Day 23 — Monitoring & Logging
**Goals:** App Insights, Log Analytics.

**Practice (Steps)**
1. Create Log Analytics workspace.
2. Send VM logs.
3. Build a basic dashboard.

---

## Day 24 — Container Basics
**Goals:** Docker fundamentals.

**Practice (Steps)**
1. Install Docker.
2. Build a Docker image.
3. Run container and expose port.

---

## Day 25 — Kubernetes Basics
**Goals:** AKS introduction.

**Practice (Steps)**
1. Create AKS cluster.
2. Deploy app (kubectl apply).
3. Expose service.

---

## Day 26 — Azure DevOps Service Connections
**Goals:** Connect Azure DevOps to Azure.

**Practice (Steps)**
1. Create Service Connection.
2. Use it in pipeline to deploy.

---

## Day 27 — End-to-End Project Setup
**Goals:** Combine tools.

**Practice (Steps)**
1. Create repo in Azure DevOps.
2. Add sample app.
3. Pipeline builds and deploys to Azure.

---

## Day 28 — Troubleshooting + Optimization
**Goals:** Debug pipelines, improve builds.

**Practice (Steps)**
1. Break a pipeline, find error.
2. Cache dependencies.
3. Add retry logic.

---

## Day 29 — Final Project Implementation
**Goals:** Student project execution.

**Practice (Steps)**
1. Choose a sample app.
2. Configure CI/CD to Azure.
3. Document steps.

---

## Day 30 — Demo Day + Review
**Goals:** Present, review, and improve.

**Practice (Steps)**
1. Demo project pipeline.
2. Collect feedback.
3. Create a learning summary.

---

# Appendix: Priority-wise Basics (Quick Reference)

## Priority 1 — Core Foundations
- Git (commit, branch, merge, conflict)
- Azure DevOps (Boards, Repos, Pipelines)
- Azure Infra (resource groups, VM, VNet, storage)
- Linux (files, permissions, processes)

## Priority 2 — Collaboration & CI/CD
- GitHub workflow
- Azure Pipelines YAML
- Releases, environments, approvals

## Priority 3 — Advanced Skills
- IaC (Bicep/Terraform)
- Containers (Docker)
- Kubernetes (AKS)
- Monitoring & Security

---

# Suggested Student Deliverables
1. Daily notes in `/notes/day-XX.md`.
2. A final project repo with CI/CD pipeline.
3. A README summarizing architecture and steps.
