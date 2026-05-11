---
type: synthesis
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/ideas/2026-05-11-llm-wiki-pattern.md
tags:
  - architecture
  - second-brain
---

# Second Brain Architecture

## Summary

This vault uses a three-layer architecture: immutable raw sources, agent-maintained wiki pages, and a schema that governs every future interaction.

## Layers

- `raw/`: source archive. User and agent can add files; agent must not mutate existing source files without explicit instruction.
- `wiki/`: generated knowledge. Agent owns maintenance and can update pages as understanding improves.
- `AGENTS.md`: operating schema. It defines folder rules, workflows, linking, citations, contradiction handling, and maintenance behavior.

## Navigation Files

- `index.md`: content-oriented map. Read first before queries.
- `log.md`: chronological append-only activity record.

## Current Design Choice

Start simple with markdown, Obsidian links, git history, `index.md`, and `log.md`. Add tools like local search only after scale makes manual index navigation insufficient.

## Links

- [[wiki/concepts/LLM Wiki]]
- [[wiki/concepts/Persistent Synthesis]]
- [[wiki/workflows/Ingest Workflow]]

## Source Notes

- Synthesized from [[wiki/sources/LLM Wiki Pattern]] and `raw/ideas/2026-05-11-llm-wiki-pattern.md`.
