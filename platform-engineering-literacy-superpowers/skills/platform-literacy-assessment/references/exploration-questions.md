# Guided Exploration Question Bank

Use these questions to probe dimensions where the Quick Scan shows interesting
signals — boundary placements, surprising gaps, or split profiles. The goal
is to distinguish between knowing the vocabulary and having internalised the
thinking.

Each question targets a specific level boundary. The facilitator notes
describe what responses at each level typically sound like.

## Context Awareness

**Boundary 0→1: From awareness to systematic exploration**

1. "How do you currently find out what your platform's users need?"
   - *Level 0 signal:* Describes informal channels — "they tell us in Slack" or "we get tickets." The sensing is reactive and ad hoc.
   - *Level 1 signal:* Describes structured methods — user interviews, journey mapping, Wardley Mapping sessions. The sensing is deliberate and repeatable.

2. "When was the last time you discovered something surprising about how developers use your platform? How did you discover it?"
   - *Level 0 signal:* Surprise comes from complaints or incidents. Discovery is accidental.
   - *Level 1 signal:* Surprise comes from structured exploration — mapping revealed an assumption, shadowing revealed a workaround.

3. "If I asked you to map your platform's strategic landscape right now, what would you reach for?"
   - *Level 0 signal:* Reaches for a technology diagram or architecture drawing.
   - *Level 1 signal:* Reaches for a Wardley Map, value stream map, or user needs map — a tool designed to reveal strategic position, not just technical structure.

**Boundary 1→2: From exploration to design decisions**

1. "Show me a design decision you made recently. What context informed that decision?"
   - *Level 1 signal:* Can describe the context but the connection to the design decision is loose or post-hoc — "we knew about X, so we built Y."
   - *Level 2 signal:* Can trace a direct line from a specific finding (a map, a user insight, a value stream bottleneck) to a concrete design choice, and explain why other choices were rejected.

2. "How do you decide which problems to solve with the platform versus which to leave to teams?"
   - *Level 1 signal:* Decisions are based on what the team is good at building or what is requested most often.
   - *Level 2 signal:* Decisions are informed by where the platform can reduce the most cognitive load, where patterns apply, and where abstraction adds genuine value.

3. "Tell me about a time your initial understanding of a problem changed during design. What changed and why?"
   - *Level 1 signal:* Change came from implementation discovery — "we found it was harder than we thought."
   - *Level 2 signal:* Change came from design-time exploration — co-design with developers, pattern analysis, or deeper context mapping revealed a different problem than originally assumed.

**Boundary 2→3: From design to living systems**

1. "How do you keep your understanding of the platform landscape current?"
   - *Level 2 signal:* Produces maps and analyses periodically but they tend to go stale. Context gathering is an event, not a practice.
   - *Level 3 signal:* Has continuous mechanisms — regular mapping sessions, automated signals, feedback loops that update understanding without requiring a dedicated effort.

2. "When the organisation's strategy shifts, how quickly does your platform's direction respond?"
   - *Level 2 signal:* Responds after the shift becomes obvious — the platform catches up to organisational change.
   - *Level 3 signal:* Strategic sensing is fast enough that the platform evolves alongside organisational direction, sometimes anticipating shifts.

3. "How do you balance what your maps tell you with what stakeholders are asking for?"
   - *Level 2 signal:* Maps inform the team's thinking but stakeholder requests drive priorities.
   - *Level 3 signal:* Can use maps to have strategic conversations with stakeholders — showing them why their request might not be the highest-leverage investment, or reframing their request in strategic terms.

**Boundary 3→4: From engineering to stewardship**

1. "If you left the team tomorrow, would strategic context awareness continue? How?"
   - *Level 3 signal:* The practice depends substantially on the individual — they drive the mapping sessions, they hold the strategic perspective.
   - *Level 4 signal:* The practice is embedded in team routines, other people can facilitate mapping sessions, and strategic awareness is distributed rather than concentrated.

2. "How do you help others develop their own ability to see the platform landscape?"
   - *Level 3 signal:* Shares findings and conclusions. Teaches by showing results.
   - *Level 4 signal:* Teaches the methods themselves — mentors others through mapping, facilitates their first strategic conversations, creates conditions for others to develop situational awareness independently.

3. "Describe a time you had to maintain strategic coherence across multiple teams or over a long time horizon."
   - *Level 3 signal:* Can describe maintaining coherence within their own team's work over quarters.
   - *Level 4 signal:* Can describe maintaining coherence across organisational boundaries, through leadership changes, or over multi-year horizons — and the specific practices they used to do it.

