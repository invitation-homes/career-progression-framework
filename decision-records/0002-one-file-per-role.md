# ADR-0002: One Markdown File Per Role

## Status

Accepted

## Date

2026-04-13

## Context

The career framework content needs to be organized across multiple roles.
The alternatives considered were:

**Single document** — all roles in one Markdown file, separated by headings.
Simple to maintain, but the file grows unwieldy, any change touches the same file, and there is no way to link directly to an individual role.

**One file per track** — one file for the IC track, one for the management track.
Reduces the number of files, but changes to one role still affect other roles in the same file, and direct linking to a role is not possible.

**One file per role** — each role is its own Markdown file with its own URL.

## Decision

Each role is defined in its own Markdown file at the root of the repository.

## Rationale

- Each role has a stable, direct URL that can be linked from the career ladder diagram, performance conversations, and external references.
- Changes to a single role are isolated in their own pull request diff, making reviews focused and easy to follow.
- Roles can be added, removed, or renamed independently without touching unrelated content.
- The sidebar navigation in `_config.yml` maps cleanly one-to-one with role files.

## Consequences

- The sidebar in `_config.yml` must be updated whenever a role file is added, removed, or renamed.
- The Mermaid diagram in `index.md` must also be updated to add or remove nodes and click directives when roles change.
