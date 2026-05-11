---
type: source
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/papers/systems-engineering/Torkjazi and Raz - 2024 - A Review on Integrating Autonomy Into System of Systems Challenges and Research Directions.pdf
tags:
  - systems-engineering
  - system-of-systems
  - autonomy
  - ai-ml
  - emergence
---

# A Review on Integrating Autonomy Into System of Systems: Challenges and Research Directions

## Summary
- Torkjazi and Raz review how AI/ML-enabled autonomous systems become [[wiki/concepts/System of Autonomous Systems|Systems of Autonomous Systems]] when integrated into [[wiki/concepts/System of Systems Engineering|systems of systems]].
- The paper identifies four major SoAS challenge areas: foundation, emergence/safety/performance, architecture/integration, and test/evaluation.
- Level of autonomy (LoA) is treated as a central complexity factor because it affects data exchange, organizational policy, interoperability, safety, operator performance, and SoAS-level emergence.
- Existing SoS, AI/ML, and autonomous systems methods help but do not fully address SoAS because the founding-domain challenges compound across system boundaries.
- Proposed research directions include a shared SoAS ontology/taxonomy, analysis of LoA impacts, MBSE/UAF-based architecting methodology, and improved test/evaluation methods for emergent behavior.

## Details
The paper defines SoAS as a purposefully integrated collection of multiple systems that individually use some form of AI/ML to achieve independent purposes while together enabling capabilities unavailable to any one system alone. This extends SoS by adding autonomy and AI/ML uncertainty to managerially and operationally independent systems.

The four challenges are:
- Foundation: SoAS lacks a consensus taxonomy that distinguishes types by managerial autonomy, operational autonomy, and data exchange/connectivity.
- Emergence, safety, and performance: LoA, AI uncertainty, and system diversity interact to produce desired or undesirable emergent behavior. The literature discusses LoA effects but gives less attention to interacting complexity factors.
- Architecture and integration: LoA affects organizational factors such as policy and agreements, and technical factors such as interoperability, cybersecurity, interfaces, and semantic alignment.
- Test and evaluation: SoAS needs testing strategies that are both comprehensive and efficient; architecture selection methods must account for uncertainty and evolving AI/ML behavior; emergent behavior needs root-cause explanation.

The paper argues that communication protocols and ontologies are complementary. Protocols solve local technical data exchange, while ontologies support shared conceptualization across heterogeneous systems and standards.

## Research Directions
- Build a SoAS taxonomy/ontology that aligns existing SoS, autonomy, and domain-specific standards.
- Update safety standards and analysis practices to include AI/ML failure modes, LoA impacts, organizational policy, and human factors.
- Combine MBSE and architecture frameworks such as UAF with methodology-level guidance for modeling LoA impacts across organizational and technical views.
- Use digital twins, ML, explainable AI, and Bayesian networks to predict, explain, and prevent undesirable SoAS emergent behaviors.

## Links
- [[wiki/concepts/System of Autonomous Systems]]
- [[wiki/concepts/System of Systems Engineering]]

## Source Notes
- `raw/papers/systems-engineering/Torkjazi and Raz - 2024 - A Review on Integrating Autonomy Into System of Systems Challenges and Research Directions.pdf`: PDF text extraction was usable for title, abstract, body, conclusion, and references. Figure/table formatting was degraded; Table 4 and figures should be checked in PDF for exact visual mappings.
- Source strength: high for mapping SoAS challenges and research directions because it reviews 195 papers across SoS, AI/ML, and autonomous systems.
- Uncertainty: conclusions are review-derived and agenda-setting; specific methods such as digital twins plus ML are proposed directions, not established validated practice for all SoAS domains.
