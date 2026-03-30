# Azure DevOps 30-Day Training Plan (Practical, Engineer-Focused)

## Practical Course Intro

This course is built to train engineers on **how delivery actually happens** in Azure DevOps teams.

### Delivery flow students will execute repeatedly

```text
Request/Requirement
  -> Azure Boards
  -> Azure Repos
  -> PR Validation
  -> CI Build/Test/Scan
  -> Artifact/Image Publish
  -> Infra Provisioning
  -> App Deployment
  -> Verification
  -> Monitoring
  -> Feedback to Backlog
```

### Daily learning model
- **Learn (30–45 min):** key concepts for the day.
- **Build (45–60 min):** hands-on implementation in repo/Azure DevOps.
- **Validate (10–15 min):** prove output with commands, pipeline logs, or portal evidence.

> Suggested daily time: **90–120 minutes**.

---

## Day-by-Day Intro (What each day is for)

| Day | Focus | Why it matters in real delivery |
|---|---|---|
| 1 | DevOps + flow reality | Align everyone to the same engineering lifecycle |
| 2 | Git foundations | Build clean commit history and confidence |
| 3 | Branching + merge | Enable parallel team work without chaos |
| 4 | PR workflow | Enforce review quality before merge |
| 5 | Azure DevOps services | Understand tool boundaries and ownership |
| 6 | Azure Repos policies | Make quality gates mandatory |
| 7 | Azure Boards hierarchy | Connect work items to code and releases |
| 8 | Linux filesystem + permissions | Operate confidently on build agents and servers |
| 9 | Linux processes + services | Diagnose runtime issues quickly |
| 10 | CLI toolchain setup | Standardize developer workstation |
| 11 | Azure resource groups | Build cloud resource hygiene |
| 12 | Core networking/storage | Prepare runtime platform basics |
| 13 | Monitoring + cost baseline | Avoid blind operations |
| 14 | Git advanced workflows | Keep histories clean and recover safely |
| 15 | First YAML CI pipeline | Start automated quality checks |
| 16 | CI comparison (GitHub Actions) | Understand portability and tradeoffs |
| 17 | Automated testing in CI | Block bad builds early |
| 18 | Azure Artifacts | Reuse versioned dependencies/packages |
| 19 | Linux operational commands | Troubleshoot faster during incidents |
| 20 | CD environments + approvals | Promote safely across stages |
| 21 | IaC with Terraform/Bicep | Make infra repeatable and reviewable |
| 22 | DevSecOps basics | Add security into delivery, not after |
| 23 | Logs + dashboards | Build operational visibility |
| 24 | Docker fundamentals | Standardize app packaging |
| 25 | AKS deployment basics | Run containerized apps on Azure |
| 26 | Service connections + identity | Secure non-interactive deployments |
| 27 | End-to-end integration | Connect planning, code, and deployment |
| 28 | Troubleshooting + optimization | Improve reliability and speed |
| 29 | Final implementation | Ship a working project pipeline |
| 30 | Demo + feedback loop | Turn outcomes into backlog improvements |

---

## Day-by-Day Practice Details

Each day includes **Goal, Practice Steps, and Validation**.

## Day 1 — DevOps and Delivery Flow Reality
**Goal:** Understand team flow and ownership boundaries.

**Practice**
1. Create `notes/day-01.md`.
2. Document the end-to-end flow in your own words.
3. Map one sample story from request to monitoring.

**Validation**
- Notes include all stages from Boards to Monitoring.

## Day 2 — Git Basics I
**Goal:** Learn clone/add/commit/log confidently.

**Practice**
1. `git init`
2. `echo "Hello DevOps" > hello.txt`
3. `git add hello.txt && git commit -m "Add hello file"`
4. `git log --oneline -n 5`

**Validation**
- Commit appears in history with correct message.

## Day 3 — Git Basics II (Branch + Merge)
**Goal:** Use branches for isolated work.

**Practice**
1. `git checkout -b feature/day3`
2. Update `hello.txt`, commit changes.
3. `git checkout main && git merge feature/day3`
4. Simulate and resolve one merge conflict.

