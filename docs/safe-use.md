# Safe use of Agent Preflight

## Use it to check before action

Agent Preflight helps an approved AI coding or agent client check a proposed tool chain, API connection, webhook connection, or workflow draft before action. Use it to identify declared compatibility gaps such as missing fields, stranded outputs, mismatched formats, and required explicit adapters.

It is deliberately a read-only preflight surface. A result supports a human decision; it does not make that decision.

## Keep inputs public-safe

Provide only the minimum declared, non-sensitive information that the discovered tool schema requires. Do not send credentials, access tokens, private keys, signing material, personal data, confidential payloads, proprietary source code, private endpoints, or deployment details.

## Do not infer access or configuration

This repository does not publish a live client configuration, endpoint setting, credential, OAuth setting, or shared key. Access is reviewed and invite-only. Use only the exact onboarding information supplied by WorkFoundry after approval.

After onboarding, use the MCP client's tools/list operation to discover the current tool set and schemas. Do not guess tool names or arguments from examples, documentation, or another account.

## Interpret findings correctly

A compatible result means only that the bounded submitted description passed the reported compatibility checks. It does not:

- authorize execution;
- alter a workflow, configuration, destination, or route;
- access secrets or customer systems;
- establish production readiness, a security approval, or an availability commitment.

Record the result accurately, retain its uncertainty, and present the next human decision. If a request falls outside this read-only preflight boundary, stop and seek separate authorisation.

## Related public information

- [WorkFoundry solution brief](https://workfoundry.co.uk/solution-brief/)
- [WorkFoundry pilot privacy information](https://workfoundry.co.uk/privacy/)
- [WorkFoundry AI-readable overview](https://workfoundry.co.uk/llms.txt)