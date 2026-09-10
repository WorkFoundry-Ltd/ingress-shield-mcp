---
name: ingress-shield-mcp
description: Use the Agent Preflight Ingress Shield MCP as a bounded, account-scoped, read-only compatibility check during an approved external pilot. Do not use it for execution, workflow changes, destination changes, or general data submission.
---

# Ingress Shield MCP

Use this skill only for the Agent Preflight Ingress Shield MCP.

Agent Preflight is a bounded, account-scoped, read-only MCP surface. It provides compatibility and preflight results for human review. It does not grant execution authority, workflow authority, destination authority, or permission to modify any system.

## Availability and onboarding

External pilot access is invite-only and requires secure onboarding.

Before onboarding is complete:

- Do not attempt to connect, authenticate, guess configuration, or invoke tools.
- Do not infer or fabricate endpoint URLs, credentials, OAuth settings, headers, or account identifiers.
- Ask the responsible human to confirm that access has been explicitly approved.

After secure onboarding, discover available capabilities only through the MCP client's standard tools/list operation. Do not guess tool names, parameters, schemas, or capabilities. Use only tools and fields returned by discovery.

If discovery fails, returns no tools, or produces an unexpected schema, stop and request human review.

## Input safety

Send only the minimum bounded, non-sensitive input required by a discovered tool schema and explicitly approved for the current account.

Never send:

- passwords, API keys, access tokens, private keys, signing material, or credentials;
- personal data or customer-identifying information;
- confidential business data, source code, private URLs, private endpoints, or deployment details;
- arbitrary payloads that are not required by the discovered schema.

Do not place secrets or sensitive data in prompts, tool arguments, logs, issue reports, commits, or generated documentation.

## Interpreting results

Treat every response as advisory preflight evidence for human review.

A compatible, valid, or passing result means only that the submitted bounded input matched the reported compatibility checks. It is not:

- permission to execute a workflow;
- permission to change a workflow or configuration;
- permission to change a destination, endpoint, account, or routing policy;
- proof of production readiness, security approval, commercial availability, or domain efficacy.

Do not automatically chain a result into another action. Do not activate, deploy, publish, route, or modify anything based solely on an Agent Preflight result.

Summarize results accurately, preserve uncertainty and failure states, and identify the human decision still required. Use the result only for human review.

## Scope boundary

This skill does not authorize access to Atom Flux runtime services, private infrastructure, deployment rails, vaults, queues, executors, customer systems, or operator workflows. It does not provide instructions for deployment, OAuth configuration, credential handling, or source-code access.

When a request exceeds this read-only preflight scope, stop and explain that human authorization and a separate approved workflow are required.