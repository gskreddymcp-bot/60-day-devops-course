# Azure DevOps Diagram Prompts (Practical)

## 1) Azure DevOps End-to-End Engineering Flow
Create a clean enterprise architecture diagram on a white background titled **"Azure DevOps End-to-End Engineering Flow"**. Show left-to-right flow:
Business Request -> Azure Boards -> Azure Repos -> Pull Request Validation Pipeline -> CI Build/Test/Scan -> Artifact Publish / ACR Image Push -> CD Deploy to DEV -> Approval Gate -> Deploy to TEST/UAT -> Approval Gate -> Deploy to PROD -> Monitoring / Alerts -> Feedback back into Boards.
Use swimlanes for: Planning, Source Control, CI, CD, Runtime, Operations.

## 2) Student Project Flow - From Story to Production
Create a premium Azure-style course diagram titled **"Student Project Flow - From Story to Production"**. Show six horizontal layers:
1) Product Owner / Student
2) Azure Boards
3) Azure Repos + Branching
4) Azure Pipelines CI
5) Azure Pipelines CD
6) Azure Runtime on AKS/App Service
Include: Git branching, PR checks, test execution, Docker build, artifact/image publish, infra provisioning, app deployment, smoke test, rollback, and monitoring.

## 3) Branching Strategy for Azure DevOps Training
Create a clean workflow diagram titled **"Branching Strategy for Azure DevOps Training"**. Show `main`, `develop`, `feature/*`, `release/*`, `hotfix/*` with arrows for PR flow, merge policy, and deployment triggers for DEV, UAT, PROD.

## 4) CI Pipeline Flow - Build, Test, Scan, Package
Create a clean engineering diagram titled **"CI Pipeline Flow - Build, Test, Scan, Package"**.
Stages: Checkout -> Restore Dependencies -> Lint -> Unit Test -> SAST / Secret Scan -> Build -> Docker Build -> Publish Artifact -> Push Image.
Add failure gates after test and scan.

## 5) CD Pipeline Flow - Environment Promotion
Create a multi-stage release diagram titled **"CD Pipeline Flow - Environment Promotion"**.
Show artifact consumed by DEV deployment, smoke test, TEST approval, UAT verification, PROD approval, PROD deployment, rollback path, and post-deploy validation.

## 6) Terraform Delivery Flow in Azure DevOps
Create an Azure IaC diagram titled **"Terraform Delivery Flow in Azure DevOps"**.
Show developer commit -> PR validation -> `terraform fmt/validate/plan` -> approval -> `terraform apply` -> Azure resources.
Include backend state storage, tfvars per environment, and service connection authentication.
