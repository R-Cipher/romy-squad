# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows for Squad automation only.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- No Azure database, cache, storage, schema, backup, replication, or migration configuration was found in the repository.
- No workload infrastructure or Azure DevOps deployment configuration was found.

## Environment Inventory

- Azure tenant and subscriptions: Unknown
- Data platforms (Azure SQL/MI, PostgreSQL/MySQL Flexible Server, Cosmos DB, Redis, Storage): Unknown
- Regions, geo-redundancy, replication, and failover configuration: Unknown
- Backups, restore points, and point-in-time restore configuration: Unknown
- Database capacity, performance baselines, and migration process: Unknown
- Infrastructure as code and deployment process: Unknown
- Code, CI/CD, and work-tracking sources of truth: Unknown
- Azure DevOps organization/projects, pipelines, service connections, and environments: Unknown
- Incident tooling: Unknown

## Learnings

- Confirm backup, restore, and replication state before recommending risky action.
- Writes, migrations, failovers, restores, SKU/storage changes, and data repair require explicit approval.
- Automated replacement or destruction of a stateful resource is **BLOCKED** pending R-Cipher's review.
