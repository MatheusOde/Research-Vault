---
type: source
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/ideas/2026-05-11-llm-wiki-pattern.md
tags:
  - llm-wiki
  - second-brain
  - knowledge-management
---

# LLM Wiki Pattern

## Summary

- [[wiki/concepts/LLM Wiki|LLM Wiki]] is a pattern where an LLM maintains a persistent markdown wiki over immutable raw sources.
- Main contrast: conventional RAG retrieves raw chunks at query time; LLM Wiki compiles knowledge into durable, interlinked pages during ingest.
- Value comes from [[wiki/concepts/Persistent Synthesis|Persistent Synthesis]]: summaries, cross-links, contradictions, and higher-level interpretations accumulate over time.
- Human role: curate sources, direct analysis, ask questions, evaluate meaning.
- Agent role: summarize, file, cross-reference, update, lint, and keep pages consistent.

## Key Claims

- Knowledge should be compiled once during ingest, then kept current, not re-derived from raw documents on every query.
- A useful second brain needs both content pages and maintenance routines.
- `index.md` and `log.md` are enough for moderate scale before specialized search tools are needed.
- Obsidian works well as the interface because markdown links, graph view, plugins, and git align with agent edits.

## Architecture Extracted

- Raw source layer: immutable files in `raw/`.
- Wiki layer: generated pages in `wiki/`.
- Schema layer: root `AGENTS.md` defines conventions and workflows.

## Operations Extracted

- Ingest one source at a time when supervision matters.
- Query against `index.md` and wiki pages first, then raw sources if evidence is needed.
- File durable answers back into wiki so chat discoveries compound.
- Lint periodically for contradictions, stale claims, orphan pages, missing links, and research gaps.

## Links

- [[wiki/concepts/LLM Wiki]]
- [[wiki/concepts/Persistent Synthesis]]
- [[wiki/workflows/Ingest Workflow]]
- [[wiki/syntheses/Second Brain Architecture]]

## Source Notes

- Raw source: `raw/ideas/2026-05-11-llm-wiki-pattern.md`.
- Source is conceptual and implementation-agnostic. Current vault schema is one concrete instantiation.
