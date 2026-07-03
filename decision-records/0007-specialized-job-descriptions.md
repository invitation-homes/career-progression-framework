# ADR-0007: Specialized Job Descriptions for Hiring Variants

## Status

Accepted

## Date

2026-07-03

## Context

Some hiring needs call for a job posting that reads as its own role — with title, framing, and requirements tailored to a specific specialization — but does not correspond to a distinct rung on the career ladder.
The first case is AI-focused hiring: "Staff AI Engineer" and "Principal AI Engineer" are titles used for external job postings, but a person hired into either is leveled, compensated, and managed internally as a Staff Engineer or Principal Engineer.
There is no separate Impact/Reach/Knowledge/Communication/Leadership bar for an "AI Engineer" track.

The dual-document structure in [ADR-0005](0005-dual-document-structure.md) assumes every JD has a matching progression document at the same level.
That assumption does not hold here, and forcing it would create a progression document, a sidebar entry, and a Mermaid diagram node for a level that does not exist — misrepresenting the ladder for the sake of file-structure consistency.

The alternatives considered were:

**Treat it as a normal role** — create a paired progression document, add it to `_config.yml` and `index.md` like any other role.
Rejected: this implies a distinct career level, which is false, and would require an artificial progression document with no real internal use.

**Store it outside the repository** — keep these JDs in whatever external system hosts the job posting.
Rejected: the user wants one source of truth for all job description content, including hiring variants, so it can be reviewed and maintained with the same process as everything else.

**A separate `job-descriptions/specialized/` subdirectory, excluded from the Jekyll build and unlinked from the main content** — the JD exists as its own file for source-of-truth and export purposes, but is not part of the published site and is not cross-linked with the progression document it maps to.

## Decision

Specialized job descriptions — postings that map to an existing progression level rather than introducing a new one — live in `job-descriptions/specialized/`.

- Filenames do not carry a `-jd` suffix (e.g. `staff-ai-engineer.md`), since there is no same-named progression document to collide with.
- Front matter still applies the `-jd` suffix to the `id` for consistency with every other JD in the repo (e.g. `id: staff-ai-engineer-jd`), even though the page is excluded from the Jekyll build.
- The `job-descriptions/specialized/` directory is added to the `exclude` list in `_config.yml`, so Jekyll does not generate a page for these files at all.
- Nothing in the main content links to a specialized JD, and a specialized JD does not link back to a progression document. These files exist purely as repo-tracked source content for the JD itself and for `bin/export-jd`, not as part of the browsable site.
- The trailing `---` separator is still present at the end of the file (with nothing following it), since `bin/export-jd` uses it as the marker for where the exportable body ends.
- They otherwise follow the same four-section format and formatting conventions as any other JD (see [ADR-0006](0006-job-description-format.md)).

## Rationale

- The underlying career ladder should only ever represent real levels. Excluding specialized JDs from the Jekyll build entirely, rather than just leaving them out of the sidebar, guarantees there's no orphaned page or stray link path that implies they're part of the ladder.
- These postings are used externally (e.g. job boards), not referenced internally during career conversations, so there is no reason for the framework's internal content to point at them.
- A dedicated subdirectory makes the "this is a hiring variant, not a new rung, not part of the site" distinction structurally obvious, rather than relying on a reader noticing the absence of a paired root file or sidebar entry.
- Keeping specialized JDs in this repository, in the same format as every other JD, preserves a single source of truth and lets them go through the same review process and export tooling as the rest of the framework, without publishing them as site pages.

## Consequences

- `bin/export-jd` must resolve roles that include a subdirectory (e.g. `specialized/staff-ai-engineer`), not just flat filenames in `job-descriptions/`.
- Adding a specialized JD does not require the three-file update described in AGENTS.md for a new role; it requires only the specialized JD itself and an entry in `_config.yml`'s `exclude` list.
- If a specialization ever grows into a genuinely distinct level with its own bar, it should be migrated out of `specialized/` into the normal one-file-per-role structure, with its own progression document, sidebar entry, diagram node, and cross-links — and removed from the `exclude` list.
