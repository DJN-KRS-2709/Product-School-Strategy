# Content Atom Schema

**Purpose:** Define the structure of a content atom — the smallest unit of teachable knowledge in the shared library. Every concept, framework, case study, and external signal follows this schema.

---

## Atom Types

| Type | Definition | Example |
|------|-----------|---------|
| `concept` | A named idea with a canonical definition and context for when it applies | "Deterministic vs. Probabilistic Software" |
| `framework` | A reusable mental model with structure, steps, or scoring criteria | "5 AI Value Archetypes" |
| `evidence` | A case study, data point, stat, or real-world example | "Klarna Automator Overcorrection (Bet → Crack → Correction)" |
| `signal` | A raw or lightly processed external input with extracted insight | "Gokul Rajaram: brand is not a moat anymore" |

---

## Atom Structure

Every atom is a markdown file with YAML frontmatter for metadata and a body for content.

### Frontmatter (Required Fields)

```yaml
---
id: "confidence-ux"                          # Unique, URL-safe identifier
title: "Confidence UX"                       # Human-readable name
type: "framework"                            # concept | framework | evidence | signal
confidence: "validated"                      # validated | emerging | speculative

created: "2026-04-03"                        # Date atom was created
last_verified: "2026-04-03"                  # Date content was last verified as accurate
verification_sla_days: 180                   # Days before atom needs re-verification

sources:
  - citation: "AI Product Strategy Certification — Module 4 Speaker Notes"
    url: ""
    date: "2026-03-01"
  - citation: "Lenny's Newsletter: Beyond vibe checks (Aman Khan)"
    url: "https://www.lennysnewsletter.com/p/beyond-vibe-checks"
    date: "2025-04-15"

tags:
  - "trust"
  - "ux-design"
  - "probabilistic-output"
  - "ai-product-design"

audience_level: "senior"                     # foundational | intermediate | senior

courses_referencing:                         # Auto-maintained; which courses use this atom
  - course: "ai-product-strategy"
    modules: ["m4"]
    depth: "deep"                            # mention | moderate | deep
    required: true                            # true if module cannot meet outcome without this atom
  - course: "ai-for-pms"
    modules: ["m4"]
    depth: "moderate"
    required: false
---
```

### Frontmatter (Optional Fields)

```yaml
supersedes: "old-confidence-scoring"         # ID of atom this replaces
superseded_by: ""                            # ID of atom that replaces this one
related_atoms:                               # Cross-references to related atoms
  - "trust-gaps"
  - "golden-dataset"
  - "reliability-contract"
module_dependencies:                         # Packaging guidance for course and enterprise use
  requires_atoms:
    - "golden-dataset"
  should_travel_with_modules:
    - course: "ai-product-strategy"
      module: "m4"
      reason: "Eval dashboard concepts need the reliability contract setup"
  standalone: false
  enterprise_repackaging_notes: "Remove AI Product Strategy course-arc references and restate the client-specific outcome."
delivery_outputs:                            # Generated artifacts that consume this atom
  - "slides"
  - "speaker-notes"
  - "student-notes"
  - "lms-page"
  - "enterprise-handout"
deprecated: false                            # If true, atom is archived
deprecation_reason: ""                       # Why it was deprecated
contributed_by: "dejan-krstic"               # Who created/last updated
review_notes: ""                             # Notes from last verification review
```

### Body Structure

The body follows a consistent structure adapted per atom type.

## Module Contract Layer

Atoms define reusable knowledge. Module contracts define how that knowledge becomes a teachable package for live courses, on-demand learning, and enterprise programs. A module contract should live next to the course material and reference atoms by ID rather than duplicating canonical content.

```yaml
---
id: "ai-product-strategy-m4"
title: "The Contract"
course: "ai-product-strategy"
module_number: 4
learning_outcome: "Define how an AI product earns trust through evals, reliability promises, and escalation paths."

required_atoms:
  - "confidence-ux"
  - "golden-dataset"
  - "reliability-contract"
optional_atoms:
  - "air-canada-chatbot"

dependency_rules:
  standalone: false
  prerequisites:
    - "ai-product-strategy-m1"
  should_travel_with:
    - module: "ai-product-strategy-m3"
      reason: "Trust contract depends on understanding AI economics and cost trade-offs."

source_inputs:
  slides: "modules/m4/slides.md"
  speaker_notes: "modules/m4/speaker-notes.md"
  activity_instructions: "modules/m4/activity.md"
  recordings:
    - "2026-05-01-live-session"

generated_outputs:
  - "slides"
  - "instructor-guide"
  - "student-notes"
  - "lms-page"
  - "enterprise-package"

enterprise_repackaging:
  remove_references:
    - "previous module"
    - "living strategy builder"
  rewrite_guidance: "Anchor the module in the client's target AI product outcome before introducing eval mechanics."
---
```

