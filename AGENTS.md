# LLM Wiki Agent Schema

This vault is an LLM-maintained second brain. Human curates sources, asks questions, checks meaning. Agent maintains wiki.

## Prime Directive

From now on, every interaction follows this schema unless user says otherwise.

- Treat `raw/` as immutable source of truth. Read from it. Never edit source files after ingest except when user explicitly asks to correct the source archive.
- Treat `wiki/` as agent-owned generated knowledge. Create, revise, link, split, merge, and prune pages as needed.
- Keep `index.md` current after every ingest, query page, lint pass, or structural wiki change.
- Append to `log.md` after every ingest, query, lint pass, or maintenance operation.
- Prefer small, accurate updates over broad rewrites.
- Preserve uncertainty. Mark weak claims as tentative. Do not invent citations.
- When new evidence contradicts old wiki claims, update affected pages and add a contradiction note with source links.
- Use Obsidian wikilinks for internal references: `[[wiki/concepts/LLM Wiki|LLM Wiki]]` or `[[wiki/concepts/LLM Wiki]]`.
- Cite sources with links to `raw/` and source summary pages in `wiki/sources/`.

## Folder Conventions

```text
raw/
  ideas/          Immutable idea files, notes, clipped articles, transcripts.
  papers/         PDFs or paper markdown exports.
  books/          Book notes, chapter files, excerpts.
  web/            Web clips.
  data/           CSV, JSON, datasets.
  assets/         Downloaded images and attachments.

wiki/
  sources/        One generated summary page per raw source.
  concepts/       Reusable ideas, theories, patterns, mechanisms.
  entities/       People, orgs, projects, places, tools.
  syntheses/      Higher-level arguments, overviews, maps, theses.
  questions/      Durable answers to user questions worth preserving.
  workflows/      How-to pages for recurring wiki operations.
  meta/           Wiki health, open questions, controlled vocabulary.

index.md          Content catalog and navigation map.
log.md            Append-only chronological activity record.
AGENTS.md         This schema.
README.md         Human-facing vault overview.
```

## Page Format

Use YAML frontmatter for generated wiki pages:

```yaml
---
type: concept | entity | source | synthesis | question | workflow | meta
status: seed | active | needs-review | superseded
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources:
  - raw/path/to/source.md
tags:
  - tag-name
---
```

Then use this body shape when useful:

```markdown
# Page Title

## Summary
1-5 bullets with core claims.

## Details
Structured notes, claims, evidence, distinctions.

## Links
- [[wiki/concepts/Related Concept]]

## Source Notes
- `raw/...`: exact support or caveat.

## Open Questions
- Question still unresolved.
```

Do not force all headings if page is small. Keep pages useful, not ceremonial.

## Ingest Workflow

When user adds or pastes a source and asks ingest:

1. Archive source under `raw/<category>/` if not already present.
2. Read source fully enough to extract claims, entities, concepts, conflicts, and useful quotes.
3. Create or update one `wiki/sources/<source-title>.md` summary.
4. Update existing concept/entity/synthesis pages touched by source.
5. Create new concept/entity pages only when concept is likely reusable.
6. Add contradictions, confirmations, and source-strength notes where relevant.
7. Update `index.md` with new/changed pages.
8. Append `log.md` entry with prefix `## [YYYY-MM-DD] ingest | Title`.
9. Tell user what changed and what to inspect next.

## Query Workflow

When user asks a question:

1. Read `index.md` first.
2. Search/read relevant `wiki/` pages and, when needed, supporting `raw/` sources.
3. Answer from wiki state with citations to wiki pages and raw sources.
4. If answer is durable, ask or infer whether to file it under `wiki/questions/` or `wiki/syntheses/`.
5. If filing, update `index.md` and append `log.md` with prefix `## [YYYY-MM-DD] query | Question`.

## Lint Workflow

When user asks for wiki health check:

1. Find orphan pages, stale pages, missing backlinks, duplicate concepts, weak claims, contradictions, and pages without sources.
2. Suggest new pages, source gaps, and research questions.
3. Make safe maintenance edits unless user asks for report-only.
4. Update `wiki/meta/wiki-health.md`, `index.md`, and `log.md`.

## Source Rules

- `raw/` files are immutable evidence, not drafts.
- If source is pasted in chat, save it with date plus slug under best `raw/` subfolder.
- If source has images, keep image paths local under `raw/assets/` when available.
- Never delete raw sources unless user explicitly requests deletion.

## Linking Rules

- Every generated page should link to at least one other generated page unless intentionally standalone.
- Prefer specific links over broad links.
- Add backlinks when a page becomes central to another page.
- Use aliases when page paths are long or title differs from sentence flow.

## Citation Rules

- Support factual claims with source page and raw source references.
- For synthesis pages, cite the strongest source pages, not every source.
- If claim comes from agent reasoning across sources, label it as synthesis.
- If evidence is weak, write `Confidence: low` or `Needs source`.

## Contradiction Rules

When new source conflicts with old wiki content:

- Do not hide conflict.
- Add `## Tensions / Contradictions` to affected pages.
- State old claim, new claim, sources, and current best interpretation.
- Mark page `status: needs-review` if conflict affects core conclusion.

## Naming Rules

- Use Title Case for wiki page filenames: `Persistent Synthesis.md`.
- Use lowercase category folders.
- Use descriptive raw filenames with date when source lacks stable title: `2026-05-11-llm-wiki-pattern.md`.
- Avoid duplicate pages. Update existing page when topic already exists.

## Interaction Rules

- Be terse and direct.
- Prefer doing the wiki work over describing hypothetical process.
- Ask one short clarifying question only when needed to avoid wrong structure or destructive change.
- After edits, report changed files and next recommended ingest.

## Maintenance Rules

- Keep `index.md` concise but complete.
- Keep `log.md` append-only; never rewrite old entries except typo fix requested by user.
- Do not over-create pages. A source can update many pages, but only durable concepts deserve pages.
- Git tracks history. Do not add separate changelog unless user asks.
