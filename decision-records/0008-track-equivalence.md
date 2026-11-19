# ADR-0008: Equivalent Grades Across Tracks

## Status

Accepted

## Date

2026-11-16

## Context

The framework has two career tracks above Software Engineer IV: the Professional Track (Staff Engineer through Tech Fellow) and the Management Track (Engineering Manager through VP of Engineering).
Moving between them is a lateral choice, not a promotion, so each Professional Track level has a Management Track counterpart at the same grade.

That equivalence was implied but never written down.
The career ladder diagram in `index.md` encodes it visually (a spacer node offsets Principal Engineer so it sits on the same row as Director of Engineering), but no page or Decision Record stated it.
Without a written mapping, the two tracks drifted apart: years of experience, Reach values, and expected behaviors did not match at levels meant to be equivalent.

The Management Track has one more level than the Professional Track above SE IV, so one management level has no Professional Track counterpart.

## Decision

These levels are equivalent grades:

| Professional Track | Management Track |
| --- | --- |
| Staff Engineer | Engineering Manager |
| none | Sr. Engineering Manager |
| Principal Engineer | Director of Engineering |
| Sr. Principal Engineer | Sr. Director of Engineering |
| Tech Fellow | VP of Engineering |

Sr. Engineering Manager is a Management Track step between Engineering Manager and Director of Engineering.
It has no Professional Track equivalent.

At each equivalent grade:

- **Reach:** the Professional Track role's Reach equals the Management Track role's Technical Reach (see [ADR-0004](0004-reach-vocabulary.md)).
- **Years of experience:** the job descriptions ask for the same minimum.
- **Behaviors:** the same core behaviors appear on both sides, scoped to the role: bias to action, disagree-and-commit, hiring, and automation.
- **Partnership:** each role names its counterpart on the other track as a partner.

## Rationale

- A written mapping lets contributors check a change on one track against its counterpart, instead of relying on the diagram's layout.
- Matching Technical Reach to Professional Track Reach expresses the idea that equivalent roles have the same technical scope; the manager's additional dimension is Leadership Reach.
- Naming counterparts as partners reflects how the roles work in practice: a Staff Engineer and an Engineering Manager, or a Principal Engineer and a Director, share responsibility for the same systems and teams.

## Consequences

- When adding or changing a role on either track, compare it with its equivalent grade as well as with adjacent levels on its own track.
- The career ladder diagram must keep equivalent grades on the same row.
- If a level is added to either track, this table must be updated, and any level without a counterpart must be called out explicitly.