**Validation**
- Branch merged and conflict resolution documented in notes.

## Day 4 — Pull Request Workflow
**Goal:** Use PR as quality and collaboration gate.

**Practice**
1. Push feature branch to remote.
2. Open PR with description and linked work item.
3. Request at least one review.
4. Address review feedback and update PR.

**Validation**
- PR shows completed review and successful merge.

## Day 5 — Azure DevOps Services Overview
**Goal:** Understand Boards, Repos, Pipelines, Artifacts, Test Plans.

**Practice**
1. Create Azure DevOps project `DevOps-Training`.
2. Explore project settings and permissions.
3. Identify which team role owns which service.

**Validation**
- Short ownership matrix added to notes.

## Day 6 — Azure Repos + Branch Policies
**Goal:** Enforce engineering quality via policy.

**Practice**
1. Create repo and push sample code.
2. Configure branch policy on `main`:
   - minimum reviewers
   - comment resolution
   - build validation required
3. Test policy using a sample PR.

**Validation**
- PR cannot merge until policy checks pass.

## Day 7 — Azure Boards Hierarchy
**Goal:** Plan work in usable granularity.

**Practice**
1. Create Epic -> Feature -> User Story -> Task.
2. Add acceptance criteria to story.
3. Link branch/PR to story.

**Validation**
- Work item traceability visible from PR to story.

## Day 8 — Linux Basics I
**Goal:** Work with files and permissions on CLI.

**Practice**
1. Use `pwd`, `ls`, `cd`, `mkdir`, `touch`.
2. Change permissions with `chmod`.
3. Verify ownership with `ls -l`.

**Validation**
- File permission changes demonstrated in notes.

## Day 9 — Linux Basics II
**Goal:** Manage processes and services.

**Practice**
1. Check processes: `ps aux`, `top`.
2. Start/stop a simple background process.
3. Inspect service state: `systemctl status <service>`.

**Validation**
- Evidence of process start/stop captured.

## Day 10 — Developer Toolchain Setup
**Goal:** Standardize local tooling.

**Practice**
1. Configure Git username/email.
2. Install and verify `az`, `git`, `kubectl`.
3. Authenticate Azure CLI and set subscription.

**Validation**
- `az account show` and `git --version` outputs recorded.

## Day 11 — Azure Fundamentals I (RG + Subscription)
**Goal:** Use resource grouping correctly.

**Practice**
1. `az group create -n rg-devops-training -l eastus`
2. `az group list -o table`

**Validation**
- Resource group created in expected region.

## Day 12 — Azure Fundamentals II (Network + Storage)
**Goal:** Build base platform components.

**Practice**
1. Create storage account.
2. Create VNet and subnet.
3. Document naming convention.

**Validation**
- VNet/subnet and storage visible in portal/CLI list.

## Day 13 — Monitoring + Cost Baseline
**Goal:** Establish operational and budget visibility.

**Practice**
1. Enable Azure Monitor insights.
2. Create a cost budget and alert.
3. Capture baseline dashboard screenshot.

**Validation**
- Alert rule exists and dashboard is accessible.

## Day 14 — Git Advanced
**Goal:** Use stash/tag/rebase safely.

**Practice**
1. `git tag v1.0`
2. `git stash && git stash pop`
3. `git rebase main` on feature branch.

**Validation**
- Clean history and successful tag creation.

## Day 15 — First YAML CI Pipeline
**Goal:** Run automated build pipeline.

**Practice**
1. Add `azure-pipelines.yml`.
2. Include steps: checkout, lint, test, build, publish artifact.
3. Trigger pipeline from commit.

**Validation**
- Successful run with artifact output.

## Day 16 — Compare with GitHub Actions
**Goal:** Understand CI portability.

**Practice**
1. Create `.github/workflows/ci.yml` equivalent.
2. Compare syntax and runner model.
3. Record tradeoffs (Azure Pipelines vs Actions).

**Validation**
- Both pipelines run for same repo state.

## Day 17 — Test Automation in CI
**Goal:** Make tests mandatory for merge.

**Practice**
1. Add unit tests to sample app.
2. Run tests locally.
3. Fail pipeline on test failure.

