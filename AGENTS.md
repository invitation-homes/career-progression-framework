# AGENTS.md

This file provides guidance to Coding Agents when working with code in this repository.

## Overview

This is a pure content repository — no build tooling, no dependencies, no tests.
The content represents Invitation Homes' career progression framework for software engineering.

## Structure

When adding or removing a role, three things must be updated:

- [_config.yml](_config.yml) — sidebar navigation
- [index.md](index.md) — Mermaid diagram nodes and `click` directives
- Two files per role: a progression document at the root (`<role>.md`) and a job description in `job-descriptions/<role>.md`

See [ADR-0002](decision-records/0002-one-file-per-role.md), [ADR-0003](decision-records/0003-mermaid-career-ladder.md), and [ADR-0005](decision-records/0005-dual-document-structure.md).

## Content Conventions

Each role document covers five sections in order: **Impact**, **Reach**, **Knowledge**, **Communication**, **Leadership**.
Reach uses a fixed vocabulary and differs between the IC and management tracks.
See [ADR-0004](decision-records/0004-reach-vocabulary.md).

Job descriptions use a four-section structure and follow specific formatting conventions.
See [ADR-0006](decision-records/0006-job-description-format.md).

Content across both documents and both tracks should reflect the seven engineering principles defined in [engineering_principles.md](engineering_principles.md).
When writing or reviewing role content, check that the principles are represented appropriately for the level.

### Front Matter

Every page requires Jekyll front matter with `id` (hyphenated slug) and `title`.
Job description IDs append `-jd` (e.g., `engineering-manager-jd`) to avoid collision with the progression page ID.
See [ADR-0006](decision-records/0006-job-description-format.md) for the full convention.

```yaml
---
id: <role-slug>
title: <Role Title>
---
```

### Links

Omit `.md` extensions from all internal links (see [ADR-0006](decision-records/0006-job-description-format.md)).

### Formatting

See [ADR-0001](decision-records/0001-semantic-line-breaks.md).

## Export

`bin/export-jd` converts job descriptions to `.docx` files using `pandoc` (must be installed: `brew install pandoc`).

```
bin/export-jd <role>              # single role → <role>.docx in current directory
bin/export-jd <role> <output_dir> # single role → specified directory
bin/export-jd all                 # all job descriptions
```

The script strips Jekyll front matter and the trailing `[Progression Document]` back-link from the generated Word output.
Both are present in the source `.md` files for Jekyll rendering purposes but have no meaning in a standalone Word document.
Do not remove the trailing `---` separator from JD files — the export script uses it as a marker for where the exportable body ends.
