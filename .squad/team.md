# Squad Team

> romy-squad

## Coordinator

| Name | Role | Notes |
|------|------|-------|
| Squad | Coordinator | Routes work, enforces handoffs and reviewer gates. |

## Members

| Name | Role | Charter | Status |
|------|------|---------|--------|
| Konrad | Lead Orchestrator | `.squad/agents/konrad/charter.md` | Active |
| Talos | Azure SRE and Delivery Lead | `.squad/agents/talos/charter.md` | Active |
| Octavia | Azure Network Engineer | `.squad/agents/octavia/charter.md` | Active |
| Variel | Azure Data Engineer | `.squad/agents/variel/charter.md` | Active |
| Cyrion | Azure Observability Engineer | `.squad/agents/cyrion/charter.md` | Active |
| Septimus | Incident Documentation Lead | `.squad/agents/septimus/charter.md` | Active |
| Sevatar | Independent QA and Reviewer | `.squad/agents/sevatar/charter.md` | Active |
| Scribe | Decision Merger | `.squad/agents/scribe/charter.md` | Built-in |
| Ralph | Work Monitor | `.squad/agents/ralph/charter.md` | Built-in |
| Rai | RAI Reviewer | `.squad/agents/Rai/charter.md` | Built-in |
| Fact Checker | Devil's Advocate & Verification Agent | `.squad/agents/fact-checker/charter.md` | Built-in


## Coding Agent

<!-- copilot-auto-assign: false -->

| Name | Role | Charter | Status |
|------|------|---------|--------|
| @copilot | Coding Agent | — | 🤖 Coding Agent |

### Capabilities

**🟢 Good fit — auto-route when enabled:**
- Bug fixes with clear reproduction steps
- Test coverage (adding missing tests, fixing flaky tests)
- Lint/format fixes and code style cleanup
- Dependency updates and version bumps
- Small isolated features with clear specs
- Boilerplate/scaffolding generation
- Documentation fixes and README updates

**🟡 Needs review — route to @copilot but flag for squad member PR review:**
- Medium features with clear specs and acceptance criteria
- Refactoring with existing test coverage
- API endpoint additions following established patterns
- Migration scripts with well-defined schemas

**🔴 Not suitable — route to squad member instead:**
- Architecture decisions and system design
- Multi-system integration requiring coordination
- Ambiguous requirements needing clarification
- Security-critical changes (auth, encryption, access control)
- Performance-critical paths requiring benchmarking
- Changes requiring cross-team discussion

## Project Context

- **Project:** romy-squad
- **Owner / human lead:** R-Cipher (final authority)
- **Description:** Squad configuration for an Azure SRE/DevOps team; this repository contains Squad configuration and GitHub-based Squad automation.
- **Stack verified in repository:** Squad Markdown/JSON configuration and GitHub Actions for Squad triage, issue assignment, heartbeat, and label synchronization.
- **Created:** 2026-11-10

## Platform Sources of Truth

| Area | Status |
|------|--------|
| Code | Unknown |
| Workload CI/CD | Unknown. The repository's GitHub Actions workflows automate Squad operations; they do not establish the workload CI/CD source of truth. |
| Work tracking | Unknown. Squad automation uses GitHub Issues and labels, and the existing retrospective convention directs action items to GitHub Issues; whether those are the overall work-tracking source of truth or coexist with Azure Boards is not established. |

No Azure tenant, subscription, landing-zone, workload, or Azure DevOps organization/project configuration was found in the repository. Do not infer platform ownership from the Squad automation.
