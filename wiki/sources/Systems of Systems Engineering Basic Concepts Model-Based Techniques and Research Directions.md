---
type: source
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/papers/systems-engineering/Nielsen et al. - 2015 - Systems of Systems Engineering Basic Concepts, Model-Based Techniques, and Research Directions.pdf
tags:
  - systems-engineering
  - system-of-systems
  - model-based-systems-engineering
---

# Systems of Systems Engineering: Basic Concepts, Model-Based Techniques, and Research Directions

## Summary
- Nielsen et al. survey system-of-systems (SoS) definitions, classifications, applications, and model-based engineering techniques.
- They treat [[wiki/concepts/System of Systems Engineering|System of Systems Engineering]] as a systems engineering subfield focused on independent, distributed, evolving constituent systems and stakeholder boundaries.
- The paper proposes eight SoS dimensions useful for model-based analysis: autonomy, independence, distribution, evolution, dynamic reconfiguration, emergence, interdependence, and interoperability.
- Model-based SoS work is organized around modelling/architecture, simulation, testing, and verification.
- The main research gap is not a single missing tool but weak integration across heterogeneous models, evolving architectures, emergent behavior analysis, and SoS-level test objectives.

## Details
The paper grounds SoS in multiple historical traditions and notes that definitions vary by community. Maier's OMGEE characteristics and Boardman and Sauser's ABCDE characteristics are central reference points, but the survey argues that a dimensional view better supports engineering analysis than a single rigid definition.

The eight dimensions function as an analysis lens:
- Autonomy: constituent behavior governed by its own rules.
- Independence: constituents remain useful outside the SoS.
- Distribution: constituents communicate across geographic, network, or organizational distance.
- Evolution: the SoS changes over time through planned or environmental changes.
- Dynamic reconfiguration: the SoS changes structure during operation.
- Emergence: SoS-level behavior arises from constituent interaction.
- Interdependence: constituents depend on one another to satisfy SoS goals.
- Interoperability: heterogeneous systems integrate through interfaces, protocols, standards, and semantic consistency.

For model-based engineering, the paper emphasizes that SoS models must handle partial information, hidden constituent behavior, evolving interfaces, dynamic architectures, and properties that only make sense at SoS level. This links directly to [[wiki/concepts/System of Autonomous Systems|System of Autonomous Systems]], where autonomy and emergence are intensified by AI/ML uncertainty.

## Research Gaps
- General-purpose model languages and tooling for SoS remain limited; many approaches use application-specific notations.
- Verification of SoS is immature, especially for evolution, dynamic reconfiguration, emergence, and heterogeneity.
- Testing needs clearer SoS-level objectives, including test objectives for emergent properties rather than only constituent conformance.
- Simulation needs better support for human-in-the-loop behavior, heterogeneous co-simulation, evolving semantics, and communication faults.

## Links
- [[wiki/concepts/System of Systems Engineering]]
- [[wiki/concepts/System of Autonomous Systems]]

## Source Notes
- `raw/papers/systems-engineering/Nielsen et al. - 2015 - Systems of Systems Engineering Basic Concepts, Model-Based Techniques, and Research Directions.pdf`: PDF text extraction was usable for title, abstract, body, tables, and references. Some table formatting was degraded, especially matrix-style tables.
- Source strength: high for definitions, dimensions, and research agenda because it is a broad ACM Computing Surveys review.
- Uncertainty: extracted table alignment may be imperfect; rely on body text over table cell positions when exact table mapping matters.
