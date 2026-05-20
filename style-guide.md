---
id: style-guide
title: Writing Style Guide
---

# Writing Style Guide

This guide covers voice, tone, sentence craft, vocabulary, and the patterns that make this framework's writing work.
It is a companion to the [ADRs](decision-records/), which handle structural and formatting decisions.
Where the two overlap, ADRs govern structure; this guide governs everything else.

## Voice and Tone

Write directly to the person holding the role, in second person.
"You lead the leaders" — not "The Director of Engineering is responsible for leading."
Contractions are welcome.
The writing should feel like a smart colleague explaining the job, not a policy document.

Be honest about hard things.
Acknowledge tensions, ambiguity, and the messiness of real work.
"You'll be further from the code than ever" is better than "This role operates at a strategic level."

The tone is warm but not soft.
It respects the reader's intelligence.
It does not patronize junior roles or over-formalize senior ones.

## Document Structure

### being-a pages

The being-a pages follow a consistent shape:

1. A short, declarative opener naming the essence of the role
2. The "Our systems touch residents in hundreds of thousands of homes" paragraph, grounding the work in real impact
3. The residents/associates footnote: `("Residents" are the people who live in our homes; "associates" are our employees.)`
4. A blockquoted external attribution from a relevant author
5. A "No two X will look the same" paragraph acknowledging the range of the role and naming what stays constant
6. Thematic sections (H2) with subsections (H3)
7. A "From here" closing paragraph linking to the next level

Narrative context always comes before lists and structure.
The reader should understand the *feel* of the role before its formal shape.

### Progression documents

Five sections in order: **Impact**, **Reach**, **Knowledge**, **Communication**, **Leadership**.
See [ADR-0004](decision-records/0004-reach-vocabulary) for Reach vocabulary and the IC vs. management track distinctions.

### Job descriptions

See [ADR-0006](decision-records/0006-job-description-format) for structure and formatting conventions.

### Formatting

See [ADR-0001](decision-records/0001-semantic-line-breaks) for the semantic line break convention (one sentence per line in prose).

## Sentence Craft

### Rhythm

Mix short and long sentences deliberately.
A short sentence creates emphasis and lets an idea land; a long sentence carries the explanation, nuance, and context that earns the landing.
Neither works in isolation.
Never run three long sentences in a row without a short one to break them up, and never cluster short sentences until the prose flattens into a list.
Short sentences land because they follow something longer.
Used in clusters, they lose their punch.

**Works:**
> You lead the leaders.
> Your direct reports are Engineering Managers.
> The lever has shifted from writing code to building the organizational conditions — the structure, culture, and leadership capacity — that let multiple teams operate well at once.

**Does not work — too many long sentences:**
> As a Director of Engineering, you are responsible for the strategic technical vision of your operating group, including the management of engineering managers, the alignment of technical decisions with business strategy, and the cultivation of a high-performance culture across multiple cross-functional teams.

**Does not work — too many short sentences:**
> Change is a constant. Your team will face new tools. Sometimes all at once. Your job isn't to absorb it. It's to help your team move through it. Explain what is changing. Create a plan. Close the loops.

### Active voice

The subject does the thing.

| Instead of | Write |
| --- | --- |
| "Decisions are made at this level" | "You make the call" |
| "Feedback should be given promptly" | "Give it as close to the event as possible" |
| "Alignment is created through..." | "Create alignment by..." |

### Sentence openers

Vary them.
Don't start three consecutive sentences with the same word.
Sentences that open with something other than "you" are especially useful for rhythm:

> "Culture at scale does not emerge on its own."
> "Context that lives in people's heads leaves when they do."
> "The best time to address an organizational gap is before you feel it."

### Nominalization

Turn noun-heavy phrases back into verbs.

| Instead of | Write |
| --- | --- |
| "provide guidance to" | "guide" |
| "make a decision" | "decide" |
| "give consideration to" | "consider" |
| "have an impact on" | "affect" or "shape" |

## Signature Moves

These are patterns the framework uses well.
Use them — but don't force them.

**The declarative opener.**
Every being-a page opens with a short, definitional sentence.
- "You are a practitioner."
- "You lead the leaders."
- "You are a [player-coach]."

**The mission paragraph.**
"Our systems touch residents in hundreds of thousands of homes: the app they use to pay rent, the portal for maintenance requests, the tools associates depend on every day."
This appears near the top of every being-a page and grounds abstract role descriptions in real-world impact.
The paragraph ends with a level-specific sentence about stakes, then: "When we get it right, people feel it."
Do not vary that final sentence.

**The disagree-and-commit pair.**
Speak up when you disagree — commit fully once a decision is made.
This appears across all levels, scoped to each role.
The closing line is always a variant of: "That combination of honest advocacy and full commitment is how [X] operate with integrity and speed."

