---
type: workflow
status: active
created: 2026-05-11
updated: 2026-05-11
sources:
  - raw/ideas/2026-05-11-llm-wiki-pattern.md
tags:
  - workflow
  - ingest
---

# Ingest Workflow

Use this when adding one new source.

## Steps

1. Place source in `raw/<category>/` with stable filename.
2. Read source and extract key claims, concepts, entities, tensions, and citations.
3. Create `wiki/sources/<Title>.md` summary with source metadata.
4. Update existing relevant pages in `wiki/concepts/`, `wiki/entities/`, and `wiki/syntheses/`.
5. Create new durable pages only for reusable concepts or entities.
6. Add contradictions or `needs-review` status if source challenges existing claims.
7. Update `index.md`.
8. Append `log.md` entry with `## [YYYY-MM-DD] ingest | Title`.
9. Report changed pages and suggested next questions.

## First Example

The pasted LLM Wiki idea file was archived as `raw/ideas/2026-05-11-llm-wiki-pattern.md`, summarized at [[wiki/sources/LLM Wiki Pattern]], and used to seed [[wiki/concepts/LLM Wiki]], [[wiki/concepts/Persistent Synthesis]], and [[wiki/syntheses/Second Brain Architecture]].
