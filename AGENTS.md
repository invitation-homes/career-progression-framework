# AGENTS.md

This file provides guidance to Coding Agents when working with code in this repository.

## Overview

This is a pure content repository — no build tooling, no dependencies, no tests. It is a Jekyll site published to GitHub Pages at https://invitation-homes.github.io/career-progression-framework/ using a remote theme defined in [_config.yml](_config.yml).

The content of the site represents Invitation Homes career progression framework for software engineering.

## Structure

- [index.md](index.md) — Overview page with a Mermaid career ladder diagram and definitions of the five competency areas (Impact, Reach, Knowledge, Communication, Leadership)
- One Markdown file per role (e.g. [software_engineer_I.md](software_engineer_I.md), [staff_engineer.md](staff_engineer.md))
- [_config.yml](_config.yml) — Jekyll config; controls the sidebar navigation order and titles
- [decision-records/](decision-records/) — ADRs documenting content and formatting decisions for this repository

Each role file uses Jekyll front matter with `id` and `title` fields. The sidebar in `_config.yml` must be updated whenever a new role file is added or a title changes.

## Career Tracks

- **Professional (IC) Track:** SE I → SE II → SE III → SE IV / Salesforce Platform Manager → Staff Engineer → Principal Engineer → Sr. Principal Engineer → Tech Fellow
- **Management Track:** SE IV → Engineering Manager → Senior Engineering Manager → Director of Engineering → Sr. Director of Engineering → VP of Engineering

## Content Conventions

Each role document covers five sections in order: **Impact**, **Reach**, **Knowledge**, **Communication**, **Leadership**. Reach uses a fixed vocabulary: Self → Individual → Team → Cross-Team → Department → Company → Industry (each level is inclusive of prior levels).

The Mermaid diagram in [index.md](index.md) is wrapped in `{% raw %}...{% endraw %}` tags — required by Jekyll to avoid Liquid template conflicts with the Mermaid syntax.

### Formatting

See [ADR-0001](decision-records/0001-semantic-line-breaks.md).

## Publishing

Merging to `main` automatically deploys via GitHub Pages. There is no local build step. The `@invitation-homes/engineering-maintainers` team owns all files (see [.github/CODEOWNERS](.github/CODEOWNERS)).
