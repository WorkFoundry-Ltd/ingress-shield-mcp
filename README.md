# Ingress Shield MCP

Public documentation and safe-use guidance for WorkFoundry Ltd's **Ingress Shield Agent Preflight** MCP.

## What it is

Ingress Shield is WorkFoundry's controlled integration pilot, built on Atom Flux foundations for explicit boundaries, governed workflow plans and evidence-led operation.

Its Agent Preflight surface is a bounded, account-scoped, read-only Model Context Protocol (MCP) interface. It helps an approved AI coding or agent client check whether a proposed tool chain, API or webhook connection, or workflow draft is compatible before action. It can surface missing fields, stranded outputs, mismatched formats and required explicit adapters.

A compatibility result is evidence for human review. It is not permission to execute work, alter a workflow, change a destination, access a secret, or make an arbitrary network call.

## Current read-only tool surface

Ingress Shield currently exposes six public capability names for the Agent Preflight pilot. They are bounded, account-scoped and read-only. Their availability and exact input schemas are confirmed through `tools/list` after approved onboarding.

- [`atomflux_preflight_tool_graph`](docs/tool-catalog.md#atomflux_preflight_tool_graph) — check a declared tool graph for interface seams.
- [`atomflux_preflight_lattice`](docs/tool-catalog.md#atomflux_preflight_lattice) — analyse an unsigned workflow or Lattice draft before action.
- [`atomflux_diff_draft`](docs/tool-catalog.md#atomflux_diff_draft) — compare two unsigned safe drafts.
- [`atomflux_scaffold_draft`](docs/tool-catalog.md#atomflux_scaffold_draft) — produce an unsigned proposal starting point.
- [`atomflux_get_status`](docs/tool-catalog.md#atomflux_get_status) — read a caller-owned bounded result status.
- [`atomflux_explain_status`](docs/tool-catalog.md#atomflux_explain_status) — read a caller-owned corrective explanation.

See the [full tool catalogue](docs/tool-catalog.md) for purpose and boundaries. Do not infer arguments from this list; use only the schema returned for the approved account.

## Controlled-pilot access

Access is invite-only and reviewed. There is no public self-service sign-up, shared credential, or general-purpose endpoint configuration in this repository.

Do not guess or copy connection settings from public documentation. When a pilot is approved, WorkFoundry supplies the exact client-specific onboarding instructions through the agreed secure channel. After onboarding, an MCP client should discover the currently available tools through its standard `tools/list` operation and use only the returned schemas.

## Safe use

Use Agent Preflight to understand a declared connection before action. Send only the minimum non-sensitive input required by the discovered tool schema.

Never submit passwords, API keys, access tokens, private keys, signing material, personal data, confidential payloads, source code, private URLs, private endpoints, or deployment details.

For detailed agent behaviour, read [SKILL.md](SKILL.md). For individual tool purpose and limits, read [docs/tool-catalog.md](docs/tool-catalog.md). For human and agent safe-use guidance, read [docs/safe-use.md](docs/safe-use.md).

## Scope

This repository is documentation only. It contains no Atom Flux runtime source, Ingress Shield service source, deployment rail, credential, endpoint configuration, OAuth configuration, customer data, or operational access material.

## Links

- [WorkFoundry](https://workfoundry.co.uk/)
- [Agent Preflight and Webhook Boundary solution brief](https://workfoundry.co.uk/solution-brief/)
- [WorkFoundry AI-readable overview](https://workfoundry.co.uk/llms.txt)
- [Pilot privacy information](https://workfoundry.co.uk/privacy/)
- Pilot enquiries: [ingress-shield@workfoundry.co.uk](mailto:ingress-shield@workfoundry.co.uk)

WorkFoundry Ltd and workfoundry.co.uk are not affiliated with WorkFoundry.ai.