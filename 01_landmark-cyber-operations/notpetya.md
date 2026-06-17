# NotPetya

## Status

Draft v1 — learning case file. To be expanded with deeper source notes, especially ESET, Microsoft, CISA and official attribution statements.

## How I discovered the topic

I discovered NotPetya through YouTube videos, Wikipedia, MITRE ATT&CK, vendor research and interviews with security teams who analyzed the incident. I also studied the connection with EternalBlue, the Shadow Brokers leak, Ukraine, M.E.Doc and the broader history of destructive malware.

For me, NotPetya is one of the clearest examples of why labels matter in CTI: calling it “ransomware” hides the fact that its behavior and impact were closer to destructive sabotage.

## Why this case matters

NotPetya matters because it looked like ransomware but behaved like a wiper. That distinction is central. If defenders interpret destructive malware as financially motivated ransomware, they may misunderstand the actor’s intent, the recovery expectations and the geopolitical context.

The case is also important because it combined several strategic themes:

- a Ukrainian initial target context;
- supply chain compromise through accounting software;
- lateral movement using multiple methods;
- destructive impact disguised behind a ransom note;
- global collateral damage affecting companies far beyond Ukraine.

## Executive summary

- NotPetya appeared on June 27, 2017 and was initially confused with Petya-like ransomware.
- MITRE ATT&CK describes it as malware used by Sandworm Team in a worldwide attack beginning on June 27, 2017.
- Although it presented a ransom interface, its main purpose was destructive: data and disk structures were not intended to be recoverable.
- ESET connected the outbreak to supply chain compromise involving Ukrainian accounting software M.E.Doc and the TeleBots activity cluster.
- NotPetya is a key case for understanding wipers, supply chain risk, geopolitical targeting and global collateral damage.

## What happened, at a high level

NotPetya surfaced in June 2017 as a fast-spreading malware outbreak. It borrowed visual and code elements associated with Petya-like ransomware, but researchers quickly identified that recovery was not realistically intended.

The initial infection vector is widely associated with the compromise of M.E.Doc, a Ukrainian accounting software used by many organizations. ESET reported evidence supporting the theory that attackers had access to the update server of the legitimate software and used it to push malicious updates.

Once inside networks, NotPetya spread through several mechanisms, including exploitation of SMBv1 vulnerabilities such as EternalBlue / EternalRomance and credential-based movement. This combination made it dangerous: even patched systems could be affected if credentials and lateral movement paths were available inside the network.

## Technical concepts to retain

### Wiper disguised as ransomware

The most important concept is that NotPetya was not normal ransomware. The ransom note created ambiguity, but the recovery design made decryption unrealistic. This matters because motive changes the defensive interpretation.

### Supply chain compromise

The M.E.Doc connection is central. A trusted software update channel can become an initial access vector. This creates a defensive problem because victims may execute malicious code through normal, trusted workflows.

### Lateral movement

NotPetya used more than one spreading mechanism. EternalBlue matters, but the case should not be reduced to EternalBlue alone. Credential theft and administrative tools also played a role.

### Collateral damage

NotPetya is a powerful example of how a geopolitically linked operation can escape the original target context and create global business disruption.

### Attribution and confidence

MITRE associates NotPetya with Sandworm Team. Public attribution should still be presented with source awareness: vendor research, government statements and technical evidence do not all carry the same type of proof.

## What I want to put forward

The main thing I want to show through this note is that I understand the difference between ransomware and destructive malware.

NotPetya is important because it shows that:

- attacker intent cannot be read only from the ransom screen;
- technical recovery design matters;
- supply chain compromise can create trusted initial access;
- patching is necessary but not sufficient;
- geopolitical operations can cause global private-sector damage;
- CTI must connect malware behavior, targeting context and strategic intent.

## Defensive relevance

### For CTI (Cyber Threat Intelligence)

For CTI, NotPetya is useful because it forces the analyst to challenge labels. A report that calls something ransomware may still describe a wiper. Analysts need to examine whether payment, decryption and recovery mechanisms are credible.

Key CTI questions:

- Is the malware financially motivated or destructive?
- Does the recovery mechanism actually work?
- What was the initial target geography or sector?
- Is the broader spread intentional or collateral?
- Which parts of attribution are technical, contextual or political?

### For SOC (Security Operations Center)

For SOC teams, NotPetya highlights the need to monitor software update channels, suspicious lateral movement, credential dumping, administrative tool abuse, SMB exploitation and destructive disk activity.

A SOC cannot rely only on perimeter detection. Once a trusted update channel is abused, the malicious activity may begin from systems and processes that appear legitimate.

### For supply chain security

NotPetya is one of the cases that makes supply chain risk concrete. A vendor or software provider does not need to be globally famous to become a systemic risk. Local or sector-specific software can become a strategic infection path.

### For incident response

The case reinforces the need for offline backups, rebuild procedures, privileged access control, network segmentation and crisis communication. If malware is destructive, negotiating or waiting for a decryptor may waste critical time.

## Analytical caveats

NotPetya is often summarized as “the most damaging cyberattack” or “a Russian cyberweapon”. Those framings may be useful shorthand, but they can become too simplistic.

First, the ransomware label is misleading. The destructive behavior matters more than the payment screen.

Second, the Ukrainian context matters, but the global impact also matters. Both should be held together.

Third, EternalBlue is important, but not the full story. Supply chain compromise and credential-based lateral movement are just as central to understanding the incident.

Fourth, attribution should be sourced. A junior analyst should not present geopolitical attribution as personal certainty without showing the basis for confidence.

## My current assessment

NotPetya is important to my CTI learning because it shows how the same technical event can be misread if the analyst relies on surface indicators. A ransom note does not necessarily mean ransomware. A global outbreak does not necessarily mean the whole world was the original target. A known exploit does not explain the entire intrusion chain.

This case is also a strong bridge between my interests in geopolitics, threat actors, supply chain security and defensive analysis.

## Confidence level

**High** for the broad technical assessment that NotPetya behaved as destructive malware / wiper rather than recoverable ransomware.

**High** for the importance of the M.E.Doc supply chain vector, based on vendor and Microsoft reporting.

**Medium-high** for Sandworm / Russian military intelligence attribution in public sources, depending on whether the note relies on MITRE, government statements or vendor reporting.

## Sources to prioritize next

- MITRE ATT&CK — NotPetya / S0368: https://attack.mitre.org/software/S0368/
- Microsoft — Update on Petya malware attacks: https://www.microsoft.com/en-us/msrc/blog/2017/06/update-on-petya-malware-attacks/
- ESET — TeleBots are back: supply-chain attacks against Ukraine: https://www.welivesecurity.com/2017/06/30/telebots-back-supply-chain-attacks-against-ukraine/
- US-CERT / CISA — TA17-181A Petya / NotPetya alert: https://www.cisa.gov/news-events/alerts/2017/07/01/petya-ransomware
- Wired / long-form reporting on NotPetya and EternalBlue context.

## Next improvements

- Add a precise timeline.
- Build a source matrix separating vendor analysis, government attribution and media reporting.
- Add a comparison table: WannaCry vs NotPetya.
- Add cross-reference to the Shadow Brokers note.
