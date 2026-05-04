# Engineering Career Progression Framework

This is Invitation Homes' career progression framework for software engineering.
It defines role expectations across both the IC and management tracks.
Engineers and managers use it in career conversations and performance evaluations.
It is also shared publicly with prospective engineers.

The site is hosted at [invitation-homes.github.io/career-progression-framework](https://invitation-homes.github.io/career-progression-framework/).

## Repo structure

```
<role>.md                  # Progression document for each role
job-descriptions/<role>.md # Job description for each role
being-a/<role>.md          # Narrative companion pages (not every role has one)
engineering_principles.md  # The seven engineering principles that underpin all roles
decision-records/          # ADRs documenting structural and formatting decisions
index.md                   # Site home page with career ladder diagram
_config.yml                # Jekyll config and sidebar navigation
bin/                       # Export scripts
```

## Contributing

**Conventions:** [AGENTS.md](AGENTS.md) is the starting point — it covers repo structure, required file updates when adding or removing a role, front matter, links, and formatting rules.

**Voice and style:** [style-guide.md](style-guide.md) covers voice, tone, sentence craft, vocabulary, anti-patterns, and a revision checklist.

**Structural decisions:** [decision-records/](decision-records/) documents the *why* behind key formatting and structural choices.

When adding a new role, update `_config.yml` (sidebar navigation), `index.md` (career ladder diagram), and create both a progression document and a job description. You may also need a being-a page in `being-a/` — not every role has one, and a single being-a page can cover multiple roles (Software Engineer I–III share one, for example). See [AGENTS.md](AGENTS.md) for details.

## Exporting job descriptions

`bin/export-jd` converts job descriptions to `.docx` using `pandoc` (`brew install pandoc`).

```
bin/export-jd <role>               # single role
bin/export-jd all                  # all job descriptions
```

## Theme

The site uses a shared GitHub Pages theme maintained at [invitation-homes/career-progression-framework-theme](https://github.com/invitation-homes/career-progression-framework-theme).
Changes to layout, CSS, and navigation are made there.
