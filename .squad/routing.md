# Work Routing

How to decide who handles what.

## Routing Table

| Work Type | Route To | Examples |
|-----------|----------|----------|
| Triage, coordination, multi-domain issues, active incidents | Konrad | Severity, scope, task breakdown, timeline, cross-domain coordination |
| Azure service troubleshooting and root-cause analysis | Talos | AKS, App Service, Functions, VMs, quotas, Azure Policy, Entra ID, RBAC, Key Vault |
| Delivery engineering and deployment failures | Talos | Azure Pipelines, GitHub Actions, runners, agent pools, service connections, OIDC, artifacts, rollback |
| Azure networking and connectivity | Octavia | VNets, peering, DNS, Private Link, firewalls, gateways, Front Door, runner connectivity |
| Azure data platforms and data integrity | Variel | Databases, Redis, Storage, replication, backups, restores, migrations |
| Observability and reliability signals | Cyrion | Azure Monitor, KQL, Application Insights, alerts, dashboards, SLOs |
| Incident records and operational documentation | Septimus | Timelines, updates, postmortems, runbooks, Azure Boards items, GitHub issues |
| Independent review and readiness | Sevatar | Pull request reviews, security checks, test plans, go/no-go, root-cause challenges |

Preset installation adds concrete routes for the configured team. Add or edit rows
here only when their agent names also exist in the casting registry.

## Issue Routing

| Label | Action | Who |
|-------|--------|-----|
| `squad` | Triage: analyze issue, assign `squad:{member}` label | Konrad |
| `squad:{name}` | Pick up issue and complete the work | Named member |

### How Issue Assignment Works

1. When a GitHub issue gets the `squad` label, **Konrad** triages it — analyzing content, assigning the right `squad:{member}` label, and commenting with triage notes.
2. When a `squad:{member}` label is applied, that member picks up the issue in their next session.
3. Members can reassign by removing their label and adding another member's label.
4. The `squad` label is the "inbox" — untriaged issues waiting for Lead review.

## Rules

1. **One accountable owner** — assign one primary owner per outcome; run other investigations in parallel only when independently useful and evidence or scope supports them.
2. **Scribe runs when needed** — spawn Scribe in the background when accepted durable decisions need merging; do not make Scribe a routine gate.
3. **Quick facts → coordinator answers directly.** Don't spawn an agent for "what port does the server run on?"
4. **When two agents could handle it**, pick the one whose domain is the primary concern.
5. **"Team, ..." → bounded coordination.** Konrad selects one accountable owner; split only independent outcomes with distinct owners.
6. **No speculative work.** Do not launch anticipatory downstream tasks unless requested or needed to meet an explicit deliverable.
7. **Issue-labeled work** — when a `squad:{member}` label is applied to an issue, route to that member. Konrad handles all `squad` (base label) triage.

## Incident Routing

For an active incident, Konrad starts Talos and Cyrion first and engages Septimus from the start. Add Octavia or Variel when evidence points to their domains. Sevatar independently reviews the proposed root cause and remediation before the incident is considered complete. Konrad does not substitute for Sevatar's review.

## Production Change Routing

The owning specialist proposes a production change in a pull request. Required checks must pass on the declared platform of record, Sevatar reviews the change and evidence, and the human lead approves before deployment. Platform-of-record details remain Unknown until confirmed.
