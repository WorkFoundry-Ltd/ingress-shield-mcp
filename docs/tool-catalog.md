# Agent Preflight MCP tool catalogue

This is the current public capability catalogue for WorkFoundry Ingress Shield Agent Preflight. Every tool is bounded, account-scoped and read-only. A result is preflight evidence for human review, never permission to execute or alter a system.

After approved secure onboarding, use the MCP client's `tools/list` operation to confirm the live availability and exact argument schema of each tool. This page intentionally does not copy a hard-coded calling schema: the discovered schema is the source of truth for the approved account.

## Current tools

| Tool | What it checks or provides | Boundary |
| --- | --- | --- |
| `atomflux_preflight_tool_graph` | Checks a declared tool graph and returns a deterministic interface seam report. | Read-only compatibility evidence; no calls are made to the declared tools. |
| `atomflux_preflight_lattice` | Analyses an unsigned workflow or Lattice draft and returns a bounded preflight report, or a caller-owned request ID where applicable. | No CCG, fuel reservation, executor work, or workflow action. |
| `atomflux_diff_draft` | Compares two unsigned safe drafts and returns a bounded comparison. | No version is applied, published, or changed. |
| `atomflux_scaffold_draft` | Produces an unsigned proposal starting point. | A proposal only; it creates no authority, workflow, route, or execution. |
| `atomflux_get_status` | Reads bounded status for a caller-owned result or request. | Read-only; it cannot inspect another account's work. |
| `atomflux_explain_status` | Reads a caller-owned corrective explanation for a returned status. | Read-only guidance; it makes no correction or change. |

## Using the catalogue safely

- Before onboarding, do not attempt to connect, authenticate, guess configuration, or invoke a tool.
- Use only a tool and fields returned by `tools/list` for the approved account. If a catalogue name is absent, stop and seek human review.
- Send only the minimum non-sensitive input the discovered schema requires. Never send credentials, personal data, customer data, source code, private URLs, or deployment details.
- Treat all output as advisory evidence for a human decision. Do not automatically deploy, publish, route, execute, or modify anything from a result.

This repository contains no endpoint configuration, credentials, OAuth settings, service source, deployment information, or operational access material.