---
type: concept
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/papers/systems-engineering/Torkjazi and Raz - 2024 - A Review on Integrating Autonomy Into System of Systems Challenges and Research Directions.pdf
  - raw/papers/systems-engineering/Nielsen et al. - 2015 - Systems of Systems Engineering Basic Concepts, Model-Based Techniques, and Research Directions.pdf
tags:
  - systems-engineering
  - autonomy
  - ai-ml
  - system-of-systems
---

# System of Autonomous Systems

## Summary
- A System of Autonomous Systems (SoAS) is a system of systems whose constituent systems individually use AI/ML-enabled autonomy while jointly producing SoS-level capabilities.
- SoAS extends [[wiki/concepts/System of Systems Engineering|System of Systems Engineering]] by adding level of autonomy (LoA), AI/ML uncertainty, and autonomous decision-making to existing SoS independence and emergence problems.
- Core challenges are foundation/taxonomy, emergence and safety, architecture and integration, and test and evaluation.
- Ontologies are proposed as a way to align heterogeneous domain standards and create shared conceptualization across autonomous constituents.

## Details
Torkjazi and Raz define SoAS around three founding domains: SoS, AI/ML, and autonomous systems. Their claim is that challenges from these domains do not merely add together; they interact and amplify at SoAS level.

LoA is central. It affects how much data systems need, how they communicate, what policies constrain them, how humans interact with them, and what kinds of emergent behavior appear at SoAS level. High LoA can improve capabilities but may also intensify safety, interoperability, cybersecurity, and explainability problems.

Research needs include a shared SoAS taxonomy/ontology, safety standards that account for AI/ML failure modes, MBSE/UAF-based architecture methodology, and test/evaluation methods that explain root causes of undesirable emergent behavior.

## Links
- [[wiki/sources/A Review on Integrating Autonomy Into System of Systems Challenges and Research Directions]]
- [[wiki/sources/Systems of Systems Engineering Basic Concepts Model-Based Techniques and Research Directions]]
- [[wiki/concepts/System of Systems Engineering]]

## Source Notes
- `raw/papers/systems-engineering/Torkjazi and Raz - 2024 - A Review on Integrating Autonomy Into System of Systems Challenges and Research Directions.pdf`: primary source for SoAS definition, challenges, and research directions.
- `raw/papers/systems-engineering/Nielsen et al. - 2015 - Systems of Systems Engineering Basic Concepts, Model-Based Techniques, and Research Directions.pdf`: background source for SoS dimensions that SoAS extends.
- Confidence: medium-high. The definition and challenge taxonomy are clear in the review, but SoAS is described as a relatively new field requiring further consensus.
