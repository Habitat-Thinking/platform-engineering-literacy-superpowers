# Scenario Bank

Use these scenarios for Phase 3 (Deep Dive) assessment or as in-class exercises.
Each scenario presents a realistic platform engineering situation. The response
guide describes how practitioners at different levels typically approach the
problem.

## Context Awareness Scenarios

**Scenario CA-1: The New Platform Request** *(boundary 0→1)*

Your VP of Engineering asks: "We need an internal developer portal. Other
companies have one. Can you build it?" You have three weeks to come back
with a proposal.

- *Level 0 response:* Researches portal technologies, evaluates vendors,
  produces a feature comparison. The proposal centres on which tool to use.
- *Level 1 response:* Before evaluating tools, maps the current developer
  landscape — who are the users, what are their workflows, where is the
  friction? Uses Wardley Mapping to position portal capabilities by
  evolution. The proposal centres on what problems the portal would solve
  and for whom.
- *Facilitator note:* The key signal is whether the person starts with
  technology or starts with users and context. Level 1 asks "what problem
  are we solving?" before "what tool should we use?"

**Scenario CA-2: The Conflicting Roadmaps** *(boundary 2→3)*

Two business units are asking for platform capabilities that conflict —
one needs strict multi-tenancy isolation, the other needs cross-tenant
data sharing. Both claim their needs are urgent. Your current platform
architecture does not cleanly support either.

- *Level 2 response:* Designs a solution that addresses both needs
  technically — an abstraction layer that supports both isolation and
  controlled sharing. Focuses on the design problem.
- *Level 3 response:* Maps the strategic landscape first — where are these
  business units going over the next 2 years? Which need is structural and
  which is transitional? Uses living context systems (regularly updated
  maps) to inform a decision that serves the long-term platform direction,
  not just the immediate ask.
- *Facilitator note:* The key signal is whether the person treats this as a
  design problem (Level 2) or a strategic problem (Level 3). Level 3 looks
  beyond the immediate conflict to the evolution of both business units.

**Scenario CA-3: The Stewardship Test** *(boundary 3→4)*

You have been promoted and will lead platform strategy across three
previously independent platform teams. Each has its own maps, its own
strategic framing, and its own relationship with business stakeholders.
They are not hostile but they are not aligned.

- *Level 3 response:* Works to understand each team's context and find
  tactical alignment opportunities — shared components, common patterns,
  joint planning sessions.
- *Level 4 response:* Establishes a practice for distributed strategic
  awareness — teaches teams to map each other's landscapes, facilitates
  cross-team strategic conversations, creates mechanisms for ongoing
  alignment that do not depend on the leader being in every meeting.
- *Facilitator note:* Level 4 builds the capacity for alignment rather than
  personally driving it.

## Cognitive Load Design Scenarios

**Scenario CL-1: The Onboarding Problem** *(boundary 0→1)*

A new developer joins a team that uses your platform. After two weeks, they
still cannot deploy independently. Their tech lead says "the platform is too
complicated." You are asked to fix it.

- *Level 0 response:* Identifies that the onboarding experience is poor and
  proposes improvements — better docs, a getting-started guide, a
  simplified first deployment.
- *Level 1 response:* Traces the new developer's actual workflow step by
  step — where do they lose context? Where is representational state
  corrupted? Diagnoses whether the problem is intrinsic complexity (the
  domain is genuinely hard) or extraneous load (the platform is adding
  unnecessary difficulty). The solution targets the specific load sources.
- *Facilitator note:* Level 0 responds to the symptom. Level 1 diagnoses
  the mechanism — the specific cognitive load sources.

**Scenario CL-2: The Feature That Adds Load** *(boundary 1→2)*

Your team wants to add a policy engine to the platform — every deployment
must pass policy checks. The security team loves it. You suspect it will add
significant cognitive load for developers. How do you proceed?

- *Level 1 response:* Recognises the load will increase and raises the
  concern, but cannot propose a specific design that addresses both needs.
- *Level 2 response:* Designs the policy engine with cognitive load as a
  first-class constraint — policies are expressed in developer-friendly
  terms, violations produce actionable feedback (not just "policy failed"),
  and the golden path pre-satisfies common policies so most developers
  never encounter a policy failure. Applies the 4pm Friday test.
- *Facilitator note:* Level 2 does not just recognise the load — they
  design around it with specific mechanisms.