## Cognitive Load Design

**Boundary 0→1: From recognising load to diagnosing it**

1. "Walk me through the last developer workflow you looked at critically. Where was the unnecessary complexity?"
   - *Level 0 signal:* Can point to obvious friction — "the deploy process has too many steps" — but the analysis is surface-level.
   - *Level 1 signal:* Can trace the workflow step by step, identifying where context is lost, where representational state breaks, and where cognitive load shifts from intrinsic to extraneous.

2. "How do you distinguish between complexity that is genuinely necessary and complexity that the platform is adding unnecessarily?"
   - *Level 0 signal:* Has an intuitive sense but cannot articulate a systematic distinction.
   - *Level 1 signal:* Can apply a structured lens — intrinsic vs extraneous vs germane load — and give specific examples of each in their platform.

3. "What tools or techniques do you use to diagnose cognitive load?"
   - *Level 0 signal:* Relies on developer complaints or personal experience.
   - *Level 1 signal:* Uses structured techniques — workflow tracing, developer shadowing, cognitive walkthroughs.

**Boundary 1→2: From diagnosis to design**

1. "Tell me about a platform feature you designed specifically to reduce cognitive load. How did you know it worked?"
   - *Level 1 signal:* Can describe features that happen to reduce load, but the load reduction was not the explicit design intent — or cannot show evidence it worked.
   - *Level 2 signal:* Can describe a feature where cognitive load reduction was the primary design goal, and can point to evidence (developer feedback, adoption rates, error reduction) that it succeeded.

2. "How do you evaluate a proposed platform feature against cognitive load?"
   - *Level 1 signal:* Considers it informally — "this seems simpler."
   - *Level 2 signal:* Has an explicit evaluation — applies the 4pm Friday test, considers the worst reasonable conditions, and can articulate exactly what load is added and what load is removed.

3. "When was the last time you rejected or redesigned a feature because it added too much cognitive load?"
   - *Level 1 signal:* Cannot recall a specific instance, or the rejection was based on general complexity concerns.
   - *Level 2 signal:* Can describe a specific instance with the reasoning — what load it would have added, for whom, and what the alternative was.

**Boundary 2→3: From design to measurement**

1. "How do you measure cognitive load in your platform today?"
   - *Level 2 signal:* Relies on qualitative signals — developer satisfaction surveys, anecdotal feedback, personal observation.
   - *Level 3 signal:* Has quantitative measures alongside qualitative — workflow completion times, error rates, onboarding time, context-switching frequency — and uses them to prioritise.

2. "How do you decide which cognitive load problems to fix first?"
   - *Level 2 signal:* Prioritises by intuition or developer loudness — the most complained-about friction gets fixed first.
   - *Level 3 signal:* Prioritises by measured impact — which load sources affect the most developers, the most critical workflows, or the highest-value activities.

3. "Show me how cognitive load considerations have changed your roadmap."
   - *Level 2 signal:* Cognitive load is a design consideration within features but does not drive roadmap prioritisation.
   - *Level 3 signal:* Cognitive load measurement directly influences what the team builds next — it is a first-class input to planning.

**Boundary 3→4: From measurement to organisational practice**

1. "Do teams outside your immediate platform team consider cognitive load when making design decisions?"
   - *Level 3 signal:* The platform team considers it; other teams benefit from it but do not think in those terms.
   - *Level 4 signal:* Cognitive load is an organisational design constraint — other teams apply it to their own work, and the platform team helped establish that practice.

2. "How would cognitive load management continue if you were not advocating for it?"
   - *Level 3 signal:* It would degrade — the practice depends on the individual or a small group of champions.
   - *Level 4 signal:* It is embedded in processes, review criteria, and team culture — it would sustain itself.

## Pattern Application

**Boundary 0→1: From naming to evaluating**

1. "Pick any three of the ten platform patterns. How do they show up — or fail to show up — in your current platform?"
   - *Level 0 signal:* Can name the patterns and give textbook descriptions but struggles to connect them to their own platform.
   - *Level 1 signal:* Can give specific, grounded examples — "our self-service is partial because X still requires a ticket" or "our guardrails exist for deployment but not for infrastructure provisioning."

2. "Which pattern do you think your platform does best? Which is weakest?"
   - *Level 0 signal:* Answers in general terms — "we're good at self-service."
   - *Level 1 signal:* Answers with specifics and evidence — "our golden path for microservice creation is strong because 80% of teams use it voluntarily, but our observability pattern is weak because developers can't see what the platform does on their behalf during deployment."

