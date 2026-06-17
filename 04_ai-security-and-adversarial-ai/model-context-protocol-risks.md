# Model Context Protocol risks

**Type:** AI Security / agents / tool-connected systems

## Why it is on my radar

MCP (Model Context Protocol) became interesting to me because it sits at the intersection of AI agents, tools, connectors, prompt injection and supply chain-style trust. It feels like one of the places where AI Security becomes concrete for defenders.

## What stuck with me

What interests me is that MCP is not “dangerous” by itself. The risk comes from what it enables: models connected to tools, files, repositories, databases, browsers or workflows.

Once a model can act through external tools, questions of trust, permissions and logging become much more important.

## What I take from it

MCP helped me think about AI agents as systems, not just models. A prompt injection against a chatbot is one thing. A prompt injection against an agent with access to tools and sensitive data is another.

For CTI (Cyber Threat Intelligence), MCP is interesting because it is still emerging: some risks are architectural, some are research proofs, and some may become real attack paths later.

## Current limit

I have not yet built or audited a full MCP environment myself, so my understanding is still research-oriented.

## Resources I actually used

MCP documentation, AI Security articles, discussions around tool poisoning, indirect prompt injection, agents and my own TAJ research on MCP as an emerging attack surface.