**Scenario CL-3: The Measurement Challenge** *(boundary 2→3)*

Your platform has reduced deploy time from 30 minutes to 5 minutes, but
developer satisfaction scores have not improved. Leadership asks whether the
platform investment is working. How do you investigate?

- *Level 2 response:* Looks at qualitative feedback — surveys, interviews —
  to understand why satisfaction has not improved despite the speed gain.
- *Level 3 response:* Measures beyond the obvious — deploy time is one load
  source, but what about config management load, debugging load, incident
  response load? Builds a measurement framework that captures the full
  cognitive load picture, not just the dimension that was optimised. Uses
  data to show which load sources still dominate.
- *Facilitator note:* Level 3 measures systematically rather than
  investigating anecdotally.

## Pattern Application Scenarios

**Scenario PA-1: The Golden Path Dilemma** *(boundary 1→2)*

Your platform's golden path for creating new services works well for
standard CRUD microservices, but data engineering teams say it does not fit
their workflow. They are building their own tooling. What do you do?

- *Level 1 response:* Recognises the gap — the golden path does not cover
  this use case. May propose building a second golden path or extending
  the existing one.
- *Level 2 response:* Analyses which patterns are in tension — Golden Path
  (opinionated route) vs Extensibility (extend without core changes) vs
  Composability (capabilities combine in unanticipated ways). Designs a
  solution that might look like a composable golden path where the data
  teams can swap specific components while keeping shared guardrails and
  observability.
- *Facilitator note:* Level 2 sees the pattern tensions explicitly and
  designs with them, rather than treating it as a gap to fill.

**Scenario PA-2: The Incremental Delivery** *(boundary 2→3)*

You have designed a comprehensive self-service platform for infrastructure
provisioning. The design covers provisioning, configuration, policy,
observability, and cost management. Your team has capacity for about
3 months of work. How do you deliver it?

- *Level 2 response:* Plans a phased rollout — provisioning first, then
  configuration, then the rest. Each phase is a complete block.
- *Level 3 response:* Slices differently — finds the smallest useful slice
  that spans the patterns (e.g., self-service provisioning for one
  resource type, with basic guardrails and minimal observability), ships
  it, measures adoption and feedback, and uses that to inform the next
  slice. Each slice is independently valuable and measurable.
- *Facilitator note:* Level 3 slices by value, not by layer. The smallest
  slice is a working end-to-end experience, not a complete layer.

**Scenario PA-3: The Pattern Evolution** *(boundary 3→4)*

Your platform has been running for 3 years. You notice that teams are
consistently building a capability that does not fit neatly into any of the
ten patterns — a "Feature Flag Gateway" that combines guardrails, incremental
rollout, and observability in a specific way. Is this a new pattern?

- *Level 3 response:* Recognises the recurring capability and builds it
  into the platform as a feature, using the existing patterns to describe
  its components.
- *Level 4 response:* Evaluates whether this is genuinely a new pattern or
  a composition of existing patterns. If new, articulates it with the same
  rigour as the existing ten — intent, forces, resolution, consequences.
  Establishes governance for how patterns are proposed, evaluated, and
  adopted across the organisation.
- *Facilitator note:* Level 4 evolves the language itself, not just the
  platform.

## Feedback and Measurement Scenarios

**Scenario FM-1: The Dashboard Nobody Watches** *(boundary 1→2)*

Your platform has extensive monitoring — uptime, latency, error rates,
deployment frequency. The dashboards exist. Nobody looks at them regularly.
When incidents happen, the team investigates reactively. How do you fix this?

- *Level 1 response:* Identifies that the feedback loops are not closing —
  data exists but does not lead to action. May propose alerts or regular
  review meetings.
- *Level 2 response:* Redesigns the feedback loops — replaces passive
  dashboards with active mechanisms: alerts tied to specific thresholds
  that trigger specific actions, a weekly review cadence with a defined
  agenda, and automated responses for known patterns. The design starts
  from "what decisions need data?" rather than "what data can we show?"
- *Facilitator note:* Level 2 designs loops that close, not just data
  that exists.

**Scenario FM-2: The Experiment** *(boundary 2→3)*

You believe that adding IDE-integrated platform commands would reduce
developer context-switching and improve adoption. Your tech lead says
"just build it and see." How do you approach this?

- *Level 2 response:* Builds it based on the design insight, gathers
  feedback after launch, iterates based on what developers say.
