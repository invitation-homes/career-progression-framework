# ADR-0009: AI-Changed Expectations

## Status

Proposed

## Date

2026-11-17

## Context

Coding agents are becoming routine tools for every engineer.
The framework mentioned AI in a few places (a note on SE I learning, three specialized job descriptions), but its core expectations still assumed that writing code is the main work of an engineer and that scope grows mainly with experience.
If agents produce a competent first draft of well-specified work, expectations at every level shift.

This branch imagines that future and rewrites the progression documents, job descriptions, and being-a pages to match.
It is a proposal for discussion, not a description of how Invitation Homes works today.

## Decision

The framework treats AI as a change in what the work is, not as a separate skill track.
The levels, Reach vocabulary, years of experience, and track equivalence (see [ADR-0004](0004-reach-vocabulary.md) and [ADR-0008](0008-track-equivalence.md)) do not change.
The expectations inside each level do, guided by these hypotheses:

1. **Code is cheap; judgment is scarce.** Framing problems, specifying intent, decomposing work, verifying results, and deciding what ships carry the value.
2. **Accountability stays human.** You own what you ship, whoever or whatever wrote it.
3. **Specs, tests, and evals are the primary artifacts.** Written context serves humans and agents alike, so the knowledge-silos anti-pattern now starves agents too.
4. **Verification is the bottleneck.** Review capacity, not typing speed, limits delivery.
5. **Speed rises; scope does not.** Agents raise throughput and the expected standard of verification at every level. What each level owns (ownership, ambiguity, influence, accountability) stays defined as it is today.
6. **Learning must be protected.** Junior engineers understand and can explain everything they submit; senior engineers create learning opportunities that automation has removed.
7. **Senior individual contributor work becomes platform and guardrail work.** Standards must be machine-readable and automatically enforced.
8. **Management shifts to human-agent work systems.** Managers own the outcomes, quality, and cost of pods that include agents, and they do not measure people by AI usage.
9. **Risk grows with autonomy.** Security, resident data privacy, permission boundaries, cost, and change control scale with the level.

The engineering principles are unchanged.
Their application shifts: Passionate about Automation now includes delegating to agents with verification, and Committed to Quality now includes evals.

## Rationale

- Rewriting expectations in place keeps one framework instead of two parallel ones that drift apart.
- Keeping levels, Reach, and experience minimums fixed isolates the question under discussion: what the work looks like, not how the ladder is shaped.
  Treating AI as a speed change, not a scope change, avoids level inflation, where an engineer does next-level work at the same title and pay.
- Naming accountability and verification explicitly guards against the failure modes of agent-assisted work: shipped code nobody understands and a junior pipeline that never learns.

## Consequences

- Reviewers should read this branch as a set of hypotheses to challenge, level by level.
- Open questions this branch does not settle:
  - Whether pod sizes and direct-report counts change when pods include agents.
  - Whether years-of-experience minimums still predict the right scope at SE I and SE II.
  - How hiring loops assess judgment when candidates use AI tools.
  - How to evaluate performance fairly without measuring AI usage or output volume.
- If adopted, the specialized AI job descriptions should be reviewed for overlap with the new baseline expectations.
- If the hypotheses prove wrong, revert by closing this branch; main is unaffected.
