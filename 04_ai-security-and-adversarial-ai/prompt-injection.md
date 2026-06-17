# Prompt injection

## Status

Draft v1 — AI Security learning note.

## Why this topic matters

Prompt injection is a core AI Security issue because it targets the instruction-following behavior of language models and becomes more serious when models can use tools, retrieve data or interact with external systems.

The key problem is that language models process trusted instructions and untrusted content through the same language channel. If an application retrieves emails, web pages, documents, tickets, code or tool descriptions, malicious instructions hidden in that content may influence the model’s behavior.

## Why it matters in my cyber culture

Prompt injection matters to me because it is one of the clearest examples of how AI Security differs from classic application security.

In classic web security, input validation, access control and code execution boundaries are easier to reason about. With LLM applications, the “input” is semantic. A malicious instruction can be embedded in natural language, Markdown, HTML, code comments, documents, screenshots or retrieved context.

This is especially relevant to my CTI (Cyber Threat Intelligence) and AI Security direction because prompt injection becomes much more dangerous when the model can act: read files, call APIs, summarize private data, send messages, query databases or operate tools.

## Core concepts

### Direct prompt injection

Direct prompt injection happens when the user directly sends adversarial instructions to the model or application.

This is the easiest form to understand, but not always the most dangerous in enterprise environments because the user is visible and the interaction is direct.

### Indirect prompt injection

Indirect prompt injection is more interesting defensively. It occurs when malicious instructions are hidden in content the model retrieves or processes: a website, email, PDF, ticket, repository file, calendar invite, documentation page or third-party data source.

The user may not see the malicious instruction, and the model may treat it as part of the task context.

### Tool-connected risk

Prompt injection becomes more serious when the model can use tools. If an attacker can influence the model’s tool choices, they may attempt to cause data exposure, unauthorized actions or workflow manipulation.

This is why prompt injection should be studied together with excessive agency, tool permissions, logging, human approval and MCP (Model Context Protocol) style integrations.

## Defensive relevance

### For CTI

For CTI, prompt injection is useful because it is not only a vulnerability class; it is also an emerging abuse pattern.

A CTI analyst should track:

- whether attacks are theoretical, experimental or observed in the field;
- which systems are targeted: chatbots, agents, coding assistants, RAG systems or tool-connected workflows;
- what the attacker tries to achieve: data exposure, tool misuse, policy bypass, phishing support or persistence in retrieved content;
- whether evidence comes from research papers, red team reports, bug bounty findings, vendor telemetry or real incidents.

### For SOC and detection

For SOC (Security Operations Center) teams, prompt injection is difficult because the payload may look like normal text.

Useful detection questions include:

- Is the model accessing unusual data after processing untrusted content?
- Are tool calls inconsistent with the user’s original intent?
- Are retrieved documents containing instruction-like text?
- Are high-risk actions being triggered without human approval?
- Are prompts, retrieved context and tool calls logged enough for investigation?

### For AppSec and AI Security

Defenses should focus less on “perfect prompt wording” and more on system design:

- least privilege for tools;
- separation of trusted and untrusted context;
- human approval for high-impact actions;
- clear data access boundaries;
- output validation;
- tool-call monitoring;
- prompt and context logging;
- evaluation against indirect prompt injection benchmarks.

## What I want to put forward

The main point is that prompt injection is not just “making the chatbot say something weird”.

The serious risk appears when a model is embedded inside a product, connected to data and allowed to act. In that environment, prompt injection becomes a way to confuse trust boundaries.

## Caveats

Prompt injection is heavily hyped. I should avoid treating every jailbreak screenshot as a security incident.

A useful note must distinguish:

- model behavior failures;
- policy bypass;
- data exposure;
- tool misuse;
- actual unauthorized action;
- experimental proof-of-concept;
- observed field abuse.

## Sources to prioritize next

- OWASP Top 10 for LLM Applications 2025 — LLM01 Prompt Injection: https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/
- NCSC — Prompt injection attacks against LLMs: https://www.ncsc.gov.uk/blog-post/prompt-injection-attacks-against-llms
- MITRE ATLAS — AI attack techniques and case studies: https://atlas.mitre.org/
- AgentDojo benchmark and indirect prompt injection research.
- Greshake et al. — Not what you’ve signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection.
- Recent research on indirect prompt injection against agents and coding assistants.
