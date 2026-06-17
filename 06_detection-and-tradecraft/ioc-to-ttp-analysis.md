# IOC to TTP analysis

**Type:** CTI tradecraft / detection thinking

## Why it is on my radar

IOC to TTP analysis is one of the concepts that helped me understand the difference between collecting cyber information and thinking like an analyst.

At the beginning, it is easy to focus on hashes, IPs, domains and malware names. But the more interesting question is what those indicators reveal about behavior.

## What stuck with me

An IOC (Indicator of Compromise) is useful, but fragile. A hash or domain can change quickly. A TTP (Tactics, Techniques and Procedures) is often more durable because it describes how the actor behaves.

That shift matters a lot for CTI (Cyber Threat Intelligence): the goal is not just to list artifacts, but to explain what they mean.

## What I take from it

This concept connects CTI with SOC (Security Operations Center) and threat hunting. A good analyst should be able to move from an indicator to a question: what behavior does this represent, what telemetry would show it, and how could we hunt for something similar?

## Current limit

I understand the logic, but I need more practice applying it to real logs, SIEM data and detection rules.

## Resources I actually used

MITRE ATT&CK, threat reports, Sigma/YARA discussions, SOC learning material and TryHackMe-style detection concepts.
