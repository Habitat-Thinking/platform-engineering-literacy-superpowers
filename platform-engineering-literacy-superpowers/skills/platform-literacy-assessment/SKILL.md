---
name: platform-literacy-assessment
description: Run a Platform Engineering Literacy Assessment (PELA) — guides individuals, instructors, or teams through a three-phase protocol (Quick Scan, Guided Exploration, Deep Dive) to determine literacy levels across six dimensions, then produces a layered assessment output with development recommendations.
---

# Platform Engineering Literacy Assessment (PELA)

This skill facilitates the Platform Engineering Literacy Assessment (PELA)
interactively. It implements the three-phase assessment protocol using the
rubric, question bank, and scenario bank in the `references/` directory.

## When to use

- A practitioner wants to understand their current literacy level
- An instructor needs to place learners before a course
- A platform team wants a collective diagnostic
- Someone asks to "assess my literacy", "where am I on the framework",
  "run an assessment", "check my level", "run a PELA", or "run the PELA"

## What this skill does NOT do

- It does not certify or gatekeep — the output is developmental, not a credential
- It does not override self-assessment without explaining why — if the
  conversation suggests a different level than claimed, say so transparently
- It does not assess dimensions it has not explored — confidence levels must
  be honest about which phases were completed

## Protocol

### Phase 1: Establish Context

Before starting the rubric, ask:

1. **Who is being assessed?** Individual or team?
2. **What prompted this assessment?** Starting a course? Mid-career
   reflection? Team planning? This context helps you tailor the
   conversation and the roadmap.
3. **Is there a previous assessment?** Check `assessments/` for existing
   files matching the person's name. If found, note the previous profile
   for longitudinal comparison.

### Phase 2: Quick Scan

Read the rubric from `references/quick-scan-rubric.md`. Walk through the
six dimensions one at a time. For each dimension:

1. Present the dimension description and all five level descriptors
2. Ask the person to select the one that best describes their *consistent*
   capability
3. Ask a brief calibration question: "Why did you pick that level?" or
   "What makes you confident about that placement?"
4. Record the selection and any calibration notes

After all six dimensions, present the **provisional profile**:

- A table showing the level for each dimension
- The overall dominant level (using dominant-pattern placement)
- Any interesting signals: wide splits, boundary placements, surprises

### Phase 3: Guided Exploration

Analyse the provisional profile and identify 2-3 dimensions to explore.
Read the questions from `references/exploration-questions.md`.

**Prioritise exploring when:**

- Two dimensions are 2+ levels apart (wide split)
- A dimension is at a level boundary where the calibration answer was thin
- The overall profile shows a recognisable pattern (Technical-Human Split,
  Thinker-Doer Split, Spiky Expert) that warrants investigation

For each selected dimension:

- Use questions targeting the relevant level boundary
- Listen for competence markers and fluency habits in the responses
- If the conversation reveals a different level than the self-rating,
  explain what you heard and propose an adjustment — do not silently change
  the placement

After exploration, present the **confirmed profile** with updated levels
and Medium confidence for explored dimensions.

### Phase 4: Deep Dive (Offer, Do Not Assume)

After presenting the confirmed profile, offer the Deep Dive:

> "For the dimensions where you'd like more confidence in the placement, I
> can present realistic scenarios for you to work through, or you can share
> artefacts (maps, designs, docs) that demonstrate your capability. Would
> you like to go deeper on any dimension?"

If accepted, read scenarios from `references/scenario-bank.md`:

- Present scenarios for the relevant dimension and level boundary
- For evidence review, ask the person to describe or share the artefact,
  then evaluate against the competence markers for the claimed level
- Update confidence to High for dimensions that complete Deep Dive

### Phase 5: Produce Output

Read scoring guidance from `references/scoring-and-roadmap.md`. Generate
the PELA assessment document with this structure:

```yaml
---
type: pela
version: 1.0
date: YYYY-MM-DD
subject: individual | team
name: "the person's name"
assessor: claude
phases_completed: [quick-scan, guided-exploration] # or [quick-scan, guided-exploration, deep-dive]
---
```

**Headline:** One sentence with the dominant pattern.
Example: "Solidly Level 2 (Designer), with Level 3 emerging in Strategic
Thinking and a Level 1 gap in Feedback and Measurement."

**Dimensional Profile:** Table with Level, Confidence, and Notes for each
dimension.

**Development Roadmap:** For each dimension where growth is actionable:

- Gap identified
- Recommended course modules (use the dimension-to-module mapping in
  `references/scoring-and-roadmap.md`)
- Fluency habit to develop (use the dimension-to-habit mapping)
- Suggested evidence for the next assessment

**Longitudinal Comparison:** If a previous assessment exists, add a
comparison table showing movement per dimension.

Create the `assessments/` directory if it does not exist, then save the
output to `assessments/YYYY-MM-DD-<name>.md` where `<name>` is the
person's name in lowercase with hyphens.

## Team Mode

When assessing a team:

1. Run individual Quick Scans for each member (or ask them to complete the
   Quick Scan from `references/quick-scan-rubric.md` beforehand)
2. Aggregate into a team profile:
   - For each dimension, show the distribution of levels (e.g., "Context
     Awareness: 1×L0, 2×L1, 3×L2, 1×L3")
   - Identify **collective gaps** — dimensions where most members cluster
     at the same level
   - Identify **coverage gaps** — dimensions where no team member is above
     Level 1
3. Produce a team-level Development Roadmap focusing on collective gaps
4. Save to `assessments/YYYY-MM-DD-team-<team-name>.md`

## Key References

- Quick Scan rubric: `references/quick-scan-rubric.md`
- Exploration questions: `references/exploration-questions.md`
- Scenario bank: `references/scenario-bank.md`
- Scoring and roadmap: `references/scoring-and-roadmap.md`
- Full framework: <https://github.com/russmiles/platform-engineering-literacy>
- Previous assessments: `assessments/`
