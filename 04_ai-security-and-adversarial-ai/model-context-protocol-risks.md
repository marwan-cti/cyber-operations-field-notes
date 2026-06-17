# Model Context Protocol risks

## Status

Draft v1 — AI Security / agentic systems note.

## Why this topic matters

MCP (Model Context Protocol) is relevant because it connects AI systems to tools, data sources and workflows. This can expand the attack surface for prompt injection, malicious tools, data exposure and agentic misuse.

The core issue is not that MCP is “bad”. The issue is that protocols which make tool integration easier also make trust boundaries more important.

## Why it matters in my cyber culture

MCP matters to me because it sits exactly at the intersection of AI Security, AppSec (Application Security), CTI (Cyber Threat Intelligence), developer tooling and agentic systems.

A chatbot that only answers questions has limited security impact. An agent connected to repositories, databases, browsers, terminals, ticketing systems or cloud tools creates a much larger risk surface.

That is why MCP is a good topic for a defensive note: it forces the analyst to think about permissions, tool metadata, untrusted context, connector trust, server compromise and monitoring.

## Core attack surfaces

### Tool poisoning

Tool poisoning occurs when tool metadata, descriptions or instructions influence the model’s tool selection or behavior in a malicious way.

The risk is semantic: the model may interpret a tool description as trustworthy guidance, even if it was supplied by an untrusted or compromised server.

### Indirect prompt injection

If an MCP-connected agent retrieves content from external sources, malicious instructions embedded in that content may influence later tool calls or data handling.

### Malicious or compromised MCP servers

An MCP server may be malicious from the beginning, compromised later or updated after trust has been granted. That makes server identity, manifest integrity and permission review important.

### Excessive agency

The more actions an agent can perform, the more severe a prompt injection or tool poisoning event becomes.

An agent with read-only documentation access is different from an agent that can write code, merge pull requests, query production data or run shell commands.

### Logging and investigation gaps

If prompts, retrieved context, tool metadata and tool calls are not logged clearly, incident response becomes difficult.

## Defensive relevance

### For CTI

For CTI, MCP is interesting because it is still an emerging surface. Analysts should distinguish:

- architectural risk;
- research proof-of-concept;
- bug bounty finding;
- vendor advisory;
- field exploitation;
- defensive best practice.

That distinction matters because MCP risk can easily become hype if every theoretical concern is treated as an active campaign.

### For SOC and detection

SOC (Security Operations Center) teams should think about telemetry:

- which MCP servers are connected;
- which tools are available;
- which permissions each tool has;
- which prompts or retrieved contexts preceded tool calls;
- whether tool calls match the user’s intent;
- whether tool metadata changed after approval;
- whether sensitive data was accessed or transmitted.

### For AppSec and AI Security

Defensive controls should include:

- tool allowlisting;
- least privilege permissions;
- signed or pinned tool manifests;
- review of tool descriptions and metadata;
- separation of trusted and untrusted context;
- user confirmation for high-impact actions;
- sandboxing of risky tools;
- audit logs for tool calls;
- monitoring for abnormal tool sequences.

## What I want to put forward

The main point is that MCP risk should not be reduced to “prompt injection but with tools”.

MCP introduces a supply-chain-like problem for AI agents: the model may rely on external tools, metadata, connectors and servers that become part of the trust chain.

## Caveats

MCP is evolving quickly. Some claims may refer to specific SDKs, clients, servers or proof-of-concept setups rather than the protocol as a whole.

A good analysis should identify:

- what component is affected;
- whether the problem is protocol-level or implementation-specific;
- whether the exploit requires user approval;
- whether real systems have been abused;
- what telemetry would confirm exposure.

## Sources to prioritize next

- Official MCP documentation: https://modelcontextprotocol.io/
- Anthropic MCP announcement and documentation.
- OWASP Top 10 for LLM Applications 2025 — excessive agency and prompt injection: https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/
- Model Context Protocol threat modeling and tool poisoning research.
- Recent research on MCP prompt injection, tool poisoning, shadowing and rug-pull style attacks.
- Vendor research from OX Security, Invariant Labs, Trail of Bits, HiddenLayer, or other AI Security teams when relevant.
