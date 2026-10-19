---
id: vp-of-infrastructure-jd
title: VP of Infrastructure
---

## About the Role

Invitation Homes set out to solve a real problem: home leasing options were limited and the experience for residents was inconsistent.
Today we're the nation's largest single-family home rental company, with 100,000+ homes.
Our teams build the technology at the center of that solution: personalized resident experiences, service tools, and the operational systems that residents and associates depend on every day.
When we ship, people feel it.

Our technology organization takes that responsibility seriously. That means collaborative teams, high standards, and real investment in the people around you.
Every one of those teams depends on the infrastructure underneath it, and so does every associate who opens a laptop in one of our field offices.
When it breaks, nothing else works.
You are accountable for all of it.
That means the cloud platform and databases our engineers build on, the corporate systems every associate uses, the network that connects our field offices, and the help desk and desktop support our associates rely on.
You lead our Enterprise Infrastructure and Support Services organization and report to the Senior Vice President (SVP) of Engineering.

We run on Amazon Web Services (AWS), and we want to run on it the way it was meant to be used.
We want every environment defined in source control, every change flowing through a pipeline, and no one logging into a server to fix it by hand.
If AWS offers a managed service that does the job, we use it unless the cost is unreasonable.
The same standard applies beyond the cloud, to laptops and network devices.
Part of our environment still runs on hand-configured EC2 instances that people have tended for years.
Moving those workloads to automated, reproducible, managed infrastructure is a large part of this job, and so is building the culture that keeps it there.

## What You'll Do

**Technical Leadership**

- Own the infrastructure strategy and multi-year roadmap: where we run, how we run it, and what we stop running ourselves.
- Lead the move from hand-configured servers to infrastructure that is declared in code, delivered only through automated pipelines, and rebuilt rather than repaired.
- Set a managed-services-first standard: default to AWS managed services (including moving self-managed databases onto RDS), and make the cost and trade-offs visible when you make an exception.
- Build the platform as a product: self-service provisioning and golden paths that make the right way the easy way for every team.
- Own reliability: service level objectives (SLOs), observability, incident response, a postmortem culture that turns incidents into improvements, and business continuity and disaster recovery plans that are tested regularly.
- Build security into the platform through least-privilege Identity and Access Management (IAM), policy as code, and automated patching.
- Own the infrastructure controls and audits behind our Sarbanes-Oxley (SOX) and Payment Card Industry (PCI) compliance.
- Own the help desk: level 1 and 2 support for every associate, including those in our field offices.
  Set SLOs for response and resolution time, measure satisfaction, and hold the team accountable for the associate experience.
- Close the loop between the help desk and engineering, so the help desk escalates what needs a deeper fix, engineering resolves it at the root, and the fix feeds back into automation and self-service.
- Run end-user technology and corporate systems: desktop support, asset and device management, Active Directory, email, SharePoint, and collaboration tools.
- Run network and telecom connectivity to our field offices, including the technology side of office openings, moves, expansions, and renovations.
- Manage the infrastructure budget, cloud spend, and strategic vendor relationships (including AWS), and make cost a design input alongside reliability and speed.
- Bring AI and automation to the help desk and IT operations where they fit: self-service, automated resolution of common requests, and faster routing.
  The team's time goes to the problems that need a person.

**Knowledge & Standards**

- Maintain the hands-on depth to review a Terraform module, question an architecture diagram, and spot a one-off server in a design proposal.
- Set clear, written standards for infrastructure, and record the decisions that matter in architecture decision records (ADRs) so the reasoning outlives the people who made it.
- Know the data protection laws that apply to us, such as the California Consumer Privacy Act (CCPA), and build their requirements into how our systems store and handle data.

**Communication & Collaboration**

- Explain infrastructure strategy, risk, and cost to executives in terms of business impact, and to engineers in terms of how their work changes.
- Make the case for change to people who built and maintain the current systems, with respect for that work and clarity about why those systems need to change.
- Partner with leaders across Engineering, Security, Data, Product, Finance, and field operations so our infrastructure serves the whole company.
- Work as a close partner to the Chief Information Security Officer (CISO): design security controls into the platform together, share ownership of the guardrails, support security incident response, and treat security findings as engineering work.
- Keep leadership informed: publish reliability, cost, help desk, and migration metrics openly, and lead communication during major outages.

**Leadership & Culture**

- Hire, develop, and retain a diverse infrastructure and support organization, and coach the managers and senior engineers who lead it.
- Build a help desk team that associates trust: clear career paths from support into engineering, and managers who coach on both technical skill and service.
- Build a culture that treats manual work as a defect: if something is done by hand twice, it gets automated.
- Invest in the people whose expertise lives in hand-built systems, and help them become the people who automate those systems away.
- Model low-ego, action-oriented leadership: decisive when needed, collaborative by default, and focused on making every team faster and safer.
- Hire and promote from a wide pool, and build a team where people with different backgrounds do their best work.

## What You Bring

- 15+ years of experience in technology, with 10+ years leading large, geographically distributed infrastructure and support organizations, including managers and directors.
- Deep, hands-on experience with AWS in production and expert command of infrastructure as code (ideally Terraform), CI/CD, and GitOps.
- A track record of moving an organization from manually managed servers to automated, cloud-native infrastructure, and of making that change stick.
- Experience running a help desk and IT operations across distributed sites, applying IT Infrastructure Library (ITIL) practices where they help.
- Experience owning reliability, disaster recovery, business continuity, and compliance at scale, including SOX and PCI controls and audits.
- Experience owning a cloud budget and running cloud financial management (FinOps) practices that reduce cost without slowing teams down.
- A degree in Computer Science, Computer Engineering, Information Systems, or a related field, or equivalent practical experience.
- Willingness to travel to our second corporate office and to field offices.
- ServiceNow experience, ITIL certification, and AWS certifications are a plus but not required.

## Our Stack

Our core AWS services include Lambda, DynamoDB, and RDS.
We manage infrastructure as code with Terraform and deliver changes through CI/CD pipelines.
ServiceNow handles our IT service management.
Our application teams build with TypeScript, Node.js, React, PostgreSQL, and Salesforce; familiarity with that stack is helpful but not required.
We care more about depth of thinking, adaptability, and the drive to keep learning than familiarity with any specific tool.

---
