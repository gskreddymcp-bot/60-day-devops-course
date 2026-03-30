# Lab 04 — First Azure Pipeline (CI: Build, Test, Scan, Publish)

## Objective
Create a practical CI pipeline with quality gates and artifact publication.

## Prerequisites
- Azure DevOps project + repository
- Pipeline permissions
- A sample app or script in repo

## Architecture
Commit/PR -> CI Pipeline -> Build/Test/Scan -> Publish Artifact (+ optional image push).

## Commands
Create `azure-pipelines.yml` in repo root:

```yaml
trigger:
- main

pr:
- main

pool:
  vmImage: ubuntu-latest

stages:
- stage: CI
  jobs:
  - job: build_test_scan
    steps:
    - checkout: self
    - script: echo "Restore dependencies"
      displayName: Restore
    - script: echo "Run lint"
      displayName: Lint
    - script: echo "Run unit tests"
      displayName: Unit Test
    - script: echo "Run SAST/secret scan"
      displayName: Security Scan
    - script: |
        mkdir -p out
        echo "build output" > out/app.txt
      displayName: Build
    - task: PublishBuildArtifacts@1
      inputs:
        PathtoPublish: out
        ArtifactName: drop
        publishLocation: Container
```

## Validation
```bash
# local yaml syntax sanity (if yq installed)
yq . azure-pipelines.yml
```
Pipeline run must show:
- PR/main trigger execution
- CI job with lint/test/scan/build steps
- Artifact named `drop` published successfully

## Troubleshooting
- Pipeline not triggering: verify pipeline is connected to correct branch/repo.
- Task errors: check agent image compatibility.
- Artifact missing: verify output folder exists before publish task.

## Assignment
Extend pipeline with:
- real test command for your sample app
- fail-fast behavior on test or scan failure
- Docker build and image push to ACR (if registry available)

## Solution
Lab is complete when a PR triggers CI and blocks merge if checks fail, while successful runs publish artifacts.
