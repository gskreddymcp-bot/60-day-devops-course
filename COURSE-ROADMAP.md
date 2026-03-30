# COURSE-ROADMAP.md

## Course Objective
Train engineers to deliver software on Azure using practical Azure DevOps workflows:
**Boards -> Repos -> PR -> CI -> Artifact/Image -> IaC -> CD -> Verify -> Monitor -> Feedback**.

## Module Order (Recommended)

1. DevOps and SDLC reality
2. Agile + Azure Boards
3. Git + Azure Repos
4. YAML pipelines
5. Docker
6. Terraform
7. Azure fundamentals
8. AKS + Helm
9. Key Vault + secrets
10. Monitoring + troubleshooting
11. End-to-end capstone

## Learning Tracks

### Track A (Must Read)
1. Pro Git (2nd Edition)
2. Terraform: Up & Running (3rd Edition)
3. Kubernetes: Up and Running (3rd Edition)

### Track B (Instructor Reference)
1. Microsoft Learn Azure DevOps docs
2. Learning DevOps (2nd Edition)
3. Azure DevOps Explained

## First Build Milestones (Do This Before Scaling Content)

- [x] `README.md`
- [x] `COURSE-ROADMAP.md`
- [x] `glossary/devops-terminology.md`
- [x] `labs/01-git-basics/README.md`
- [x] `labs/04-first-pipeline/README.md`
- [ ] one sample app
- [ ] one working CI pipeline
- [ ] one working CD pipeline

## Capstone Ideas

### Capstone 1: Single App Delivery
- Backlog in Azure Boards
- Repo and branch policy in Azure Repos
- PR validation
- CI build/test/scan
- Docker image push to ACR
- Deploy to AKS
- Smoke test + rollback

### Capstone 2: Infra + App Split
- Separate infra and app repositories
- Terraform modules and environment tfvars
- Key Vault secret injection
- Environment approvals (DEV/UAT/PROD)

## Lab Quality Standard
Each lab must include:
- Objective
- Prerequisites
- Architecture
- Commands
- Validation
- Troubleshooting
- Assignment
- Solution

If a lab does not include validation commands, it is incomplete.