**Validation**
- Broken test causes pipeline failure.

## Day 18 — Azure Artifacts
**Goal:** Publish and consume package versions.

**Practice**
1. Create feed.
2. Publish one package version.
3. Consume package in pipeline build.

**Validation**
- Pipeline resolves package from feed.

## Day 19 — Linux for DevOps Operations
**Goal:** Improve troubleshooting speed.

**Practice**
1. Analyze logs with `journalctl`.
2. Add a scheduled task with `cron`.
3. Run connectivity checks using `curl` and `ss`.

**Validation**
- Cron entry and command outputs documented.

## Day 20 — CD Environments + Approvals
**Goal:** Promote artifacts safely.

**Practice**
1. Create multi-stage deployment (DEV -> TEST/UAT -> PROD).
2. Add manual approvals for TEST/UAT and PROD.
3. Add smoke test post-deploy in DEV.

**Validation**
- Promotion blocked until approval is granted.

## Day 21 — Infrastructure as Code
**Goal:** Provision infra through code review process.

**Practice**
1. Write Terraform/Bicep template.
2. Run `fmt/validate/plan` in PR pipeline.
3. Apply only after approval.

**Validation**
- Plan output attached to PR; apply changes recorded.

## Day 22 — Security in Delivery
**Goal:** Add security gates into CI/CD.

**Practice**
1. Configure RBAC for least privilege.
2. Add secret scanning/SAST in CI.
3. Move sensitive values to Key Vault.

**Validation**
- Scan results published and secrets removed from repo.

## Day 23 — Monitoring + Logging
**Goal:** Observe app and infra health.

**Practice**
1. Create Log Analytics workspace.
2. Send app/platform logs.
3. Build alert and dashboard.

**Validation**
- Alert rule triggers on test condition.

## Day 24 — Docker Fundamentals
**Goal:** Package app into container image.

**Practice**
1. Write Dockerfile.
2. `docker build -t <app>:v1 .`
3. `docker run -p 8080:8080 <app>:v1`

**Validation**
- App responds successfully on local test endpoint.

## Day 25 — AKS Basics
**Goal:** Deploy containerized app to Kubernetes.

**Practice**
1. Create AKS cluster.
2. Deploy manifests (Deployment + Service).
3. Validate pod readiness and service exposure.

**Validation**
- `kubectl get pods,svc` shows healthy resources.

## Day 26 — Service Connections + Identity
**Goal:** Securely connect pipelines to Azure resources.

**Practice**
1. Create service connection.
2. Scope permissions minimally.
3. Use connection in deployment job.

**Validation**
- Deployment succeeds without interactive credentials.

## Day 27 — End-to-End Integration
**Goal:** Execute full flow from story to deployment.

**Practice**
1. Create Boards story and task.
2. Implement code on feature branch and PR.
3. Trigger CI, publish artifact/image, deploy to DEV.

**Validation**
- Traceability: story -> branch -> PR -> pipeline -> deployment.

## Day 28 — Troubleshooting + Optimization
**Goal:** Improve reliability and speed.

**Practice**
1. Intentionally break pipeline and diagnose root cause.
2. Add dependency caching.
3. Reduce noisy/failing steps.

**Validation**
- Build duration reduced and failure cause documented.

## Day 29 — Final Project Implementation
**Goal:** Deliver a production-like student project.

**Practice**
1. Build sample app + repo policy + CI/CD.
2. Provision infra using IaC.
3. Add monitoring + rollback runbook.

**Validation**
- End-to-end run demo works from PR to deployment.

## Day 30 — Demo, Review, Backlog Feedback
**Goal:** Close loop with evidence-driven improvement.

**Practice**
1. Demo architecture, pipeline, and monitoring.
2. Collect reviewer feedback as backlog items.
3. Plan next sprint improvements.

**Validation**
- At least three actionable backlog improvements created.

---

## Suggested Student Deliverables
1. Daily notes in `/notes/day-XX.md`.
2. A final project repo with CI/CD pipeline.
3. A README summarizing architecture, pipelines, and rollback steps.
4. Evidence pack: PR links, pipeline runs, deployment proof, alerts.
