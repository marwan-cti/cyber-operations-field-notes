# WannaCry

## Status

Draft v1 — learning case file.

## How I discovered the topic

I discovered WannaCry through YouTube videos, Wikipedia, MITRE ATT&CK and interviews with security researchers, including material around the researcher who found the kill switch. I also studied the broader context of EternalBlue, MS17-010 and the Shadow Brokers leaks.

## Why this case matters

WannaCry matters because it turned a known and patched vulnerability into a global crisis. Microsoft had released MS17-010 in March 2017 to address critical SMBv1 vulnerabilities, but many systems remained unpatched when WannaCry began spreading in May 2017.

The case also shows how offensive tooling can escape its original context. EternalBlue is publicly associated with the Shadow Brokers leak of tools attributed to NSA-linked / Equation Group capabilities. Once the exploit became public, it was reused in mass malware.

## Executive summary

- WannaCry was a ransomware worm first seen in a global attack in May 2017.
- It spread using EternalBlue against vulnerable SMBv1 systems.
- The patch existed before the outbreak, but patch lag, legacy systems and exposed services created systemic risk.
- The kill switch discovered by Marcus Hutchins / MalwareTech slowed the spread, but it did not decrypt already infected machines.
- The case connects ransomware, leaked exploit tooling, vulnerability management, incident response and internet-scale propagation.

## Technical concepts to retain

- Ransomware worm.
- EternalBlue.
- MS17-010.
- Patch lag.
- Kill switch and sinkholing.
- Shadow Brokers context.

## Defensive relevance

For CTI, WannaCry is useful because it connects vulnerability intelligence, exploit availability, actor attribution, malware behavior and operational impact.

For SOC teams, useful monitoring areas include SMB scanning, abnormal service creation, mass file modification, suspicious encryption behavior and attempts to contact known sinkhole or kill-switch domains.

For vulnerability management, the strongest lesson is patch prioritization. A critical remotely exploitable vulnerability affecting a widely deployed protocol becomes much more urgent when exploit code is public and weaponized.

## Sources to prioritize next

- MITRE ATT&CK — WannaCry / S0366: https://attack.mitre.org/software/S0366/
- Microsoft — MS17-010: https://learn.microsoft.com/en-us/security-updates/securitybulletins/2017/ms17-010/
- Microsoft — WannaCrypt ransomware worm targets out-of-date systems: https://www.microsoft.com/security/blog/2017/05/12/wannacrypt-ransomware-worm-targets-out-of-date-systems
- CISA — WannaCry ransomware alert: https://www.cisa.gov/news-events/alerts/2017/05/12/indicators-associated-wannacry-ransomware
- Wired — kill switch reporting: https://www.wired.com/2017/05/accidental-kill-switch-slowed-fridays-massive-ransomware-attack/