**Boundary 1→2: From evaluating to designing**

1. "Tell me about a platform feature you designed. Which patterns did you apply, and were there tensions between them?"
   - *Level 1 signal:* Can retrospectively identify which patterns a feature embodies, but didn't consciously use the patterns during design.
   - *Level 2 signal:* Consciously selected patterns during design and can describe tensions — "we had to balance self-service against guardrails because full self-service would have allowed unsafe configurations."

2. "How do you involve developers in validating your pattern choices?"
   - *Level 1 signal:* Gets feedback after building — "we shipped it and asked what they thought."
   - *Level 2 signal:* Co-designs — runs workshops, tests prototypes, validates pattern choices before committing to implementation.

3. "Tell me about a time you chose *not* to apply a pattern. What was the situation and how did you decide?"
   - *Level 1 signal:* Cannot recall a deliberate omission, or omitted a pattern because it seemed too hard.
   - *Level 2 signal:* Made a deliberate design choice — "we chose not to build extensibility here because the use cases are well-known and the cost of extension points would add complexity without clear benefit."

**Boundary 2→3: From designing to shipping incrementally**

1. "How do you deliver a complex pattern like Composability or Extensibility? Do you ship it all at once or incrementally?"
   - *Level 2 signal:* Designs the full pattern and delivers it as a project — a single release or a small number of large releases.
   - *Level 3 signal:* Slices the pattern into the smallest viable increments — ships the first useful slice, measures adoption and feedback, and iterates.

2. "How do you know when a pattern is working in practice, not just in design?"
   - *Level 2 signal:* Relies on adoption or developer feedback — "people are using it, so it works."
   - *Level 3 signal:* Has specific measures — adoption rates, time-to-value, error rates, cognitive load impact — and uses them to iterate on the pattern's implementation.

3. "Tell me about a pattern that didn't work as designed. What happened and how did you adapt?"
   - *Level 2 signal:* Redesigned the feature based on feedback.
   - *Level 3 signal:* Ran a systematic learning loop — measured what went wrong, hypothesised why, tested the hypothesis, and shipped a refined version. Can show the evidence trail.

**Boundary 3→4: From shipping to evolving the language**

1. "Has your team identified any patterns that the standard ten don't cover?"
   - *Level 3 signal:* Applies the existing ten patterns effectively but hasn't needed to extend them.
   - *Level 4 signal:* Has identified patterns unique to their context — "we found we needed an explicit Data Sovereignty pattern because none of the ten fully addressed our regulatory constraints" — and can describe how it relates to the existing pattern language.

2. "How do you govern pattern application across multiple teams?"
   - *Level 3 signal:* Ensures their own team applies patterns well but doesn't govern cross-team consistency.
   - *Level 4 signal:* Has established contribution standards, quality gates, and review practices for how patterns are applied across the organisation.

## Feedback and Measurement

**Boundary 0→1: From understanding importance to mapping loops**

1. "What feedback loops exist in your platform today? How fast do they close?"
   - *Level 0 signal:* Can identify that feedback exists ("we have monitoring") but cannot describe the loop — who sees the signal, what action it triggers, and how quickly.
   - *Level 1 signal:* Can map specific OODA loops — observe what, orient how, decide what, act when — and identify where they are slow or broken.

2. "What is the difference between a leading and lagging indicator for your platform? Give me an example of each."
   - *Level 0 signal:* Struggles to distinguish or gives textbook examples not grounded in their own platform.
   - *Level 1 signal:* Gives specific examples — "deploy frequency is a lagging indicator of developer experience improvement; time-to-first-deploy for a new joiner is a leading indicator."

3. "Where are the feedback gaps — places where your platform produces no signal about how it is performing?"
   - *Level 0 signal:* Has not systematically looked for gaps.
   - *Level 1 signal:* Can identify specific blind spots — "we have no signal on how long developers spend understanding platform errors before finding the right action."

**Boundary 1→2: From mapping to designing**

1. "Tell me about a feedback loop you designed into a platform capability. How did you decide what to measure?"
   - *Level 1 signal:* Added monitoring or metrics to an existing feature but the feedback loop was not part of the original design.
   - *Level 2 signal:* Designed the feedback loop as part of the capability — knew from the start what needed to be measured and how the data would close the loop.

