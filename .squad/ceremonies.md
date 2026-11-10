# Ceremonies

> Team meetings that happen before or after work. Each squad configures their own.

## Incident Kickoff

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | before |
| **Condition** | Active production incident or suspected customer-impacting outage |
| **Facilitator** | Konrad |
| **Participants** | Talos, Cyrion, Septimus; add Octavia or Variel based on evidence |
| **Time budget** | focused |
| **Enabled** | yes |

**Agenda:**
1. Establish severity, affected customers, subscriptions, regions, services, and repositories from evidence.
2. Check Azure Service Health, recent deployments, pipeline and workflow runs, and merged pull requests.
3. Record UTC timeline, confirmed facts, hypotheses, open questions, and action owners.
4. Keep investigation read-only until the human lead approves a production-changing action.

## Production Change Review

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | before |
| **Condition** | Proposed production change before deployment |
| **Facilitator** | Konrad |
| **Participants** | Owning specialist, Sevatar |
| **Time budget** | focused |
| **Enabled** | yes |

**Agenda:**
1. Confirm the platform of record, target subscription and environment, approved pull request, artifact, and required checks.
2. Have Sevatar independently verify the change, evidence, approval path, and rollback.
3. State exact action, expected impact, blast radius, verification method, and rollback plan for human approval.
4. Do not deploy until the human lead explicitly approves.

## Post-Incident Review

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | after |
| **Condition** | Incident mitigated and closure explicitly approved by the human lead |
| **Facilitator** | Septimus |
| **Participants** | Konrad, incident owners, Sevatar |
| **Time budget** | focused |
| **Enabled** | yes |

**Agenda:**
1. Reconstruct the UTC timeline from evidence and separate confirmed facts from hypotheses.
2. Review detection, response, customer impact, mitigations, and unresolved risks without blame.
3. Verify the proposed root cause and remediation with Sevatar; link safe evidence.
4. Record follow-up actions in the confirmed work-tracking source of truth; do not duplicate work across platforms.

## Design Review

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | before |
| **Condition** | multi-agent task involving 2+ agents modifying shared systems |
| **Facilitator** | lead |
| **Participants** | all-relevant |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. Review the task and requirements
2. Agree on interfaces and contracts between components
3. Identify risks and edge cases
4. Assign action items

---

## Retrospective

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | after |
| **Condition** | build failure, test failure, or reviewer rejection |
| **Facilitator** | lead |
| **Participants** | all-involved |
| **Time budget** | focused |
| **Enabled** | ✅ yes |

**Agenda:**
1. What happened? (facts only)
2. Root cause analysis
3. What should change?
4. Action items for next iteration


---

## Retrospective with Enforcement

| Field | Value |
|-------|-------|
| **Trigger** | auto |
| **When** | weekly |
| **Condition** | No *retrospective* log in .squad/log/ within the last 7 days |
| **Facilitator** | lead |
| **Participants** | all |
| **Time budget** | focused |
| **Enabled** | yes |
| **Enforcement skill** | retro-enforcement |

**Agenda:**
1. What shipped this week? (closed issues, merged PRs)
2. What did not ship? (open issues, blockers)
3. Root cause on any failures
4. Action items -- each MUST become a GitHub Issue labeled retro-action

**Coordinator integration:**
At round start, call Test-RetroOverdue (see skill retro-enforcement). If overdue, run this ceremony before the work queue.

**Why GitHub Issues, not markdown:**
Production data: 0% completion across 6 retros using markdown checklists, 100% after switching to GitHub Issues.
