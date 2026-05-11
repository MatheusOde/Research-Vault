---
type: concept
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/papers/enterprise-integration-erp/Panetto et al. - 2016 - New perspectives for the future interoperable enterprise systems.pdf
  - raw/papers/enterprise-integration-erp/Shen et al. - 2010 - Systems integration and collaboration in architecture, engineering, construction, and facilities man.pdf
  - raw/papers/enterprise-integration-erp/Putrama and Martinek - 2024 - Heterogeneous data integration Challenges and opportunities.pdf
tags:
  - interoperability
  - enterprise-integration
  - data-integration
---

# Enterprise Integration and Interoperability

## Summary
- Interoperability is both data-level and framework/protocol-level ability to exchange, interpret, and use information across heterogeneous systems.
- Next-generation enterprise systems are framed as everything-centric, context-aware, model-driven, open, reconfigurable, cloud-based, cyber-physical, and inherently interoperable.
- AEC/FM integration literature distinguishes data interoperability via common models such as BIM from framework interoperability via communication protocols, web services, agents, and semantic web technologies.
- Heterogeneous data integration still struggles with semantic, structural, syntactic, unstructured-data, privacy, and ontology-evolution issues.

## Details
Panetto et al. move beyond traditional EIS generations toward NG EIS, where people, data, things, and services form interplay networks. They emphasize context awareness, semantic interoperability, cyber-physical systems, cloud-based systems, and interoperability assessment.

Shen et al. review AEC/FM integration as a fragmented lifecycle problem. They distinguish common data models and BIM for data interoperability from web-based systems, distributed objects, agents, web services, semantic web, RFID/wireless sensors, and virtual organizations for collaboration and framework interoperability.

Putrama and Martinek review heterogeneous data integration. Physical integration improves query performance but costs more and can stale; virtual integration avoids replication but is harder under heterogeneity. Ontology and graph approaches dominate, but ontology creation/evolution and unstructured data remain hard.

## Links
- [[wiki/concepts/Enterprise Resource Planning]]
- [[wiki/concepts/Enterprise Modeling for ERP Implementation]]

## Open Questions
- How can semantic interoperability move from manual ontology/schema reconciliation toward trustworthy automation?
- When should enterprise systems prefer physical integration, virtual integration, or hybrid data fabric patterns?

## Source Notes
- `raw/papers/enterprise-integration-erp/Panetto et al. - 2016 - New perspectives for the future interoperable enterprise systems.pdf`: broad position paper; use for research agenda, not validated system performance.
- `raw/papers/enterprise-integration-erp/Shen et al. - 2010 - Systems integration and collaboration in architecture, engineering, construction, and facilities man.pdf`: domain-specific AEC/FM review with transferable interoperability distinctions.
- `raw/papers/enterprise-integration-erp/Putrama and Martinek - 2024 - Heterogeneous data integration Challenges and opportunities.pdf`: recent review; strongest for integration-method taxonomy.
