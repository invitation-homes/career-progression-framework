# ADR-0005: Dual-Document Structure Per Role

## Status

Accepted

## Date

2026-04-14

## Context

Each role in the framework serves two distinct audiences with different needs.

**Internal audience** — engineers and managers using the framework for career conversations, growth planning, and performance calibration.
They need a concise articulation of what excellence looks like at each level across the five dimensions: Impact, Reach, Knowledge, Communication, and Leadership.

**Hiring audience** — recruiters, hiring managers, and candidates evaluating whether a role is a fit.
They need a document structured around what the role does day-to-day, what experience is required, and how it fits into the organization.

The alternatives considered were:

**Single document per role** — one file that serves both purposes, switching between internal and external framing.
Avoids duplication but creates audience confusion: the growth-oriented language useful for career conversations reads awkwardly as a job posting, and the external-facing requirements language can feel evaluative in a coaching context.

**Job descriptions only** — eliminate progression documents and rely on JDs for all purposes.
Reduces files but loses the internal-facing, growth-conversation framing that makes the framework useful to practicing engineers.

**Progression documents only** — use the internal documents as the basis for all hiring.
Loses the practical requirements and day-to-day framing that candidates and recruiters expect from a job description.

## Decision

Each role is represented by two documents:

- A **progression document** at the repository root (`<role>.md`), structured around the five sections (Impact, Reach, Knowledge, Communication, Leadership), written for internal career conversations.
- A **job description** in the `job-descriptions/` subdirectory (`job-descriptions/<role>.md`), structured for hiring and written for candidates.

The two documents are linked bidirectionally: the progression document links to its corresponding JD, and the JD links back to the progression document.

## Rationale

- The two audiences have different mental models and different goals; a document that tries to serve both ends up serving neither well.
- Separating them allows each to be updated on its own cadence.
  Progression documents evolve as the organization's standards mature; JDs may change to reflect market conditions or specific hiring needs without touching the growth framework.
- Bidirectional links keep the two documents discoverable from each other without coupling their content.

## Consequences

- Adding a new role requires creating two files, not one.
- The cross-links between the two documents must be maintained when roles are renamed or removed.
- The Jekyll sidebar in `_config.yml` governs navigation to progression documents only; job descriptions are reachable through links from progression documents and directly by URL.
- The five-section structure (Impact/Reach/Knowledge/Communication/Leadership) applies to progression documents.
  Job descriptions use a different four-section structure (see ADR-0006).
