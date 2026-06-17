# NotPetya

## Status

Draft v1 — learning case file.

## How I discovered the topic

I discovered NotPetya through YouTube videos, Wikipedia, MITRE ATT&CK, vendor research and interviews with security teams who analyzed the incident. I also studied the connection with EternalBlue, the Shadow Brokers leak, Ukraine, M.E.Doc and the broader history of destructive malware.

## Why this case matters

NotPetya matters because it looked like ransomware but behaved like a wiper. That distinction is central. If defenders interpret destructive malware as financially motivated ransomware, they may misunderstand the actor’s intent, the recovery expectations and the geopolitical context.

## Executive summary

- NotPetya appeared on June 27, 2017 and was initially confused with Petya-like ransomware.
- MITRE ATT&CK describes it as malware used by Sandworm Team in a worldwide attack beginning on June 27, 2017.
- Although it presented a ransom interface, its main purpose was destructive: data and disk structures were not intended to be recoverable.
- ESET connected the outbreak to supply chain compromise involving Ukrainian accounting software M.E.Doc and the TeleBots activity cluster.
- NotPetya is a key case for understanding wipers, supply chain risk, geopolitical targeting and global collateral damage.

## Technical concepts to retain

- Wiper disguised as ransomware.
- Supply chain compromise.
- M.E.Doc.
- Lateral movement.
- EternalBlue / EternalRomance.
- Collateral damage.
- Attribution and confidence.

## Defensive relevance

For CTI, NotPetya forces the analyst to challenge labels. A ransom note does not necessarily mean ransomware. Analysts need to examine whether payment, decryption and recovery mechanisms are credible.

For SOC teams, NotPetya highlights the need to monitor software update channels, suspicious lateral movement, credential dumping, administrative tool abuse, SMB exploitation and destructive disk activity.

For supply chain security, the case shows that local or sector-specific software can become a strategic infection path.

## Sources to prioritize next

- MITRE ATT&CK — NotPetya / S0368: https://attack.mitre.org/software/S0368/
- Microsoft — Update on Petya malware attacks: https://www.microsoft.com/en-us/msrc/blog/2017/06/update-on-petya-malware-attacks/
- ESET — TeleBots are back: https://www.welivesecurity.com/2017/06/30/telebots-back-supply-chain-attacks-against-ukraine/
- CISA — Petya / NotPetya alert: https://www.cisa.gov/news-events/alerts/2017/07/01/petya-ransomware
