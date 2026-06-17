# Pliny the Liberator

## Status

Draft v1 — person / ecosystem profile.

## How I discovered him

I first heard Pliny the Liberator mentioned during a DEF CON-related conference context, then encountered the name again through interviews and discussions involving Jason Haddix and the AI security / red team community.

What caught my attention was not only the persona, but the fact that jailbreak culture has become visible enough to be discussed by experienced offensive security practitioners. That makes Pliny relevant to study as an ecosystem signal, not as a source of techniques to copy.

## Why this person / persona matters

Pliny the Liberator is relevant as a visible figure in AI jailbreak culture and adversarial prompt experimentation.

For my learning, the important point is not to reproduce jailbreak prompts. The important point is that figures like Pliny show how quickly communities test model boundaries, challenge safety claims and turn new releases into adversarial experimentation targets.

This matters for AI Security because public model behavior, guardrail bypass claims and jailbreak communities create signals defenders should observe carefully: what techniques are discussed, what model capabilities are targeted, which claims are exaggerated, and how fast new methods spread.

## Area

- AI jailbreak culture.
- Adversarial prompting.
- AI red teaming communities.
- Model safety discourse.
- Public testing of frontier and open-weight models.
- Ecosystem monitoring for AI Security and CTI.

## What I learned from following this topic

- AI security is not only a vendor/model problem; it is also a community and ecosystem problem.
- New model releases are quickly tested by adversarial communities.
- Public claims of “jailbreak” need careful validation: a bypass, a refusal failure, system prompt extraction and harmful task completion are not always the same thing.
- Guardrails and model-level safety are only one layer; tool access, permissions, logging, product design and workflow boundaries matter just as much.
- Studying jailbreak culture can be defensively useful if the goal is to understand risk signals, not to operationalize misuse.

## Relevance for CTI

For CTI (Cyber Threat Intelligence), Pliny is useful as a case study in emerging adversarial AI culture.

A CTI analyst should ask:

- Who is making the claim?
- What was actually demonstrated?
- Was the output harmful, merely policy-violating, or only framed as a jailbreak?
- Is the evidence reproducible or just screenshots / social media claims?
- Does the claim affect a standalone model, an AI product, or an agentic system with tools?
- What would matter defensively for an organization using similar systems?

This connects directly to AI Security because defenders need to separate hype from real exposure. A spectacular jailbreak claim is less important than whether a model has access to sensitive data, tools, credentials, internal systems or automated decision workflows.

## Caveats

This profile is not intended to reproduce jailbreak instructions, prompt templates or bypass methods.

The Pliny ecosystem is partly documented through podcasts, social media, secondary reporting and community sources. That means the evidence quality varies. I should treat this as an object of ecosystem observation, not as a fully verified technical authority.

I should also avoid adopting the ideology or framing of the community uncritically. Terms like “liberation”, “safety theater” or “uncensored AI” are part of a narrative. A defensive analyst should observe the narrative without automatically accepting it.

## Sources to prioritize next

- Latent Space — Jailbreaking AGI: Pliny the Liberator & John V on Red Teaming, BT6, and the Future of AI Security: https://www.youtube.com/watch?v=lFbAr2IPK9Q
- TechBriefly — Pliny jailbreaks OpenAI's GPT-OSS models: https://techbriefly.com/2025/08/07/pliny-jailbreaks-openais-gpt-oss-120b-models/
- OpenAI — gpt-oss-120b & gpt-oss-20b model card: https://arxiv.org/abs/2508.10925
- Red Teaming AI Red Teaming: https://arxiv.org/abs/2507.05538
- Red-Teaming for Generative AI: Silver Bullet or Security Theater?: https://arxiv.org/abs/2401.15897
