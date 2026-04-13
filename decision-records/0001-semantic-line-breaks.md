# ADR-0001: Semantic Line Breaks in Markdown

## Status

Accepted

## Date

2026-04-13

## Context

The Markdown files in this repository are prose-heavy content documents.
When written or edited over time, paragraphs and bullet points were broken at arbitrary line widths (typically ~80 characters), a convention inherited from terminal editors and older tooling.

This created inconsistency: some paragraphs were wrapped mid-sentence, others were written as single long lines, and there was no clear rule to follow when adding new content.

We considered three conventions:

**Single line per paragraph** — each paragraph is one long line, letting the editor or renderer wrap as needed.
This is simple and consistent, but git diffs show the entire paragraph as changed when a single word is edited, making reviews harder to read.

**Hard wrap at ~80 characters** — breaks lines at a fixed column limit.
This is a legacy of terminals and older editors.
It makes raw files readable in narrow views, but diffs are noisy and the line breaks feel arbitrary within sentences.

**Semantic line breaks** — one sentence per line.
Each sentence ends with its terminal punctuation, and the next sentence begins on a new line.
The rendered output is identical (Markdown renderers treat these line breaks as spaces within a paragraph), but git diffs become granular: a change to one sentence shows exactly that sentence in the diff, nothing more.

## Decision

Use semantic line breaks throughout all Markdown content files in this repository.

The rules are:

- Each sentence in a prose paragraph ends on its own line.
- Multi-sentence bullet points break at sentence boundaries, with continuation lines indented 2 spaces.
- Single-sentence bullets remain on one line.
- Code blocks, tables, and front matter are not affected.

## Rationale

This repository is a pure content repo with no build step, reviewed via GitHub pull requests.
The primary audience for the raw source is contributors reviewing or editing the content.

Semantic line breaks optimize for that workflow:
- Reviewers see exactly which sentence changed in a PR diff.
- Writers can edit one sentence without reflowing an entire paragraph.
- The rendered output on GitHub Pages is unaffected.

The convention is also self-enforcing: each sentence is a discrete unit, so there is no ambiguity about where to break a line.

## Consequences

- All existing content files were updated to follow this convention when this decision was adopted.
- New content should follow the same convention: one sentence per line in prose paragraphs and multi-sentence bullets.
- Editors that auto-format Markdown (e.g., Prettier with `proseWrap: always`) may reflow lines; contributors should configure their tools to respect the existing line breaks or disable prose wrapping for this repo.
