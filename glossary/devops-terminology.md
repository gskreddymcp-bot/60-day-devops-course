# DevOps Terminology (Prioritized)

This glossary is ordered for teaching sequence, not alphabetically.

## 1) Planning
- **Epic**: Large business outcome grouping multiple features.
- **Feature**: A functional slice that delivers user/business value.
- **User Story**: End-user need in the format "As a..., I want..., so that...".
- **Task**: Technical work item required to complete a story.
- **Bug**: Defect that causes incorrect behavior.
- **Sprint**: Time-boxed iteration for planned delivery.

## 2) Git / Source Control
- **Repo**: Version-controlled source code container.
- **Clone**: Local copy of a remote repository.
- **Commit**: Snapshot of code changes with message/history.
- **Branch**: Independent line of development.
- **Pull Request (PR)**: Proposed change for review and merge.
- **Merge**: Integrate branch changes into target branch.
- **Rebase**: Re-apply commits on a new base for cleaner history.

## 3) Pipeline
- **Trigger**: Event that starts a pipeline (push/PR/schedule/manual).
- **Agent**: Compute worker running pipeline jobs.
- **Stage**: Major pipeline boundary (e.g., Build, Test, Deploy).
- **Job**: Group of steps running on an agent.
- **Step**: Individual command/task in a job.
- **Artifact**: Build output passed between stages.
- **Variable**: Reusable pipeline value.
- **Secret**: Sensitive value protected in pipeline/runtime.
- **Environment**: Target deployment scope with controls/history.
- **Approval**: Manual or policy gate before promotion.

## 4) Cloud / Platform
- **Subscription**: Billing and governance boundary in Azure.
- **Resource Group**: Logical container for Azure resources.
- **Service Connection**: Pipeline identity/config for Azure access.
- **Key Vault**: Secure storage for secrets, keys, certificates.
- **Managed Identity**: Azure-managed identity for service auth.
- **VNet**: Private virtual network in Azure.
- **Subnet**: Segmented IP range inside a VNet.

## 5) Containers / AKS
- **Image**: Immutable packaged application template.
- **Registry**: Image storage service (e.g., ACR).
- **Pod**: Smallest deployable unit in Kubernetes.
- **Deployment**: Desired-state controller for application pods.
- **Service**: Stable networking endpoint for pods.
- **Ingress**: HTTP/HTTPS routing into cluster services.
- **Namespace**: Logical isolation boundary in a cluster.
- **ConfigMap**: Non-sensitive configuration object.
- **Secret**: Sensitive configuration object.
- **Helm**: Kubernetes package manager.
- **Rollout**: Controlled deployment progression.
- **Rollback**: Revert deployment to known-good version.

## Practical Examples
- **User Story vs Task**:
  - Story: "As a buyer, I want to upload invoices."
  - Task: "Create pipeline YAML for invoice service."
- **Pipeline Artifact vs Deployment Artifact**:
  - Pipeline artifact: output from CI build.
  - Deployment artifact: Docker image or Helm chart used in CD.
