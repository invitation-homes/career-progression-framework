# ADR-0004: Fixed Reach Vocabulary

## Status

Accepted

## Date

2026-04-13

## Context

Each role in the framework needs to express the scope of its impact — how widely a person in that role is expected to influence the organization.
The alternatives considered were:

**Free-form descriptions** — each role describes its scope in its own words.
Flexible, but makes it difficult to compare roles or see clear progression, and gives no guidance to contributors writing new content.

**Numeric levels** — a scale from 1 to N.
Structured, but abstract and not meaningful on its own without a legend.

**Fixed enumerated vocabulary** — a predefined, ordered set of named scopes.
Each role selects from the same set of values, making progression explicit and comparable across all roles.

## Decision

Reach uses a fixed, ordered vocabulary:

**Self → Individual → Team → Cross-Team → Department → Company → Industry**

Each level is inclusive of the levels that precede it.

The framework has two career tracks:

- **IC track** — Software Engineer I through Tech Fellow.
  Each role declares a single Reach value.
- **Management track** — Engineering Manager through VP of Engineering.
  Each role declares two Reach values: **Leadership Reach** (the scope of direct people leadership) and **Technical Reach** (the scope of technical influence), because these two dimensions often differ for managers.

## Rationale

- A shared vocabulary makes the progression of scope explicit and easy to compare across roles.
- Contributors and agents adding or editing roles have a concrete, bounded set of values to choose from, reducing ambiguity.
- The inclusive definition (each level encompasses all prior levels) reflects how real-world influence grows; it avoids implying that senior roles stop operating at earlier levels.
- Management roles warrant two dimensions because an Engineering Manager's direct leadership scope (their team) is meaningfully different from their technical influence scope (cross-team), and collapsing them into one value would obscure that distinction.

## Consequences

- Every role document must declare a Reach value using this vocabulary.
- IC track roles declare a single Reach value; management track roles declare both a Leadership Reach and a Technical Reach.
- When creating or reviewing a role, the Reach value should be compared against adjacent roles in the progression to ensure it represents a meaningful step.
- The IC track tops out at **Industry** (Tech Fellow); the management track tops out at **Industry** for technical reach and **Company** for leadership reach (VP of Engineering).