#### For `concept` atoms:

```markdown
## Definition

[1-3 sentence canonical definition. This is the source of truth across all courses.]

## Why It Matters

[Context: when and why a PM needs this concept. 2-4 sentences.]

## How It Works

[Explanation with appropriate depth. Use tables, lists, or diagrams as needed.]

## Teaching Notes

[Guidance for instructors: what to emphasize, common misunderstandings, 
what makes this concept click for students.]

## Course-Specific Applications

### AI Product Strategy (M4)
[How this concept is applied in this specific course context.]

### AI for PMs (M4)
[How this concept is applied differently here.]
```

#### For `framework` atoms:

```markdown
## The Framework

[Visual representation: table, diagram, or structured list. 
This is the canonical version all courses reference.]

## When to Use It

[Decision criteria: when does this framework apply? When does it NOT apply?]

## How to Apply It

[Step-by-step or guided application. Practical, not theoretical.]

## Adaptation Guidance

[Per the AI Product Strategy design principle: "If someone's artifact looks 
exactly like the template, that's a smell." How should PMs adapt this to 
their context?]

## Teaching Notes

[Instructor guidance: common pitfalls, what makes it land, 
what follow-up questions to expect.]

## Course-Specific Depth

### [Course Name] ([Module])
[How this framework is taught at what depth in each course.]
```

#### For `evidence` atoms:

```markdown
## The Story

[What happened? Who was involved? What was the outcome? 
Factual, sourced, with dates.]

## The Lesson

[What does this teach? 1-2 sentences.]

## Teaching Format

[How to present this: 3-act structure (Bet → Crack → Correction), 
quick aside, deep case study, etc.]

## Key Data Points

[Specific numbers, stats, quotes that make this evidence compelling. 
Each with source attribution.]

## Verification Notes

[When was this last fact-checked? Any updates to the story since 
initial capture?]
```

#### For `signal` atoms:

```markdown
## Source

[Full citation: author, publication, date, URL]

## Raw Insight

[What was said or observed? Direct quotes preferred.]

## Extracted Takeaway

[What does this mean for Product School's curriculum? 1-3 sentences.]

## Potential Course Applications

[Which courses/modules could benefit from this signal? How?]

## Maturity Assessment

[Is this validated by other sources? Is it contradicted? 
What would it take to promote this to "emerging" or "validated"?]
```

---

## Confidence Levels — Detailed Criteria

Adapted from the AI Product Strategy course's three-tier Confidence UX model.

### Validated

**Criteria:**
- Supported by 2+ credible, independent sources
- Taught in at least one cohort with positive student signal
- Core definition stable for 3+ months
- Peer-reviewed by at least one content lead

**Course author guidance:** Use directly in materials. Cite as established knowledge.

**Verification cadence:** Per type SLA (60–180 days).

### Emerging

**Criteria:**
- Supported by 1 credible source OR recent industry publication
- Not yet tested in classroom delivery
- May represent a trend that hasn't fully developed

**Course author guidance:** Use with qualification ("recent research suggests...", "emerging practice shows..."). Flag for validation in next cohort delivery. Note student reaction for promotion decision.

**Verification cadence:** Every 60 days — emerging knowledge changes fast.

### Speculative

**Criteria:**
- Based on a single signal: trending post, conference talk, Reddit discussion, early-stage research
- No corroboration from independent sources
- May be provocative, contrarian, or unproven

**Course author guidance:** Do NOT use in course materials without escalation to content lead. Suitable for: internal research tracking, instructor FYI, future investigation queue.

**Verification cadence:** Every 30 days — either promote with evidence or archive.

---

## Naming Conventions

### Atom IDs

- Lowercase, hyphen-separated: `agent-spectrum`, `confidence-ux`, `klarna-automator`
- Descriptive, not abbreviated: `data-flywheel` not `df`
- Framework names use the framework name: `five-ai-value-archetypes`
- Case studies use company + topic: `jasper-chatgpt-encroachment`
- Signals include source shorthand: `lenny-evals-guide-2025`

### File Organization

