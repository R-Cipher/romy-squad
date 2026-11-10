# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows for Squad triage, issue assignment, heartbeat, and label synchronization.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- `.github/agents/squad.agent.md` contains the installed Squad coordinator instructions.
- `.github/workflows/` contains Squad automation workflows, not workload deployment pipelines.
- Those workflows read `.squad/team.md` / `.squad/routing.md` and use GitHub Issues and labels.
- No workload infrastructure, Azure tenant/subscription details, or Azure DevOps org/project configuration was found.
- Code, workload CI/CD, and work-tracking sources of truth: **Unknown**. GitHub Issues are used by Squad automation, but that does not establish work-tracking ownership.

## Environment Inventory

- Azure tenant and subscriptions: Unknown
- Management groups and landing zones: Unknown
- Regions and DR pairs: Unknown
- Compute: Unknown
- Networking: Unknown
- Data platforms: Unknown
- Observability: Unknown
- Source of truth for code: Unknown
- Source of truth for workload CI/CD: Unknown
- Source of truth for work tracking: Unknown
- GitHub organization, workload repositories, runner model, environments, rulesets, CODEOWNERS: Unknown
- Azure DevOps organization, projects, Boards process, pipelines, agent pools, service connections, environments: Unknown
- Integrations: Unknown
- Infrastructure as code and deployment process: Unknown
- Incident tooling: Unknown

## Learnings

- Active incidents require Talos and Cyrion first, Septimus from the start, and Octavia or Variel as indicated by evidence.
- Sevatar independently reviews the proposed root cause and remediation before completion.