2. "How do you ensure that data from your feedback loops leads to action rather than sitting in a dashboard?"
   - *Level 1 signal:* Acknowledges this is a problem — "we have dashboards but nobody looks at them regularly."
   - *Level 2 signal:* Has designed specific mechanisms — alerts, review cadences, automated responses — that ensure signals lead to decisions.

3. "When you instrument something, how do you decide what to measure versus what to ignore?"
   - *Level 1 signal:* Measures what is easy to measure or what is standard practice (DORA metrics, uptime).
   - *Level 2 signal:* Measures what informs specific decisions — can articulate "we measure X because it tells us Y, which helps us decide Z."

**Boundary 2→3: From designing to operating**

1. "Show me your platform scorecard. What does it track and how do you use it?"
   - *Level 2 signal:* Has metrics and dashboards but no integrated scorecard — measurements are scattered and not used systematically for decisions.
   - *Level 3 signal:* Has a running scorecard tracking quantitative and qualitative health, reviews it regularly, and can show decisions it has influenced.

2. "Describe your most recent experiment-driven improvement. What was the hypothesis, what did you measure, and what did you learn?"
   - *Level 2 signal:* Builds improvements based on feedback but doesn't run formal experiments — "developers asked for X, so we built it."
   - *Level 3 signal:* Can describe a complete experiment loop — hypothesis, measurement plan, result, and what changed as a result.

3. "How do you run continuous discovery for your platform?"
   - *Level 2 signal:* Gathers feedback periodically (surveys, retros) but discovery is episodic.
   - *Level 3 signal:* Has continuous mechanisms — regular developer interviews, usage analytics, feedback channels with review cadences.

**Boundary 3→4: From operating to organisational practice**

1. "Do teams outside the platform team use measurement to drive their own platform-related decisions?"
   - *Level 3 signal:* The platform team measures well; other teams consume the results but do not drive their own measurement.
   - *Level 4 signal:* Measurement culture has spread — domain teams measure their own platform interactions and contribute data back.

2. "How would your measurement practices continue if you moved to a different team?"
   - *Level 3 signal:* The practices would degrade without the individual driving them.
   - *Level 4 signal:* The practices are embedded in team routines, tooling, and culture.

## Strategic Thinking

**Boundary 0→1: From awareness to mapping**

1. "When you last made a significant platform technology choice, what information did you base it on?"
   - *Level 0 signal:* Based on technical merit, team familiarity, or industry trends — "we chose Kubernetes because everyone uses it."
   - *Level 1 signal:* Considered strategic positioning — where the technology sits on the evolution curve, what alternatives exist, and what the implications of the choice are over time.

2. "How do you think about the build/buy/partner decision for platform components?"
   - *Level 0 signal:* Decides based on capability or cost — "we can build it" or "the vendor tool is cheaper."
   - *Level 1 signal:* Uses evolutionary positioning — builds custom where it is a differentiator, buys commodity where the market has evolved, partners where neither extreme fits.

3. "What would change about your platform if your organisation's strategy shifted significantly?"
   - *Level 0 signal:* Has not connected platform decisions to organisational strategy — the platform is seen as a technical concern.
   - *Level 1 signal:* Can identify specific platform components that would need to change and why — "if we pivot to B2B, our multi-tenancy abstractions become critical and need to move from custom to commodity."

**Boundary 1→2: From mapping to design influence**

1. "Show me a design decision that was directly informed by strategic analysis. What was the analysis and what did it change?"
   - *Level 1 signal:* Has strategic awareness but it lives alongside design decisions rather than driving them.
   - *Level 2 signal:* Can trace a direct line — "the Wardley Map showed this component is commoditising, so we designed for replaceability rather than deep integration."

2. "How do you balance strategic positioning with immediate developer needs?"
   - *Level 1 signal:* Treats them as separate concerns — strategic thinking happens in planning, developer needs drive day-to-day.
   - *Level 2 signal:* Integrates them — makes design decisions that serve immediate needs while maintaining strategic optionality.

**Boundary 2→3: From design influence to strategic leadership**

1. "How do you justify platform investment to non-technical stakeholders?"
   - *Level 2 signal:* Justifies in technical terms that stakeholders accept but may not deeply understand.
   - *Level 3 signal:* Justifies in business terms — connects platform investment to developer productivity, time-to-market, risk reduction, and organisational agility, using data.

2. "Describe your platform's 3-year technology evolution plan. What is commoditising, what is emerging, and what are you building?"
   - *Level 2 signal:* Has a roadmap but it is feature-driven rather than evolution-driven.
   - *Level 3 signal:* Has an evolution-aware plan — knows what to build now, what to buy as it commoditises, and where to invest ahead of the curve.

