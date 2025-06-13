---
id: overview
title: Engineering Career Progression Framework
---

This framework is a reference for you to understand the expectations of the roles at 
Invitation Homes. It should be used as a guide for behaviors we want to recognize, improve, or hold individuals 
accountable for. It should not be used as a definitive checklist for promotion. You should be meeting with your manager 
and creating a development plan, which may contain expectations and goals that are not explicitly defined here.

Our culture is driven by a few guiding principles. These principles are shared amongst all Engineers, regardless of role.

- Give feedback that is clear, kind, and actionable
- Provide opinions and thoughts in a way that is conducive to collaboration and invites participation from others.
- Show empathy and kindness toward your peers and try to understand the views of others before attempting to defend your 
own.

# Career Progression Tracks

Engineers at Invitation Homes can take a individual contributed focused track, our Professional Track, or a people management focused track, the Management Track.

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
    SE1["Software Engineer 1"] --> SE2["Software Engineer 2"]
    SE2 --> SE3["Software Engineer 3"]
    SE3 --> SE4["Software Engineer 4"]
    SE4 -- Professional Track --> Staff["Staff Engineer"]
    SE4 -- Management Track --> EM["Engineering Manager"]
    Staff --> Principal["Principal Engineer"]
    EM --> SEM["Senior Engineering Manager"]
    SEM --> ED["Engineering Director"]
    ED --> SED["Sr. Engineering Director"]
    SED --> VP["VP of Engineering"]
    SE1@{ shape: rounded}
    SE2@{ shape: rounded}
    SE3@{ shape: rounded}
    SE4@{ shape: rounded}
    Staff@{ shape: rounded}
    EM@{ shape: rounded}
    SEM@{ shape: rounded}
    Principal@{ shape: rounded}
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
     ED:::mgr
     SED:::exec
     VP:::exec
    classDef eng fill:#f7f7fa,stroke:#bbb,stroke-width:2px,color:#343a40
    classDef mgr fill:#f7f7fa,stroke:#bbb,stroke-width:2px,color:#343a40
    classDef exec fill:#f7f7fa,stroke:#bbb,stroke-width:2px,color:#343a40
    classDef normNode fill:#f7f7fa,stroke:#bbb,stroke-width:1.5px,color:#343a40
    click SE1 "./software_engineer_I" _blank
    click SE2 "./software_engineer_II" _blank
    click SE3 "./software_engineer_III" _blank
    click SE4 "./software_engineer_IV" _blank
    click Staff "./staff_engineer" _blank
    click Principal "./principal_engineer" _blank
    click EM "./engineering_manager" _blank
    click SEM "./senior_engineering_manager" _blank
    click ED "./director_of_engineering" _blank

</div>
{% endraw %}

# Our Expectations

Our roles have five areas of focus: Impact, Reach, Knowledge, Communication and Leadership.

## Impact

Impact is _what_ you do. It is a reflection of how you serve your customers, whether they are internal or external. 
How you produce impact is also a factor of your reach. 

**Example**: A `Software Engineer I` will focus mostly on self-improvement and small well-defined tasks. Their impact 
is very localized and depends on following process and learning quickly to get to a place where they can work 
independently and provide more value. A `Software Engineer III` will, conversely, be expected to contribute to design, 
use their knowledge for innovation, and provide mentorship to less senior roles.

## Reach

Reach is _where_ you have impact. It could also be considered your “sphere of influence”. It is expected that your 
sphere of influence should grow as you do. Each level is inclusive of the ones that came before it. i.e. `Team` 
encompasses both `Individual` and `Self`.

- Self
- Individual
- Team
- Cross-Team
- Department
- Company

## Knowledge

Knowledge is one of the three factors of _how_ you work. This covers both technical skills, such as the language your 
team works with, as well as domain and business-specific context. The more knowledge you gain, the more tools and 
insight you have to impact code, projects, architectural designs, etc…

## Communication

This area covers how you communicate with those around you, in both technical and non-technical situations; this 
includes understanding how context, your tone and the method you choose to communicate can impact those situations.

## Leadership

Leadership is how one can provide impact within your sphere of influence without releasing code. Whether it’s actively 
looking to mentor other engineers or using your expertise in a particular area to provide support or training across 
teams.
