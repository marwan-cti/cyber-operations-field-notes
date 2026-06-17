# IOC to TTP analysis

## Status

Living note — detection and CTI tradecraft.

## Core idea

An IOC (Indicator of Compromise) is useful, but often fragile. TTP (Tactics, Techniques and Procedures) analysis is usually more durable because it focuses on adversary behavior rather than isolated artifacts.

The goal is not to reject IOCs. The goal is to understand what they represent and how to move from static indicators toward behavior-based analysis.

## Why this matters

Many beginner CTI (Cyber Threat Intelligence) workflows start with lists of hashes, IP addresses, domains or URLs.

Those are useful, but attackers can change them quickly. If an analyst stops there, the intelligence may expire fast.

The more important question is: what behavior does the IOC reveal?

## IOC examples

Examples of IOCs include:

- file hashes;
- malicious domains;
- IP addresses;
- URLs;
- registry keys;
- filenames;
- mutexes;
- email sender addresses;
- wallet addresses;
- command-and-control infrastructure;
- YARA matches.

## TTP examples

TTPs describe behavior and method:

- spearphishing;
- credential dumping;
- lateral movement;
- privilege escalation;
- command-and-control;
- data staging;
- exploitation of public-facing applications;
- abuse of legitimate admin tools;
- deployment of wipers or ransomware;
- on-chain laundering patterns after theft.

## How to move from IOC to TTP

A useful workflow:

1. **Identify the IOC** — what artifact was observed?
2. **Ask what behavior it represents** — payload delivery, persistence, C2, exfiltration, staging, laundering?
3. **Map to a technique** — MITRE ATT&CK if relevant.
4. **Determine telemetry** — what logs or sensors would show this behavior?
5. **Assess durability** — can the attacker easily change the indicator?
6. **Build detection or hunting logic** — focus on behavior when possible.
7. **Track confidence** — separate observed fact from analytical inference.

## Example reasoning

A malicious domain by itself is useful for blocking.

But the analytical value increases when I ask:

- Was it used for phishing, C2 (Command and Control), staging or exfiltration?
- Was the domain newly registered?
- Was it typo-squatting a legitimate service?
- Did it host malware or redirect to another infrastructure layer?
- Which users or systems contacted it?
- Does the same actor use similar naming patterns?

This turns an IOC into a behavioral question.

## Defensive relevance

### For CTI

For CTI, IOC-to-TTP thinking improves intelligence quality.

It helps analysts:

- avoid dumping indicators without context;
- explain why an indicator matters;
- assess actor behavior;
- generate detection hypotheses;
- compare campaigns;
- produce more durable reporting.

### For SOC

For SOC (Security Operations Center) teams, IOC-based detection is often useful for immediate blocking and triage.

But TTP-based detection supports:

- threat hunting;
- behavioral analytics;
- detection engineering;
- prioritization;
- incident reconstruction.

### For threat hunting

Threat hunters can use IOCs as starting points, then expand:

- what happened before the IOC appeared?
- what happened after?
- which systems show similar behavior?
- is this a one-off artifact or part of a chain?
- can we hunt for the technique instead of the artifact?

## Caveats

TTPs are more durable than IOCs, but they are not perfect. Broad TTP descriptions can become vague and hard to operationalize.

A good analyst needs both:

- IOCs for speed and specificity;
- TTPs for durability and context.

The tradecraft is knowing when to use each one.

## Sources to prioritize next

- MITRE ATT&CK Enterprise: https://attack.mitre.org/
- Mandiant, Microsoft, Unit 42 and ESET reports that map IOCs to TTPs.
- SigmaHQ for detection logic: https://github.com/SigmaHQ/sigma
- YARA documentation: https://yara.readthedocs.io/
- Florian Roth / Neo23x0 resources: https://github.com/Neo23x0
