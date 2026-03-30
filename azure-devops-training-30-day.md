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