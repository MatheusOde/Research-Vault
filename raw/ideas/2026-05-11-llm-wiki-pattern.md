# LLM Wiki Pattern

Source type: pasted idea file from user, archived on 2026-05-11.

## Core Idea

Most LLM document workflows use RAG: upload documents, retrieve chunks at query time, and generate answers. This works, but the LLM rediscovers knowledge from scratch each time. Subtle questions requiring synthesis across many documents must be reconstructed repeatedly.

LLM Wiki proposes a different pattern: the LLM incrementally builds and maintains a persistent wiki, a structured interlinked collection of markdown files between the user and raw sources. When a new source arrives, the LLM reads it, extracts key information, integrates it into existing pages, updates entity and concept pages, revises summaries, and flags contradictions.

The wiki is a persistent, compounding artifact. Cross-references, contradictions, and syntheses accumulate. The user curates sources and asks questions; the LLM handles summarizing, cross-referencing, filing, and bookkeeping.

## Example Contexts

- Personal goals, health, psychology, self-improvement, journals, articles, and podcast notes.
- Research projects over weeks or months, with evolving thesis and comprehensive notes.
- Reading books by building pages for characters, themes, plot threads, and connections.
- Business/team internal wiki from Slack threads, meeting transcripts, project docs, and customer calls.
- Competitive analysis, due diligence, trip planning, course notes, and hobby deep-dives.

## Architecture

There are three layers:

- Raw sources: curated source documents. Immutable. Source of truth.
- Wiki: LLM-generated markdown. Agent creates and updates pages, links, summaries, syntheses, and consistency.
- Schema: instructions file such as `AGENTS.md` or `CLAUDE.md` defining structure, conventions, and workflows.

## Operations

Ingest: user adds source, agent reads it, discusses or extracts takeaways, creates source summary, updates index, updates relevant concept/entity pages, and appends log entry.

Query: user asks against wiki. Agent reads index first, searches relevant pages, synthesizes answer with citations, and may file useful answers back into wiki.

Lint: agent periodically health-checks wiki for contradictions, stale claims, orphan pages, missing concept pages, missing cross-references, and data gaps.

## Indexing And Logging

`index.md` is content-oriented catalog of wiki pages with links and one-line summaries. Agent updates it every ingest and reads it first for queries.

`log.md` is chronological append-only record of ingests, queries, and lint passes. Consistent headings make it parseable with simple tools.

## Optional Tools

- Obsidian Web Clipper for saving web articles as markdown.
- Local attachment download into `raw/assets/` for robust image references.
- Obsidian graph view for inspecting link structure.
- Marp for slide decks.
- Dataview for frontmatter queries.
- Git for history, branching, and collaboration.
- `qmd` or another markdown search tool when index becomes insufficient.

## Why It Works

Knowledge bases fail because bookkeeping cost grows: updating cross-references, summaries, contradictions, and consistency. LLMs can do this maintenance cheaply. Human remains responsible for source curation, direction, questions, and judgment.

Related idea: Vannevar Bush's Memex, a personal curated knowledge store with associative trails. LLMs solve the maintenance problem.
