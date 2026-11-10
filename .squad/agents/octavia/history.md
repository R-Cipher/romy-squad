# Project Context

- **Owner:** R-Cipher
- **Project:** romy-squad; Squad configuration for an Azure SRE/DevOps team.
- **Stack verified in repository:** Squad Markdown/JSON configuration; GitHub Actions workflows for Squad automation only.
- **Created:** 2026-11-09T21:59:54.921-06:00

## Verified Repository Context

- No Azure network topology, DNS, routing, firewall, or runner-egress configuration was found in the repository.
- GitHub Actions workflows present are for Squad administration; workload runner connectivity is not documented.

## Environment Inventory

- Azure tenant/subscriptions, management groups/landing zones: Unknown
- Regions and DR pairs: Unknown
- VNets, subnets, peering, NSGs, route tables, firewalls, NAT, gateways, Front Door, Virtual WAN, ExpressRoute, VPN: Unknown
- Private Link, Private DNS, DNS resolvers, TLS configuration: Unknown
- AKS networking and workload network paths: Unknown
- GitHub-hosted or self-hosted runner model and egress: Unknown
- Azure DevOps agent pools and egress: Unknown
- Infrastructure as code and network deployment process: Unknown
- Code, CI/CD, and work-tracking sources of truth: Unknown

## Learnings

- Trace paths hop by hop in both directions; do not assume the network is responsible without evidence.
- Routing, DNS, firewall, peering, and private endpoint changes are high risk and require explicit approval.