- *Level 3 response:* Frames it as an experiment — defines the hypothesis
  ("IDE integration will reduce context-switching by X% and increase
  platform adoption by Y%"), identifies what to measure before building,
  sets success/failure criteria, ships the smallest testable version, and
  measures against the criteria.
- *Facilitator note:* Level 3 treats improvement as experiment, not just
  feature delivery.

## Strategic Thinking Scenarios

**Scenario ST-1: The Build vs Buy Decision** *(boundary 1→2)*

Your team has been maintaining a custom CI/CD pipeline for 2 years. A
commercial product has emerged that covers 80% of your use cases. Your
team is split on whether to migrate. How do you decide?

- *Level 1 response:* Maps the landscape — positions the CI/CD component
  on the evolution curve, understands it is commoditising. Recommends
  evaluating the commercial product seriously.
- *Level 2 response:* Translates the strategic analysis into a design
  decision — "the 80% that is commodity should move to the product; the
  20% that is our differentiator should remain custom. Here is the
  integration architecture that supports this split, and here is how we
  maintain optionality if the product does not evolve as expected."
- *Facilitator note:* Level 2 turns strategic insight into a specific,
  defensible design decision.

**Scenario ST-2: The Investment Pitch** *(boundary 2→3)*

Your CTO asks you to justify continued platform investment. Developer
teams are happy, but the finance team sees the platform as a cost centre.
You need to make the case for increased investment in the next budget cycle.

- *Level 2 response:* Presents the platform's value in terms of developer
  experience improvements and technical achievements.
- *Level 3 response:* Presents in business terms — developer productivity
  gains (quantified), time-to-market acceleration, risk reduction,
  operational cost trends. Uses Wardley Mapping to show strategic
  positioning: where the platform prevents vendor lock-in, where it
  enables faster response to market changes, where underinvestment
  creates organisational risk.
- *Facilitator note:* Level 3 speaks the language of business strategy,
  not just engineering value.

## Human and Cultural Dimensions Scenarios

**Scenario HC-1: The Resistant Team** *(boundary 1→2)*

A team of experienced developers refuses to use your platform's golden
path. They say "we've been deploying our way for years and it works fine."
Their deployment process is manual, error-prone, and undocumented.

- *Level 1 response:* Understands through empathy-driven exploration why
  they resist — discovers they fear losing control, distrust automation
  they do not understand, and feel their expertise is being devalued.
- *Level 2 response:* Co-designs a migration path *with* the team rather
  than mandating one. Starts from what they value (control, understanding)
  and designs a golden path variant that preserves those values while
  adding safety — perhaps starting with observability (so they can see
  what happens) before automation (which changes what happens).
- *Facilitator note:* Level 2 designs with the team's values, not against
  their resistance.

**Scenario HC-2: The Adoption Cliff** *(boundary 2→3)*

Your platform has strong adoption among new teams (they start on the
golden path) but legacy teams are not migrating. Leadership is
considering mandating adoption. You are asked for your recommendation.

- *Level 2 response:* Recommends against mandating and instead improving
  the migration experience — better docs, migration tooling, support.
- *Level 3 response:* Analyses the adoption dynamics — distinguishes
  between teams that resist because of rational concerns (real migration
  cost, real workflow differences) and teams that resist because of
  emotional concerns (loss of control, not-invented-here). Designs
  different strategies for each: rational concerns get addressed with
  design changes; emotional concerns get addressed with involvement,
  agency, and demonstrated value. Advises leadership on when mandate is
  appropriate (security, compliance) versus when it is counterproductive.
- *Facilitator note:* Level 3 diagnoses the adoption dynamics rather than
  defaulting to either mandate or accommodation.

**Scenario HC-3: The Multiplier Test** *(boundary 3→4)*

You have been leading platform engineering for 4 years. The organisation
now has three platform teams. You are asked: "How do we maintain quality
and coherence as we scale?"

- *Level 3 response:* Proposes standards, review processes, and governance
  structures to maintain quality.
- *Level 4 response:* Focuses on building capability, not just controls —
  mentors platform leads in the other teams, establishes a community of
  practice, teaches the framework so others can make good decisions
  independently. Designs governance that balances consistency with
  autonomy. Asks: "How do I make myself replaceable?"
- *Facilitator note:* Level 4 builds capacity for quality rather than
  personally gatekeeping it.