**The "no two X will look the same" paragraph.**
After the opening quote in each being-a page, this paragraph names the variables that shift the role (team maturity, company phase, individual context) and names what stays constant.
It gives permission for variation while anchoring expectations.

**Short emphatic sentences after explanation.**
When you have explained something complex, land it with a short sentence.
> "Context that lives in people's heads leaves when they do."
> "The best time to address an organizational gap is before you feel it."
> "When we get it right, people feel it."
The power is in the contrast with what came before. Used back to back, the emphasis dissolves.

**External attribution format.**
Blockquote with an attribution line:

```
> *"The quote text."*
> — Author Name, *Book or Source Title*
```

Verify every quote before publishing.
Do not present paraphrases as direct quotes.
If you cannot confirm a quote is accurate, find an alternative.

## Anti-Patterns

### AI tells to remove on sight

| Word / phrase | Why it's weak | What to write instead |
| --- | --- | --- |
| ensure | Vague obligation | "make sure," or reframe as a direct action |
| foster | Corporate warmth | "build," "create," "encourage" |
| leverage (verb) | Jargon | "use," "draw on," "build on" |
| navigate (metaphorical) | Overused | "work through," "handle," "manage" |
| pivotal / crucial / critical | Inflation | Cut, or restate with specifics |
| streamline | Jargon | Say what actually changes |
| utilize | Bureaucratic | "use" |
| robust | Vague positive | Say what specifically makes it strong |
| seamlessly | Fantasy language | Cut |
| empower | Corporate warmth | Be specific about what is enabled or possible |
| it is important to note | Throat-clearing | Just say the thing |
| in order to | Padding | "to" |
| at the end of the day | Cliché | Cut or rewrite |
| cutting-edge | Marketing language | Name the specific technology or approach |

### Em-dashes

Do not use em-dashes in prose.
Use a colon, a period, or a semicolon instead — they force more precise thinking about the relationship between clauses.

The one exception: attribution lines in blockquotes (`— Author Name, *Source*`).

The "Engineering — that's you —" construction in triad and quad role descriptions is grandfathered in as a shared pattern across the EM and Director pages.

### Softening

Do not use euphemism or corporate softening for hard realities.

| Instead of | Write |
| --- | --- |
| "This role involves some ambiguity" | "You'll have significant autonomy and incomplete information." |
| "Provide constructive feedback" | "Give direct, specific feedback." |
| "Support your team members' growth" | "Coach them. Give feedback. Create opportunities." |

## Vocabulary Reference

Use these terms consistently.
Introducing synonyms creates noise.

Where the company's Key Competencies define specific language for a behavior or expectation, use that language.
The competencies and their preferred vocabulary are summarized in [key_competencies.md](key_competencies.md).

| Term | Form | Notes |
| --- | --- | --- |
| pod | lowercase | The cross-functional team. Not "team," "squad," or "group." |
| operating group | lowercase | The Director's scope. Not "department" — that refers to the full engineering org. |
| EM | abbreviation | Define as "Engineering Manager" at first use; abbreviate thereafter. |
| IC | abbreviation | Define as "Individual Contributor" at first use. |
| KLO | abbreviation | Define as "Keep the Lights On" at first use. |
| CAB | abbreviation | Define as "Change Approval Board" at first use. |
| triad | lowercase | The pod leadership group: EM, Product Owner, Product Designer. |
| Strategy Tier | title case | The operating group leadership group: Director, Product, Design, Project Manager. |
| residents | lowercase | People who live in IH homes. Define at first use with the standard footnote. |
| associates | lowercase | IH employees. Defined alongside residents. |
| on-call | hyphenated | Always. |
| Decision Record | title case | Use in prose. "ADR" is acceptable in technical or tooling contexts. |
| player-coach | hyphenated | Used specifically for the EM role. |
| bias to action | — | Not "bias toward action." |
| postmortem | one word | No hyphen. |

## Revision Checklist

Run this before considering a draft done.

- [ ] No em-dashes in prose (exceptions: attribution lines; "Engineering — that's you —" in triad/quad tables)
- [ ] None of these words: "ensure," "foster," "leverage" (verb), "navigate" (metaphorical), "pivotal," "crucial," "streamline," "utilize," "robust," "seamlessly," "empower"
- [ ] Active voice — the subject does the thing
- [ ] Every paragraph has at least one short sentence (under ~15 words)
- [ ] No three consecutive sentences starting with the same word
- [ ] All abbreviations defined at first use
- [ ] "residents" and "associates" used (not "customers," "users," "employees")
- [ ] All external quotes verified and attributed
- [ ] First sentence of each being-a page is short and declarative
- [ ] No throat-clearing ("it is important to note," "in order to," "at the end of the day")
- [ ] Noun phrases converted to verbs where possible
