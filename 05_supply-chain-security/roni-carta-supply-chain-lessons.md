# Roni Carta supply chain lessons

## Status

Draft v1 — supply chain security synthesis note.

## Why this matters

Roni Carta's public interviews and work are useful for understanding real-world supply chain security, dependency risk and the practical mindset required to detect or prevent compromise.

This note is not a biography. The person-profile is in the `people-communities-and-researchers` section. This note focuses on the supply chain lessons I take from his work and from Lupin & Holmes / Depi-style research.

## Core idea

Supply chain security is not only about vulnerabilities in code.

It includes:

- package registries;
- dependencies;
- maintainers;
- expired domains;
- CI/CD pipelines;
- build systems;
- developer accounts;
- permissions;
- trust relationships;
- update mechanisms;
- forgotten assets.

Roni Carta's work is interesting because it shows how attackers can look upstream and sideways instead of attacking the front door.

## Why it matters in my cyber culture

I discovered Roni Carta through interviews, conferences, LinkedIn posts and articles. What stood out to me was his passion, creativity and ability to explain supply chain risks through real cases.

His work helped me understand that supply chain attacks are often about imagination: finding the unexpected trust path that an organization forgot existed.

## Key lessons

### 1. Dependencies are trust relationships

A dependency is not just code. It is a relationship with a maintainer, registry, package name, domain, release process and distribution channel.

If one part of that chain is compromised, downstream organizations may be affected without being directly targeted.

### 2. Attackers can abuse abandoned assets

Expired domains, unused package names, forgotten repositories and inactive accounts can become entry points.

This matters because organizations often clean active assets but forget historical trust paths.

### 3. Supply chain attacks may look legitimate

A malicious package update, dependency confusion event or compromised maintainer account may arrive through a trusted mechanism. That makes prevention and detection harder.

### 4. Research can become product thinking

The interesting part of Lupin & Holmes / Depi is the movement from offensive discovery to defensive monitoring: how to identify risky dependencies, trust relationships and exposed supply chain paths before attackers use them.

## Defensive relevance

### For CTI

For CTI (Cyber Threat Intelligence), this topic is useful because supply chain attacks require relationship mapping.

A CTI analyst should ask:

- Which third-party components are critical?
- Which maintainers or packages create concentration risk?
- Which dependencies are unmaintained?
- Which domains or repositories are still trusted but no longer monitored?
- What threat actors are known to abuse software supply chains?
- Which indicators are technical artifacts vs trust-path weaknesses?

### For AppSec and engineering

Engineering teams should think about:

- dependency inventory;
- package allowlisting;
- lockfiles and pinning;
- artifact signing;
- maintainer verification;
- CI/CD hardening;
- dependency confusion prevention;
- secrets scanning;
- expired domain monitoring;
- review of transitive dependencies.

### For SOC

SOC (Security Operations Center) teams should monitor:

- new package installation from unexpected registries;
- unusual build pipeline behavior;
- changes in trusted dependencies;
- suspicious post-install scripts;
- outbound connections from build systems;
- unexpected package maintainer or registry changes;
- alerts from software composition analysis tools.

## Caveats

This note should avoid turning Roni Carta into a hero figure. The useful lesson is the mindset: creative offensive thinking, responsible disclosure and focus on real attack paths.

I should also separate:

- interview narratives;
- company/product positioning;
- technical blog posts;
- independently verifiable evidence;
- my own interpretation.

## Related notes

- [Roni Carta profile](../07_people-communities-and-researchers/roni-carta.md)
- [XZ Utils backdoor](xz-utils-backdoor.md)

## Sources to prioritize next

- Roni Carta — Netflix vulnerability / dependency confusion: https://www.landh.tech/blog/20250610-netflix-vulnerability-dependency-confusion/
- Roni Carta — Hacking millions of companies with $10: https://www.landh.tech/blog/20241107-10-to-hack-millions-of-companies
- Seedcamp — Lupin & Holmes pre-seed and supply chain security: https://seedcamp.com/views/seedcamp-co-leads-lupin-holmes-5-9m-pre-seed-to-defend-against-software-supply-chain-attacks/
- Tronche de Tech — Roni Carta interviews.
- OWASP — Software Component Verification Standard / supply chain references.
- SLSA — Supply-chain Levels for Software Artifacts: https://slsa.dev/
