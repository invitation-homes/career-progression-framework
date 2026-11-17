---
id: overview
title: Engineering Career Progression Framework
---

This framework is a reference for you to understand the expectations of the roles at Invitation Homes.
Use it as a guide for behaviors we want to recognize, improve, or hold individuals accountable for.
Don't use it as a definitive checklist for promotion.
Meet with your manager to create a development plan, which may contain expectations and goals that aren't explicitly defined here.

The expectations in this framework are grounded in our [Engineering Vision, Mission, and Principles](./engineering-principles).
Regardless of role or track, a few behaviors reflect those principles and apply to everyone:

- Give feedback that is clear, kind, and actionable.
- Provide opinions and thoughts in a way that is conducive to collaboration and invites participation from others.
- Show empathy and kindness toward your peers and try to understand the views of others before attempting to defend your own.

# Career Progression Tracks

Engineers can take an individual contributor focused track, the Professional Track, or a people management focused track, the Management Track, as they build their careers here at Invitation Homes.

{% raw %}
<div class="mermaid" style="text-align: center;">
---
config:
  theme: neutral
  flowchart:
    curve: monotoneY
    nodeSpacing: 20
    rankSpacing: 25
  layout: fixed
---
flowchart TD
    SE1["Software Engineer I"] --> SE2["Software Engineer II"]
    SE2 --> SE3["Software Engineer III"]
    SE3 --> SE4["Software Engineer IV / Salesforce Platform Manager"]
    SE4 -- Professional Track --> Staff["Staff Engineer"]
    SE4 -- Management Track --> EM["Engineering Manager"]
    Staff --- Dummy[ ]
    Dummy --> Principal["Principal Engineer"]
    Principal --> SrPrincipal["Sr. Principal Engineer"]
    SrPrincipal --> TF["Tech Fellow"]
    EM --> SEM["Sr. Engineering Manager"]
    SEM --> ED["Director of Engineering"]
    ED --> SED["Sr. Director of Engineering"]
    SED --> VP["VP of Engineering"]
    SE1@{ shape: rounded}
    SE2@{ shape: rounded}
    SE3@{ shape: rounded}
    SE4@{ shape: rounded}
    Staff@{ shape: rounded}
    EM@{ shape: rounded}
    SEM@{ shape: rounded}
    Principal@{ shape: rounded}
    SrPrincipal@{ shape: rounded}
    TF@{ shape: rounded}
    ED@{ shape: rounded}
    SED@{ shape: rounded}
    VP@{ shape: rounded}
     SE1:::normNode
     SE2:::normNode
     SE3:::normNode
     SE4:::normNode
     Staff:::eng
     EM:::mgr
     SEM:::mgr
     Principal:::eng
     SrPrincipal:::exec
     TF:::exec
     ED:::mgr
     SED:::exec
     VP:::exec
     Dummy:::dummy
    classDef eng fill:#f7f7fa,stroke:#bbb,stroke-width:2px,color:#343a40
    classDef mgr fill:#f7f7fa,stroke:#bbb,stroke-width:2px,color:#343a40
    classDef exec fill:#f7f7fa,stroke:#bbb,stroke-width:2px,color:#343a40
    classDef normNode fill:#f7f7fa,stroke:#bbb,stroke-width:1.5px,color:#343a40
    classDef dummy style X width:1px,height:1px,fill:transparent,stroke:transparent 
    click SE1 "./software-engineer-i" _blank
    click SE2 "./software-engineer-ii" _blank
    click SE3 "./software-engineer-iii" _blank
    click SE4 "./software-engineer-iv" _blank
    click Staff "./staff-engineer" _blank
    click Principal "./principal-engineer" _blank
    click SrPrincipal "./sr-principal-engineer" _blank
    click TF "./tech-fellow" _blank
    click EM "./engineering-manager" _blank
    click SEM "./sr-engineering-manager" _blank
    click ED "./director-of-engineering" _blank
    click SED "./sr-director-of-engineering" _blank
    click VP "./vp-of-engineering" _blank

</div>
{% endraw %}

Levels on the same row are equivalent grades: Staff Engineer = Engineering Manager; Principal Engineer = Director of Engineering; Sr. Principal Engineer = Sr. Director of Engineering; Tech Fellow = VP of Engineering.
Moving between tracks at the same grade is a lateral move, not a promotion.
Sr. Engineering Manager is a Management Track step between Engineering Manager and Director of Engineering.

# Our Expectations

Our roles have five areas of focus: Impact, Reach, Knowledge, Communication, and Leadership.

## Impact

Impact is _what_ you do.
It reflects how you serve the people who depend on your work: residents, associates, and other teams.
How you produce impact is also a factor of your reach.

**Example**: A `Software Engineer I` will focus mostly on self-improvement and small, well-defined tasks.
Their impact is very localized and depends on following process and learning quickly to get to a place where they can work independently and provide more value.
By contrast, a `Software Engineer III` contributes to design, uses their knowledge to innovate, and mentors less senior engineers.

## Reach

Reach is _where_ you have impact.
Think of it as your "sphere of influence."
Your sphere of influence grows as you do.
Each level includes the ones before it: `Team` encompasses both `Individual` and `Self`.

- Self
- Individual
- Team
- Cross-Team
- Operating Group
- Department
- Company
- Industry

## Knowledge

Knowledge is one of the three factors of _how_ you work.
This covers both technical skills, such as the language your team works with, and domain and business-specific context.
The more knowledge you gain, the more tools and insight you have to shape code, projects, and architectural designs.

## Communication

This area covers how you communicate with those around you, in both technical and non-technical situations; this includes understanding how context, your tone, and the method you choose to communicate can impact those situations.

## Leadership

Leadership is how you create impact within your sphere of influence beyond the code you ship.
It might mean mentoring other engineers or using your expertise in a particular area to support or train other teams.
