# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows for Squad automation only.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- The repository has GitHub Actions workflows for Squad triage, issue assignment, heartbeat, and label synchronization.
- No workload pipeline, Azure subscription, workload deployment, or Azure DevOps configuration was found.
- Code, workload CI/CD, and work-tracking sources of truth: **Unknown**.

## Environment Inventory

- Azure tenant and subscriptions: Unknown
- Management groups and landing zones: Unknown
- Regions and DR pairs: Unknown
- Compute: Unknown
- Azure Policy, Entra ID, RBAC, managed identity, and Key Vault configuration: Unknown
- Azure Pipelines and workload GitHub Actions: Unknown
- GitHub organization, workload repositories, runner model, environments: Unknown
- Azure DevOps organization, projects, pipelines, agent pools, service connections, environments: Unknown
- Infrastructure as code and deployment process: Unknown
- Incident tooling: Unknown

## Learnings

- Trace every production change from pull request to build, artifact, approval, deployment, and running version.
- Network issues go to Octavia; deep data issues go to Variel. Production actions require R-Cipher's explicit approval.
