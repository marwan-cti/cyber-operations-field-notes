# Lazarus Group

## Status

Draft v1 — threat actor profile.

## Why this actor matters

Lazarus Group is important for studying the overlap between state-linked operations, financial theft, crypto targeting, espionage, destructive malware and sanctions-driven strategic objectives.

MITRE ATT&CK describes Lazarus Group as a North Korean state-sponsored cyber threat group attributed to the Reconnaissance General Bureau (RGB), active since at least 2009. MITRE also notes that public reporting often uses “Lazarus Group” as an umbrella term for multiple North Korean cyber operators conducting espionage, destructive attacks and financially motivated campaigns.

That caveat is central: Lazarus is not always a precise single team label. It can be a broad public label covering several clusters, sub-groups and campaign names.

## Why this actor matters in my cyber culture

Lazarus matters to me because it connects several domains I care about:

- APT (Advanced Persistent Threat) activity;
- North Korean state strategy;
- destructive operations such as Sony Pictures;
- crypto theft and laundering;
- social engineering;
- developer targeting;
- sanctions evasion;
- attribution complexity.

It is one of the best examples of how CTI (Cyber Threat Intelligence) cannot be limited to malware names. To understand Lazarus, the analyst has to connect geopolitics, finance, infrastructure, malware, recruitment lures, blockchain tracing and public attribution.

## Area

- State-sponsored cyber operations.
- Crypto theft and laundering.
- Espionage.
- Destructive malware.
- Social engineering.
- Developer and exchange targeting.
- Sanctions evasion and strategic financing.

## Key cases to connect later

- Sony Pictures / Guardians of Peace.
- Bangladesh Bank cyber heist.
- WannaCry attribution discussions.
- Ronin Bridge / Axie Infinity.
- Bybit and other high-value crypto incidents if publicly attributed or suspected.
- Developer-targeting campaigns against crypto and technology workers.

## What I learned from this actor

- State-linked actors can use cybercriminal methods when it serves strategic objectives.
- Crypto is not only a financial topic; it is a national security and threat intelligence topic.
- Attribution can be difficult when umbrella labels hide sub-groups and shared infrastructure.
- Social engineering remains central even in highly technical operations.
- Financial flows can become part of CTI when blockchain tracing, sanctions and exchange behavior are involved.

## Relevance for CTI

For CTI, Lazarus is useful because it forces analysis across several evidence types:

- malware and infrastructure indicators;
- TTP (Tactics, Techniques and Procedures) overlap;
- targeting patterns;
- blockchain flows;
- government sanctions and advisories;
- vendor naming conventions;
- geopolitical context.

A CTI analyst should ask:

- Is “Lazarus” being used as a precise actor label or an umbrella term?
- Which sub-cluster or campaign name is being discussed?
- What evidence supports the attribution?
- Are we dealing with espionage, theft, sabotage or a hybrid objective?
- What can defenders monitor or harden based on the report?

## Defensive relevance

For SOC (Security Operations Center) and security teams, Lazarus-linked activity is relevant to:

- phishing and recruitment-themed lures;
- malware delivery through fake job offers or developer tooling;
- credential theft;
- crypto wallet and exchange compromise;
- suspicious blockchain movement after theft;
- infrastructure reuse;
- endpoint detection and network telemetry around known toolchains.

For crypto organizations, the actor is especially important because compromise may begin through human trust, hiring processes, developer machines or privileged wallet operations rather than obvious perimeter exploitation.

## Caveats

This profile should avoid treating Lazarus as a monolithic cartoon villain.

North Korean cyber operations are complex, and public labels vary across vendors. The term “Lazarus Group” may refer to different activity clusters depending on the source.

Attribution should be handled with care, especially when connecting crypto incidents to state sponsorship. Blockchain tracing can show fund movement; it does not automatically prove who controlled every step without additional evidence.

## Sources to prioritize next

- MITRE ATT&CK — Lazarus Group / G0032: https://attack.mitre.org/groups/G0032/
- CISA — HIDDEN COBRA / North Korea advisories.
- US Treasury sanctions notices on North Korean cyber groups.
- Mandiant / Google Cloud research on DPRK cyber structure.
- Chainalysis and TRM Labs reports on DPRK crypto theft and laundering.
- Ronin Bridge official postmortems and US attribution statements.
