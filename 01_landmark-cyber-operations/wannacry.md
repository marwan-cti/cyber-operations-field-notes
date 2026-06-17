# WannaCry

## Status

Draft v1 — learning case file. To be expanded with deeper source notes and a MITRE ATT&CK mapping.

## How I discovered the topic

I discovered WannaCry through YouTube videos, Wikipedia, MITRE ATT&CK and interviews with security researchers, including material around the researcher who found the kill switch. I also studied the broader context of EternalBlue, MS17-010 and the Shadow Brokers leaks.

For me, WannaCry is not only a ransomware story. It is a case about how a leaked exploit, patching delays, legacy systems, flat networks and accidental defensive discovery can combine into a global incident.

## Why this case matters

WannaCry matters because it turned a known and patched vulnerability into a global crisis. Microsoft had released MS17-010 in March 2017 to address critical SMBv1 vulnerabilities, but many systems remained unpatched when WannaCry began spreading in May 2017.

The case is also important because it shows how offensive tooling can escape its original context. EternalBlue is publicly associated with the Shadow Brokers leak of tools attributed to the NSA-linked Equation Group. Once the exploit became public, it was reused in mass malware. This is one of the central lessons of the case: offensive capability does not remain controlled once it leaks.

## Executive summary

- WannaCry was a ransomware worm first seen in a global attack in May 2017.
- It spread using EternalBlue against vulnerable SMBv1 systems.
- The patch existed before the outbreak, but patch lag, legacy systems and exposed services created systemic risk.
- The kill switch discovered by Marcus Hutchins / MalwareTech slowed the spread, but it did not decrypt already infected machines.
- The case connects ransomware, leaked exploit tooling, vulnerability management, incident response and internet-scale propagation.

## What happened, at a high level

WannaCry encrypted files and demanded payment in Bitcoin. What made it especially disruptive was its worm-like propagation. Instead of relying only on victims opening attachments or running a payload, it could spread across vulnerable Windows systems using SMBv1 exploitation.

MITRE ATT&CK describes WannaCry as ransomware first seen during a global attack in May 2017 that affected more than 150 countries and used EternalBlue for worm-like spreading across networks.

Microsoft had already released MS17-010 on March 14, 2017. That patch corrected vulnerabilities in SMBv1 where specially crafted requests could allow remote code execution. This timing is important: WannaCry was not only a story of an unknown zero-day. It was also a story of organizations failing to apply a critical patch quickly enough.

A major turning point was the discovery of a kill switch. The malware attempted to reach a hard-coded domain. Marcus Hutchins, known as MalwareTech, registered the domain while analyzing the malware. This action caused many samples to stop executing their encryption logic, slowing the outbreak. The defensive lesson is subtle: the kill switch was extremely useful, but it was not a universal fix and did not recover already encrypted files.

## Technical concepts to retain

### Ransomware worm

WannaCry combined ransomware impact with worm-like propagation. This makes it different from traditional ransomware campaigns that depend primarily on phishing or user execution.

### EternalBlue

EternalBlue exploited SMBv1 vulnerabilities addressed by MS17-010. Its reuse in WannaCry shows how leaked offensive tooling can become commodity infrastructure for broader attacks.

### Patch lag

The patch existed before the outbreak. The incident therefore highlights the operational gap between vendor disclosure, patch availability and real deployment across complex environments.

### Kill switch and sinkholing

The kill switch is one of the most memorable parts of the case. It shows how reverse engineering and fast analysis can have direct defensive impact. It also shows why defenders should be careful not to confuse containment with remediation.

### Shadow Brokers context

WannaCry cannot be fully understood without the Shadow Brokers story. The leak of exploitation tooling changed the threat landscape and created a bridge between state-level exploit development and mass criminal or destructive reuse.

## What I want to put forward

The main point I want to show through this note is that I understand WannaCry as a systemic failure, not just as malware.

It is about:

- the reuse of leaked offensive tooling;
- the consequences of slow patch management;
- the danger of exposed or internally reachable legacy protocols;
- the role of individual researchers during live incidents;
- the difference between stopping spread and recovering victims;
- the way a technical vulnerability can become a global operational crisis.

## Defensive relevance

### For CTI (Cyber Threat Intelligence)

For CTI, WannaCry is useful because it connects vulnerability intelligence, exploit availability, actor attribution, malware behavior and operational impact.

A CTI analyst should separate:

- the vulnerability: SMBv1 / MS17-010;
- the exploit: EternalBlue;
- the leak context: Shadow Brokers;
- the malware: WannaCry;
- the attribution discussion;
- the defensive lesson: patching, segmentation and visibility.

### For SOC (Security Operations Center)

For SOC teams, WannaCry shows the need to detect both infection behavior and propagation behavior. Useful monitoring areas include SMB scanning, abnormal service creation, mass file modification, suspicious encryption behavior and attempts to contact known sinkhole or kill-switch domains.

### For vulnerability management

The strongest lesson is patch prioritization. A critical remotely exploitable vulnerability affecting a widely deployed protocol becomes much more urgent when exploit code is public and weaponized.

### For incident response

The kill switch bought time, but did not solve infected systems. The case reinforces the need for backups, asset inventory, emergency patching processes, SMBv1 removal, segmentation and tested recovery plans.

## Analytical caveats

WannaCry is often told as a simple story: “NSA exploit leaked, ransomware hits the world, one researcher stops it.” That story is memorable, but incomplete.

First, the Microsoft patch was already available. The incident therefore cannot be explained only by the existence of EternalBlue.

Second, the kill switch was important, but it did not decrypt systems. Treating it as a miracle fix would be misleading.

Third, attribution should be handled carefully. Public attributions exist, but this note focuses mainly on the defensive and systemic lessons rather than political blame.

## My current assessment

WannaCry is important to my CTI learning because it shows how a single vulnerability can become a global event when exploit availability, poor patching, legacy infrastructure and worm logic converge.

It also shows why CTI must connect technical details to operational reality. Knowing the CVE is not enough. The analyst must understand who can exploit it, whether exploit code is available, how exposed the organization is and what business impact could follow.

## Confidence level

**High** for the broad technical facts: WannaCry used EternalBlue, affected many countries and exploited systems missing MS17-010.

**High** for the defensive lesson around patching, segmentation and SMBv1 exposure.

**Medium** for attribution-related discussion, which depends on public government and vendor statements rather than direct access to classified evidence.

## Sources to prioritize next

- MITRE ATT&CK — WannaCry / S0366: https://attack.mitre.org/software/S0366/
- Microsoft — MS17-010 security bulletin: https://learn.microsoft.com/en-us/security-updates/securitybulletins/2017/ms17-010/
- Microsoft — WannaCrypt ransomware worm targets out-of-date systems: https://www.microsoft.com/security/blog/2017/05/12/wannacrypt-ransomware-worm-targets-out-of-date-systems
- US-CERT / CISA — WannaCry ransomware alert: https://www.cisa.gov/news-events/alerts/2017/05/12/indicators-associated-wannacry-ransomware
- Wired — kill switch reporting around MalwareTech / Marcus Hutchins: https://www.wired.com/2017/05/accidental-kill-switch-slowed-fridays-massive-ransomware-attack/

## Next improvements

- Add a precise timeline from MS17-010 to Shadow Brokers to the May 2017 outbreak.
- Add a short Shadow Brokers cross-reference.
- Map key behaviors to MITRE ATT&CK.
- Add source matrix: Microsoft / MITRE / CISA / researcher interviews / documentaries.
