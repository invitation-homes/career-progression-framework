# ADR-0006: Job Description Format

## Status

Accepted

## Date

2026-04-14

## Context

Job descriptions (see ADR-0005) need a consistent internal structure so they read coherently as a set and give contributors a clear template to follow when adding new roles.
Several format decisions arose during the initial authoring of all thirteen JDs and are captured here.

**Section structure** — JDs need sections that make sense to candidates and hiring managers.
The five-section progression document structure (Impact/Reach/Knowledge/Communication/Leadership) is growth-oriented and internally framed; it does not map naturally onto what candidates expect from a job posting.

**File location and naming** — JDs live alongside progression documents (root) or in a subdirectory.
A subdirectory keeps the two document types cleanly separated and avoids any filename collision with existing root-level progression documents.

**Jekyll page IDs** — Each Jekyll page needs a unique `id` in its front matter.
JD filenames mirror their progression document counterparts (e.g., `engineering_manager.md` in both locations), which would produce duplicate IDs if the same convention were used.

**Cross-link syntax** — Jekyll renders Markdown links without `.md` extensions.
Links that include the `.md` extension work in raw Markdown editors but produce broken URLs in the rendered Jekyll site.

## Decision

**Section structure** — Job descriptions use four sections:

1. **About the Role** — a short narrative introducing the role, who it reports to, and the mindset it requires.
2. **Technical Leadership** — hands-on technical expectations and the scope of technical influence.
3. **Knowledge & Standards** — required experience, technologies, and domain depth.
4. **Communication & Collaboration** — how the role communicates within and across teams, with stakeholders, and (where relevant) externally.
5. **Leadership & Culture** — people, culture, and organizational contributions expected at this level.

**File location** — Job descriptions live in the `job_descriptions/` subdirectory.
The filename matches the corresponding progression document exactly (e.g., `job_descriptions/engineering_manager.md` pairs with `engineering_manager.md`).

**Jekyll front matter** — Each JD includes a front matter block with `id` and `title`.
The `id` value appends `-jd` to the role's base identifier to avoid collision with the progression document's page ID (e.g., `engineering-manager-jd` vs. `engineering-manager`).

**Cross-link syntax** — Links between progression documents and JDs omit the `.md` extension.
From a progression document: `[Job Description](job_descriptions/<role>)`.
From a JD: `[Progression Document](../<role>)`.

**Trailing separator** — Each JD ends with a horizontal rule (`---`) followed by the `[Progression Document]` back-link.
This separator is used by the `bin/export-jd` export script to detect and strip the link from generated Word documents, where it has no meaning.

## Rationale

- The four-section JD structure reflects how candidates evaluate roles: what is the day-to-day work, what are the requirements, how does this role communicate, and what does leadership look like here.
  This is meaningfully different from the growth-conversation framing of the five-section progression document structure.
- The `job_descriptions/` subdirectory avoids cluttering the root with two files per role and makes the separation of document types structurally obvious.
- The `-jd` suffix on page IDs is the minimal change needed to satisfy Jekyll's uniqueness constraint without altering filenames or URLs.
- Omitting `.md` from links is required for Jekyll compatibility; links with the extension break on the rendered site.
- The trailing separator convention co-locates the back-link with the content it belongs to while giving the export script a reliable, format-agnostic signal for where the body ends.

## Consequences

- Every new role requires a JD in `job_descriptions/` following this four-section structure.
- Front matter IDs for JDs must use the `-jd` suffix.
- All internal links between progression documents and JDs must omit `.md` extensions.
- The trailing `---` + back-link must be maintained at the end of each JD; removing it breaks the export script's stripping logic.
