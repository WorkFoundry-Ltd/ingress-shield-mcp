# Ingress Shield MCP

Public documentation and safe-use guidance for WorkFoundry Ltd's **Ingress Shield Agent Preflight** MCP.

## What it is

Ingress Shield is WorkFoundry's controlled integration pilot, built on Atom Flux foundations for explicit boundaries, governed workflow plans and evidence-led operation.

Its Agent Preflight surface is a bounded, account-scoped, read-only Model Context Protocol (MCP) interface. It helps an approved AI coding or agent client check whether a proposed tool chain, API or webhook connection, or workflow draft is compatible before action. It can surface missing fields, stranded outputs, mismatched formats and required explicit adapters.

A compatibility result is evidence for human review. It is not permission to execute work, alter a workflow, change a destination, access a secret, or make an arbitrary network call.

## Controlled-pilot access

Access is invite-only and reviewed. There is no public self-service sign-up, shared credential, or general-purpose endpoint configuration in this repository.

Do not guess or copy connection settings from public documentation. When a pilot is approved, WorkFoundry supplies the exact client-specific onboarding instructions through the agreed secure channel. After onboarding, an MCP client should discover the currently available tools through its standard tools/list operation and use only the returned schemas.

## Safe use

Use Agent Preflight to understand a declared connection before action. Send only the minimum non-sensitive input required by the discovered tool schema.

Never submit passwords, API keys, access tokens, private keys, signing material, personal data, confidential payloads, source code, private URLs, private endpoints, or deployment details.

For detailed agent behaviour, read [SKILL.md](SKILL.md). For human and agent safe-use guidance, read [docs/safe-use.md](docs/safe-use.md).

## Scope

This repository is documentation only. It contains no Atom Flux runtime source, Ingress Shield service source, deployment rail, credential, endpoint configuration, OAuth configuration, customer data, or operational access material.

## Links

- [WorkFoundry](https://workfoundry.co.uk/)
- [Agent Preflight and Webhook Boundary solution brief](https://workfoundry.co.uk/solution-brief/)
- [WorkFoundry AI-readable overview](https://workfoundry.co.uk/llms.txt)
- [Pilot privacy information](https://workfoundry.co.uk/privacy/)
- Pilot enquiries: [ingress-shield@workfoundry.co.uk](mailto:ingress-shield@workfoundry.co.uk)

WorkFoundry Ltd and workfoundry.co.uk are not affiliated with WorkFoundry.ai.