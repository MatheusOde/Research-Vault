---
type: concept
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/ideas/2026-05-11-llm-wiki-pattern.md
tags:
  - llm-wiki
  - second-brain
---

# LLM Wiki

## Summary

LLM Wiki is a second-brain pattern where an LLM maintains a persistent, interlinked markdown wiki over immutable raw sources. The wiki becomes a compounding knowledge artifact instead of a temporary chat answer.

## Core Model

- Human controls source curation, exploration, questions, and judgment.
- Agent controls wiki maintenance: summaries, links, page updates, contradictions, and logs.
- Raw sources remain immutable evidence.
- Generated wiki pages are allowed to evolve as understanding changes.

## Difference From RAG

RAG retrieves relevant chunks at query time. LLM Wiki integrates new knowledge during ingest, then answers from already-structured pages. RAG rediscovers; LLM Wiki accumulates.

## Useful When

- Knowledge accumulates over weeks or months.
- Questions require synthesis across many sources.
- Cross-references and contradictions matter.
- Human wants a browsable artifact in Obsidian, not only chat history.

## Links

- [[wiki/concepts/Persistent Synthesis]]
- [[wiki/workflows/Ingest Workflow]]
- [[wiki/syntheses/Second Brain Architecture]]

## Source Notes

- Derived from [[wiki/sources/LLM Wiki Pattern]] and `raw/ideas/2026-05-11-llm-wiki-pattern.md`.
