# Why crypto matters for CTI

## Status

Draft v1 — domain framing note.

## Core idea

Crypto matters for Cyber Threat Intelligence (CTI) because it connects technical compromise, financial infrastructure, laundering behavior, social engineering and geopolitical incentives.

Crypto is not only a market topic. From a CTI perspective, it is an operational environment where attackers steal, move, hide, launder and sometimes monetize funds in ways that can be partially observed through public ledgers.

## Why this matters in my cyber culture

Crypto threat intelligence matters to me because it connects several interests:

- hacks and technical compromise;
- OSINT (Open Source Intelligence);
- scam exposure;
- on-chain tracing;
- North Korean / DPRK-linked operations;
- sanctions and laundering;
- social engineering;
- bridge and exchange security;
- public-private incident response.

It also helps me connect my earlier crypto/web3 experience with my current CTI learning path.

## Why crypto is a CTI domain

### 1. The money trail is partly visible

Blockchains can expose fund movement, wallet interactions, swaps, bridges and mixer usage.

That does not make attribution automatic, but it gives analysts a type of telemetry that does not exist in the same way for traditional bank fraud.

### 2. Crypto attacks are hybrid

A crypto incident may involve:

- phishing;
- fake job offers;
- malware;
- smart contract bugs;
- bridge design flaws;
- signing workflow compromise;
- cloud or endpoint compromise;
- insider risk;
- wallet governance failure;
- laundering and sanctions exposure.

### 3. State-linked actors use crypto

DPRK-linked actors such as Lazarus Group show that crypto theft can serve strategic financing objectives, not only individual criminal profit.

### 4. Independent investigators matter

Researchers like ZachXBT show that community-driven investigations can influence public awareness, exchange response and victim support.

### 5. Attribution is layered

Crypto investigations require separating:

- wallet movement;
- clustering;
- platform attribution;
- social identity correlation;
- malware or infrastructure links;
- law enforcement confirmation;
- sanctions designation;
- public speculation.

## Defensive value

Crypto investigations help develop:

- source evaluation;
- timeline reconstruction;
- attribution caution;
- OSINT skills;
- evidence chaining;
- financial threat infrastructure awareness;
- understanding of laundering behavior;
- incident response coordination.

## Relevance for CTI

A CTI analyst working on crypto-related threats should ask:

- What was compromised: smart contract, bridge, wallet, signer, endpoint, identity or workflow?
- How did the attacker gain trust or access?
- Where did funds move after the theft?
- Which evidence is on-chain and which evidence is off-chain?
- Are there links to known actor clusters?
- What confidence level is appropriate?
- What can defenders do before the funds move?

## Relevance for SOC and security teams

For crypto organizations, security needs to connect traditional and blockchain-specific telemetry:

- endpoint logs;
- identity and access logs;
- cloud logs;
- CI/CD activity;
- wallet signing events;
- transaction simulation;
- bridge withdrawal patterns;
- on-chain monitoring;
- exchange and law enforcement coordination.

For non-crypto organizations, crypto still matters because attackers may use crypto for ransom payments, laundering, fraud, fake investment schemes, DPRK IT worker operations or sanctions evasion.

## Caveats

Blockchain transparency can create false confidence.

Seeing funds move does not automatically reveal who controls them. Attribution still requires correlation with technical, behavioral, social, legal or governmental evidence.

Crypto threat intelligence should avoid hype and moral panic. The goal is not to say “crypto is bad”. The goal is to understand how adversaries use crypto rails and how defenders can respond.

## Related notes

- [ZachXBT and on-chain investigations](zachxbt-and-on-chain-investigations.md)
- [Ronin Bridge hack](ronin-bridge-hack.md)
- [Bybit hack](bybit-hack.md)
- [Lazarus and crypto operations](lazarus-and-crypto-operations.md)

## Sources to prioritize next

- Chainalysis Crypto Crime Reports.
- TRM Labs reports on DPRK and crypto crime.
- Elliptic reports on crypto laundering.
- FBI and Treasury attribution / sanctions statements.
- MITRE ATT&CK — Lazarus Group: https://attack.mitre.org/groups/G0032/
- ZachXBT public investigations.