```
library/
├── concepts/
│   ├── deterministic-vs-probabilistic.md
│   ├── trust-not-accuracy.md
│   └── comprehension-debt.md
├── frameworks/
│   ├── agent-spectrum.md
│   ├── five-ai-value-archetypes.md
│   ├── confidence-ux.md
│   ├── data-flywheel.md
│   ├── eval-stack.md
│   └── awspec.md
├── evidence/
│   ├── klarna-automator.md
│   ├── jasper-chatgpt-encroachment.md
│   ├── air-canada-chatbot.md
│   ├── samsung-data-leak.md
│   └── duolingo-ai-transformation.md
└── signals/
    ├── lenny-evals-guide-2025.md
    ├── lenny-ai-pricing-2025.md
    ├── gokul-eight-moats-2026.md
    └── helmer-seven-powers.md
```

---

## Lifecycle

```
Signal captured (Speculative)
    ↓ evidence found + source verified
Emerging
    ↓ taught in cohort + positive signal + peer review
Validated
    ↓ SLA expires without re-verification
Flagged for Review
    ↓ re-verified
Validated (renewed)
    ↓ superseded by better atom
Deprecated (archived with rationale)
```

---

## Example Atom: Confidence UX

```yaml
---
id: "confidence-ux"
title: "Confidence UX — Making Probabilistic Output Legible"
type: "framework"
confidence: "validated"
created: "2026-04-03"
last_verified: "2026-04-03"
verification_sla_days: 180
sources:
  - citation: "AI Product Strategy Certification — Module 4: The Contract"
    url: ""
    date: "2026-03-01"
  - citation: "Lenny's Newsletter: Beyond vibe checks — Aman Khan"
    url: "https://www.lennysnewsletter.com/p/beyond-vibe-checks"
    date: "2025-04-15"
tags:
  - "trust"
  - "ux-design"
  - "probabilistic-output"
  - "ai-product-design"
audience_level: "senior"
courses_referencing:
  - course: "ai-product-strategy"
    modules: ["m4"]
    depth: "deep"
  - course: "ai-for-pms"
    modules: ["m4"]
    depth: "moderate"
related_atoms:
  - "trust-gaps"
  - "golden-dataset"
  - "reliability-contract"
  - "deterministic-vs-probabilistic"
---
```

```markdown
## The Framework

Confidence UX is the practice of surfacing an AI system's certainty level
to users — making probabilistic output legible rather than hiding uncertainty
behind a deterministic-looking interface.

Three tiers:

| Confidence Level | System Behavior | UX Treatment |
|-----------------|----------------|--------------|
| >90% (High) | Automate — act without asking | Show result with subtle provenance |
| 50–90% (Medium) | Assist — suggest with disclosure | Show result + confidence indicator + easy override |
| <50% (Low) | Flag — escalate for human review | Present options, require human decision, explain uncertainty |

## When to Use It

Apply when designing any AI feature that produces outputs users will
act on — recommendations, classifications, generated content, predictions.
Especially critical in:
- Regulated verticals (finance, healthcare, legal)
- High-stakes decisions (pricing, hiring, diagnosis)
- User-facing content generation (where hallucination has real cost)

## How to Apply It

1. Identify where your AI system produces outputs users rely on
2. Determine the system's actual confidence range for each output type
3. Map each confidence range to the appropriate UX treatment
4. Design the specific UI components: confidence indicators, override
   controls, escalation paths
5. Define what happens when confidence drops below threshold mid-session

## Adaptation Guidance

The three tiers are a starting point. Some products need finer granularity
(five tiers). Some need coarser (binary: auto vs. review). The question
to ask: "What is the cost of a wrong output at each confidence level?"
If the cost is always high (medical), skew toward human review. If the
cost is always low (playlist suggestions), skew toward automation.

## Teaching Notes

The key insight that makes this click: "Trust is not a function of accuracy.
It is a function of perceived control." Students who have shipped AI features
will immediately recognize the pattern — users who can see and override AI
decisions trust the system more than users who get better results but can't
see how they were produced.

Common misunderstanding: students assume higher accuracy always means higher
trust. The Air Canada chatbot case study is the counter-example — high
accuracy overall, but one wrong answer with no audit trail destroyed trust.

## Course-Specific Depth

### AI Product Strategy (M4: The Contract)
Deep treatment. Students build an eval dashboard spec with confidence UX
as a core component. Connected to reliability contract, golden datasets,
and HITL architecture. The framework is part of the living strategy artifact.

### AI for PMs (M4: AI-Native UX)
Moderate treatment. Presented as part of the Three Trust Gaps framework
(Black Box, Hallucination, Control). Students learn the concept but don't
build a full spec around it. Connected to AI-UX Readiness Checklist.
```
