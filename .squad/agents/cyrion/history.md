# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows for Squad automation only.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- No workload Azure Monitor, Log Analytics, Application Insights, Grafana, dashboard, alert, or SLO configuration was found.
- The repository's workflows report Squad automation activity; they do not document application telemetry.

## Environment Inventory

- Azure tenant/subscriptions, regions, and workload inventory: Unknown
- Azure Monitor, Log Analytics, Application Insights, Container Insights: Unknown
- Managed Grafana, alert rules, action groups, workbooks: Unknown
- SLOs, SLIs, burn-rate thresholds, and baselines: Unknown
- Diagnostic settings, retention, sampling, and ingestion configuration: Unknown
- Deployment markers and workload pipeline/workflow telemetry: Unknown
- Code, CI/CD, and work-tracking sources of truth: Unknown
- Incident tooling and notification integrations: Unknown

## Learnings

- Correlation is not causation. Include the KQL or metric query, UTC time range, confidence, and data gaps for each conclusion.
- Check retention, diagnostic settings, sampling, and ingestion delay before treating missing telemetry as absence of an event.
