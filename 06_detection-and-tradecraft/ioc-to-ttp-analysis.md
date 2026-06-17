# IOC to TTP analysis

## Status

Living note.

## Core idea

An IOC (Indicator of Compromise) is useful, but often fragile. TTP (Tactics, Techniques and Procedures) analysis is usually more durable because it focuses on adversary behavior rather than isolated artifacts.

## Questions to ask

- What behavior does this IOC represent?
- Is the indicator unique, reusable or easily changed?
- Which MITRE ATT&CK technique does the behavior map to?
- What telemetry would confirm or weaken the hypothesis?
- What confidence level is appropriate?

## Defensive relevance

This note supports the transition from consuming threat reports to producing useful CTI and detection hypotheses.