**Boundary 3→4: From strategic leadership to stewardship**

1. "How do you maintain strategic coherence when leadership priorities change?"
   - *Level 3 signal:* Adapts the platform strategy to new leadership priorities.
   - *Level 4 signal:* Maintains strategic coherence *through* leadership changes — can show how the platform strategy evolved while preserving its core direction.

2. "How do you coordinate strategy across multiple platform teams or domains?"
   - *Level 3 signal:* Coordinates within their own team's scope.
   - *Level 4 signal:* Facilitates cross-team strategic alignment — runs coordination practices, resolves strategic conflicts, and maintains a coherent organisational platform strategy.

## Human and Cultural Dimensions

**Boundary 0→1: From recognising people matter to empathy-driven exploration**

1. "When did you last spend time watching a developer use your platform? What did you learn?"
   - *Level 0 signal:* Has not done this, or did it informally and long ago.
   - *Level 1 signal:* Does this deliberately and recently — can describe specific insights from developer shadowing or interviews.

2. "How do you find out what developers actually think about the platform, as opposed to what they say in formal feedback?"
   - *Level 0 signal:* Relies on formal channels — surveys, retros, support tickets.
   - *Level 1 signal:* Uses empathy-driven methods — informal conversations, contextual inquiry, observing workarounds.

3. "What has surprised you most about how developers experience your platform?"
   - *Level 0 signal:* General surprise — "they don't use it the way we expected."
   - *Level 1 signal:* Specific surprise grounded in structured exploration — "during shadowing, we discovered that developers were copying configuration from a shared doc rather than using our self-service tool, because the tool's terminology didn't match their mental model."

**Boundary 1→2: From exploration to co-design**

1. "Tell me about a platform feature that was shaped by developer input during design, not just after launch."
   - *Level 1 signal:* Gathered requirements from developers before building, but the design was done by the platform team.
   - *Level 2 signal:* Co-designed — developers were in the room during design sessions, their input changed the design direction, and the result reflects their contribution.

2. "How do you handle conflicting needs between different developer groups?"
   - *Level 1 signal:* Picks the most common need or the loudest voice.
   - *Level 2 signal:* Uses structured facilitation — surfaces the different perspectives, identifies shared needs, and designs solutions that address the underlying problem rather than the surface requests.

3. "When you catch yourself designing *for* developers rather than *with* them, what do you do?"
   - *Level 1 signal:* Does not recognise this distinction consistently.
   - *Level 2 signal:* Recognises it and has a corrective habit — stops, involves developers, adjusts the design.

**Boundary 2→3: From co-design to adoption strategy**

1. "Tell me about a platform capability that developers resisted adopting. What did you learn?"
   - *Level 2 signal:* Describes the resistance and the eventual fix, but the learning is about the technical solution.
   - *Level 3 signal:* Describes what the resistance revealed about emotional and rational dimensions — "they resisted because it felt like a loss of control, not because the tool was bad. We redesigned the rollout to give them more agency."

2. "How do you build support for platform investment across the organisation?"
   - *Level 2 signal:* Relies on the quality of the platform work to speak for itself, or on management mandate.
   - *Level 3 signal:* Actively builds coalitions — identifies champions, manages stakeholder relationships, addresses political dynamics.

3. "How do you decide between mandating adoption and making adoption voluntary?"
   - *Level 2 signal:* Defaults to one approach or decides based on urgency.
   - *Level 3 signal:* Makes a deliberate choice based on context — understands when mandate is appropriate (security, compliance) versus when voluntary adoption is more sustainable, and designs the rollout accordingly.

**Boundary 3→4: From adoption strategy to teaching and community**

1. "How do you help other platform engineers develop their skills?"
   - *Level 3 signal:* Mentors informally — answers questions, reviews work, shares knowledge when asked.
   - *Level 4 signal:* Mentors deliberately — has a teaching practice, can see others' growth over time, creates structured learning opportunities.

2. "When you solve a platform problem, what happens to the learning?"
   - *Level 3 signal:* Documents the solution for the team.
   - *Level 4 signal:* Shares the learning, not just the solution — teaches the reasoning, the diagnosis, the principles, so others can solve similar problems independently.

3. "Is there a community of practice around platform engineering in your organisation? What role do you play in it?"
   - *Level 3 signal:* Participates in communities if they exist.
   - *Level 4 signal:* Has helped create or sustain a community of practice — facilitates sessions, brings in outside perspectives, creates conditions for collective learning.
