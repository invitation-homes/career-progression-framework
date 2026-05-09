# ADR-0003: Mermaid for the Career Ladder Diagram

## Status

Accepted

## Date

2026-04-13

## Context

The overview page needs a visual representation of the career ladder showing how roles relate and progress.
The alternatives considered were:

**Static image (PNG or SVG)** — a diagram exported from a design tool.
Visually flexible, but stored as a binary, not reviewable in diffs, and requires an external tool to update.

**Markdown table** — roles arranged in a table.
Plain text and diff-friendly, but cannot express branching tracks or directional progression clearly.

**ASCII art** — a text-based diagram.
Diff-friendly, but difficult to maintain and renders poorly outside of monospace contexts.

**Mermaid** — a diagram defined in code and rendered by the site theme.
Stored as plain text, fully diff-reviewable, and supports directional flow and clickable nodes.

## Decision

The career ladder is defined as a Mermaid `flowchart` diagram embedded in `index.md`.

## Rationale

- The diagram is stored as plain text, so changes are visible and reviewable in pull request diffs.
- Mermaid's `click` directive allows each node to link directly to the corresponding role page, making the diagram interactive.
- No external tooling or design software is needed to make updates.
- The Jekyll theme used by this site renders Mermaid natively.

## Consequences

- The diagram must be wrapped in `{% raw %}...{% endraw %}` tags to prevent Jekyll's Liquid template engine from interpreting Mermaid's `{}` syntax as template expressions.
- When a role is added or removed, both the diagram nodes and the `click` directives in `index.md` must be updated alongside the role file and `_config.yml`.
- Contributors must be familiar with Mermaid's `flowchart` syntax to make structural changes to the diagram.
