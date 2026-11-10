# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows use GitHub Issues and labels for Squad automation.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- `squad-triage.yml`, `squad-issue-assign.yml`, `squad-heartbeat.yml`, and `sync-squad-labels.yml` automate Squad handling of GitHub Issues and labels.
- The existing retrospective convention directs retrospective action items to GitHub Issues.
- The workflows do not establish whether GitHub Issues or Azure Boards is the organization's work-tracking source of truth.
- No Azure Boards organization, project, process, or integration configuration was found.

## Environment Inventory

- Code source of truth: Unknown
- Workload CI/CD source of truth: Unknown
- Work-tracking source of truth: Unknown
- GitHub organization, workload repositories, environments, rulesets, CODEOWNERS: Unknown
- Azure DevOps organization, projects, Boards process, pipelines, pools, service connections, environments: Unknown
- Azure Boards/GitHub integration: Unknown
- Incident tooling (Azure Monitor alerts, PagerDuty, ServiceNow, Teams, or other): Unknown
- Incident stakeholder and customer communication process: Unknown

## Learnings

- Keep confirmed facts, hypotheses, and open questions separate, and use UTC timestamps.
- Do not duplicate tracking across platforms or use AB# links until the Azure Boards/GitHub integration is confirmed.
- Formal records use a plain, professional tone without the team theme.
