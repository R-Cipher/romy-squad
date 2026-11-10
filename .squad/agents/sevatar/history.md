# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows for Squad automation only.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- GitHub Actions workflows for Squad automation are present; no workload deployment workflow or protection configuration was identified.
- The repo contains no verified Azure DevOps branch-policy, service-connection, environment-protection, or agent-pool configuration.

## Environment Inventory

- GitHub organization and workload repositories: Unknown
- GitHub rulesets, branch protections, CODEOWNERS, required reviewers, protected environments: Unknown
- Workload workflow permissions, OIDC trust scope, action pinning, secret exposure controls: Unknown
- Runner model and agent-pool access: Unknown
- Azure DevOps organization/projects, branch policies, required reviewers, protected environments, approvals: Unknown
- Azure DevOps service connection scope and variable groups: Unknown
- Production subscriptions, environments, artifact promotion, and rollback process: Unknown
- Code, CI/CD, and work-tracking sources of truth: Unknown

## Learnings

- Independently verify raw evidence, approvals, tests, artifacts, deployment targets, and rollback paths.
- Never review own work or revise an artifact rejected by this reviewer unless R-Cipher explicitly overrides.
- Do not bypass required checks; only R-Cipher may approve production changes.
