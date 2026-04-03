# Product School — Living Content Library: Product Strategy

**Author:** Dejan Krstic, Chief Product & Technology Officer
**Date:** April 2026
**Status:** Draft v1

---

## The One-Sentence Thesis

Product School's nine certifications share a single strategic problem: **content ages faster than courses can be rewritten.** The solution is a living content library — a shared, course-agnostic knowledge layer that compounds in quality with every cohort, every customer interaction, and every external signal captured.

This strategy is structured through the same six strategic questions we teach in the AI Product Strategy certification — and the same Confidence Line we teach in Vibe Coding maps the implementation maturity. We practice what we teach.

---

## Why This Strategy Exists

### The Diagnosis

Product School operates nine certifications:

| Certification | Domain |
|---------------|--------|
| Product Management | Core PM skills |
| Go-to-Market | Positioning and distribution |
| Product Experimentation | Data-driven experimentation |
| AI Product Management | AI-powered product fundamentals |
| Vibe Coding | AI-assisted prototyping and deployment |
| AI Evals | AI evaluation pipelines |
| Advanced AI Agents | Multi-agent system design |
| Product Leadership | Leading AI product strategy |
| AI Product Strategy | Strategic AI product decision-making |

Each certification was built and is maintained independently. The AI Product Strategy course lives in its own repo with its own speaker notes, slides, meeting notes, and insights folder. The Vibe Coding certification has its own repo with its own instructor guide, its own feedback synthesis, its own competitive analysis. AI Agents has a single markdown file containing all six modules. AI for PMs has six separate files under an `Insights/` folder.

This independence served early speed. It now creates five structural problems:

**1. Framework drift.** The same concept is taught differently across courses with no canonical definition. The Agent Spectrum appears in both AI Agents (Helper → Teammate → Operator; levels 0–3) and AI for PMs (levels 0–3 with similar but not identical definitions). AWSpec is taught in both. Eval stacks appear in AI for PMs, AI Product Strategy (M4), and presumably AI Evals. Each instructor interprets and presents these independently.

**2. Content staleness.** AI capabilities change weekly. A stat, framework, or case study taught in one course becomes outdated, but there is no mechanism to propagate an update across the other eight certifications that might reference the same concept. Lenny insights are manually curated in a single markdown file (`lenny-insights.md`) inside the AI Product Strategy repo — valuable work that benefits exactly one course.

**3. Feedback silos.** Student survey data, customer success observations, and enterprise customer requests all contain signal about what content needs updating, what topics are emerging, and what is falling flat. This signal is captured in ad-hoc meeting notes, Google Doc comments, and working session transcripts — then acted on within a single course. Three cohorts of Vibe Coding feedback drove a full course redesign, but none of that feedback signal reached the AI Agents or AI for PMs courses, even where the topics overlap.

**4. Duplication of effort.** When the Vibe Coding course was redesigned, the strategy document mapped ~55–60% content reuse from the old AI Prototyping course. That mapping was done manually, course-by-course. Every new certification or major revision requires this same manual archaeology. There is no inventory of what content exists, where it lives, or which courses use it.

**5. External signal is ad-hoc.** The AI Product Strategy course draws on Lenny's newsletter and podcast, Gokul Rajaram's 8 Moats framework, Hamilton Helmer's 7 Powers, and other sources. These are curated by individual course authors based on personal reading. LinkedIn posts with high traction about new frameworks, Substack thought pieces, Reddit discussions — none of these are systematically captured, evaluated, or routed to the courses that would benefit.

### The Root Cause

The root cause is the same one diagnosed in the Vibe Coding redesign: **the unit of content management is the course, when it should be the concept.** Just as the old AI Prototyping course "tried to teach a tool" when it should have been "teaching a process," our content operations try to maintain courses when they should be maintaining knowledge.

---

## The Strategy: Six Questions That Build One System

We teach senior PMs that AI product strategy requires answering six sequential questions. Each answer depends on the last. The same discipline applies here.

```
THE BET → THE MOAT → THE MARGIN → THE CONTRACT → THE GUARDRAILS → THE PITCH
  What       Why it      What         How we       What breaks     How this
  to build   compounds   it unlocks   trust it     when it scales  gets funded
```

---

### The Bet — What should we build, and how do we know fast?

> *"You can't predict which AI feature wins. Stop pretending you can."*
> — AI Product Strategy, M1 provocation

#### The Bet Statement

Build a **course-agnostic content library** — a structured knowledge layer where every teachable concept, framework, case study, external insight, and evidence point is stored as an independent, reusable **content atom**. Courses consume atoms. Feedback enriches atoms. External signal creates new atoms. The library is the product; courses are the distribution channels.

#### What a Content Atom Is

An atom is the smallest unit of teachable knowledge that can exist independently of any specific course. Four types:

| Type | Definition | Example |
|------|-----------|---------|
| **Concept** | A named idea with a canonical definition, context for when it applies, and version history | "Confidence UX" — three tiers (>90%, 50–90%, <50%), making probabilistic output legible to users |
| **Framework** | A reusable mental model with structure, application guidance, and adaptation notes | "5 AI Value Archetypes" — Automator, Copilot, Oracle, Creator, Orchestrator — each with margin profile, governance burden, example |
| **Evidence** | A case study, data point, stat, or real-world example with source attribution and recency metadata | "Klarna Automator overcorrection" — 3-act case study (Bet → Crack → Correction), source: public reporting, last verified March 2026 |
| **Signal** | A raw or lightly processed external input — podcast transcript excerpt, LinkedIn post, research finding — with extracted insight | "Gokul Rajaram: brand is not a moat anymore" — source: 20VC podcast March 2026, extracted insight: switching costs approaching zero due to agent-driven data migration |

Each atom carries metadata:

- **Unique ID** for stable cross-referencing
- **Source** with URL/citation
- **Date created** and **date last verified**
- **Confidence level**: Validated (multiple sources + taught in at least one cohort), Emerging (single credible source, not yet tested in class), Speculative (signal only, needs curation)
- **Courses that reference it** (automatically tracked)
- **Tags** for concept domain, audience level, and topic area

#### Why We Know This Is the Right Bet

Three signals validate this direction before we build anything:

1. **The Vibe Coding redesign already proved reuse works.** The strategy document mapped 55–60% content reuse from the old AI Prototyping course, module by module, content piece by content piece. But it was a one-time manual exercise. A library makes this the default operating model.

2. **Framework overlap across courses is already visible.** Agent Spectrum, AWSpec, eval methodology, RAG patterns, autonomy levels — these concepts appear in at least 2–3 courses each. The overlap isn't a bug; it validates that certain knowledge is foundational across the PM curriculum. It just needs a canonical home.

3. **External signal curation already happens — in one place.** The `lenny-insights.md` file in the AI Product Strategy repo demonstrates the value: Lenny sources mapped to specific modules, with actionable integration notes. The effort is proven; the scope is too narrow.

#### What Our Probabilistic Confidence Level Is

Using the M1 framework: **Medium-High confidence.** The concept is validated by internal evidence (reuse mapping, framework overlap, existing curation patterns) and external analogy (knowledge management systems in content-heavy organizations). The primary uncertainty is execution — specifically, whether course authors will adopt library-first workflows over their current independent approaches. This is an adoption risk, not a desirability risk.

---

### The Moat — Why won't this get copied in 6 months?

> *"Your data is not your moat. Your workflow is."*
> — AI Product Strategy, M2 provocation

A shared content library is a table-stakes idea. Any education company could decide to centralize their curriculum. The moat is not the structure — it is the **compounding loops** that make the library more valuable with every interaction.

#### Three Compounding Loops

**Loop 1: Cohort Feedback → Atom Refinement**

Every cohort that takes any of the nine certifications generates signal: student survey responses, in-class questions that reveal confusion or gaps, instructor adaptations that improve a concept's clarity. Today, this signal stays in meeting notes and Google Doc comments within a single course. In the library model, every feedback signal is routed to the specific atoms it touches. When three Vibe Coding cohorts say "the transition point concept needs more examples," the atom for "Transition Point (Vibe to Structure)" gets enriched — and every other course that references transition-point thinking benefits automatically.

The feedback loop that drove the Vibe Coding redesign — three cohorts of feedback surfacing five core problems — would, in this model, have enriched atoms used by multiple courses, not just triggered a single-course rewrite.

**Loop 2: External Signal → New Atoms**

The industry moves weekly. Lenny publishes a newsletter on AI pricing that reshapes how we should teach M3 of AI Product Strategy. Gokul Rajaram defines 8 Moats on a podcast and it immediately enriches M2. A LinkedIn post goes viral about a new PM framework. A Reddit thread surfaces a real-world failure mode that would make a perfect case study.

Today, this curation is one person's reading list, benefiting one course. In the library model, external signal is systematically ingested, processed into atoms (with source, date, confidence level), and routed to the courses where it adds value. The ingestion pipeline turns individual research into institutional knowledge.

**Loop 3: Cross-Course Citation → Canonical Authority**

When an atom is referenced by 5 out of 9 courses, it becomes foundationally important. When an atom is referenced by 1 course, it may be niche or speculative. The citation count across courses is itself a signal of importance. This creates a natural priority ranking for maintenance: the most cross-referenced atoms get the most attention, the freshest verification, and the deepest treatment.

No competitor — Reforge, Maven, Harvard, Coursera — operates this way. They maintain courses as independent products. Our structural advantage is the compounding layer between courses.

#### The Kill Switch (Vendor Dependency)

Applying our own M2 framework: what are the dependencies, and can we survive if any fail?

The library is markdown-based, stored in Git, with no proprietary tooling dependency. Atoms are plain text with structured metadata. Any migration — from GitHub to another platform, from markdown to a CMS, from Git to a database — is straightforward because the format is open. This is deliberate: the AI Product Strategy course teaches "abstraction layers and unified APIs for swapping vendors in under 48 hours." The content library follows the same principle.

---

### The Margin — What efficiency does this unlock?

> *"AI will compress your margins before it expands them."*
> — AI Product Strategy, M3 provocation

For a content business, the equivalent of inference costs is **content creation and maintenance cost per certification.** The library changes the cost curve.

#### Current Cost Model (Per-Course Silo)

| Cost Driver | Current Approach |
|-------------|-----------------|
| New course creation | Start from scratch or manually audit existing courses for reusable content (~55–60% reuse found in Vibe Coding, but discovery took significant manual effort) |
| Content updates | Each course author independently monitors their domain, updates their own materials, unaware of updates made in sibling courses |
| External research | Individual course authors curate their own sources (one `lenny-insights.md`, one `gokul-rajaram-8-moats-summary.md`, each benefiting only one course) |
| Feedback processing | Student feedback is captured in course-specific meeting notes, acted on within that course only |
| Quality assurance | No cross-course consistency checks — the same concept can be defined differently in different certifications with no detection mechanism |

#### Library Cost Model (Shared Atoms)

| Cost Driver | Library Approach | Efficiency Gain |
|-------------|-----------------|-----------------|
| New course creation | Compose from existing atoms; only create atoms for genuinely new concepts | Estimated 40–60% reduction in content creation time for new certifications |
| Content updates | Update an atom once, propagation is automatic to all referencing courses | Linear scaling eliminated — one update, N courses benefit |
| External research | Centralized ingestion pipeline; one researcher's work benefits all 9 courses | 9x leverage on external research investment |
| Feedback processing | Feedback routes to atoms, not courses; cross-course pattern detection becomes possible | Systemic improvements replace one-off fixes |
| Quality assurance | Canonical definitions prevent drift; automated alerts when an atom hasn't been verified within its SLA window | Consistency is structural, not aspirational |

#### The Value Capture Comparison

Adapting the M3 framework of "old SaaS revenue vs. AI usage revenue" to content operations:

- **Old model:** Content value is locked inside individual courses. Each certification captures 100% of the value of its own content and 0% of the value of content that exists in sibling courses. Enterprise customers see nine separate products.
- **New model:** Content value compounds across the portfolio. Each atom serves multiple courses. Enterprise customers see a unified, continuously updated knowledge platform. The content depth across nine certifications becomes a portfolio advantage, not nine parallel costs.

#### Enterprise Pricing Implication

Enterprise customers increasingly ask: "How current is your curriculum?" and "Can you customize content for our organization's needs?" A living library with freshness metadata and modular atoms answers both questions structurally. This supports premium pricing for enterprise — not because the delivery changes, but because the content substrate is demonstrably richer and more current than any competitor's static curriculum.

---

### The Contract — How do we trust the content is accurate?

> *"95% accuracy with no audit trail loses to 85% accuracy with one."*
> — AI Product Strategy, M4 provocation

Trust in a content library is trust that every atom is accurate, current, and well-sourced. The AI Product Strategy course teaches that trust is not a function of quality — it is a function of **perceived control and transparency.** The same principle applies here.

#### The Reliability Contract for Content

Every atom in the library makes an implicit promise: **this information is accurate as of its last verification date.** Making that promise explicit and measurable is the contract.

**Freshness SLAs by Atom Type:**

| Atom Type | Verification SLA | Rationale |
|-----------|-----------------|-----------|
| Concept (canonical definition) | Every 180 days | Core definitions change slowly; annual review is too infrequent given AI industry pace |
| Framework | Every 180 days | Frameworks are durable but need periodic validation against new industry developments |
| Evidence (case study, stat) | Every 90 days | Stats go stale fast; case studies may be superseded by newer, better examples |
| Signal (external input) | Every 60 days | Raw signal ages fastest; a LinkedIn post from 4 months ago may already be conventional wisdom or debunked |

**Confidence Scoring (Adapted from M4's Three-Tier Confidence UX):**

The AI Product Strategy course teaches confidence UX in three tiers: >90% confidence (automate), 50–90% (assist with disclosure), <50% (flag for review). The content library adapts this:

| Confidence Level | Criteria | Course Author Guidance |
|-----------------|----------|----------------------|
| **Validated** | Multiple credible sources; taught in at least one cohort; positive student signal | Use directly in course materials. Cite as established. |
| **Emerging** | Single credible source or recent publication; not yet tested in classroom delivery | Use with context ("recent research suggests..."). Flag for validation in next cohort. |
| **Speculative** | Signal only — trending discussion, single data point, unverified claim | Do not use in course materials without escalation. Include in internal research queue. |

**Source Attribution (The Audit Trail):**

Every claim, every stat, every framework in the library traces back to its source. The `lenny-insights.md` file in the AI Product Strategy repo is an example of good attribution practice:

> "Evals are 'the defining skill for AI PMs in 2025 and beyond'" — source: Lenny's Newsletter, "Beyond vibe checks: A PM's complete guide to evals," April 2025, by Aman Khan (Arize AI, ex-Spotify/Cruise/Apple).

This level of attribution — author, publication, date, context — becomes the standard for every evidence and signal atom. When a student or enterprise customer asks "where does this come from?", the answer is immediate and verifiable.

**The Golden Dataset Analogy:**

The AI Product Strategy course teaches golden datasets as product infrastructure — "the ground truth against which AI outputs are evaluated." The content library has its own golden dataset: the set of canonical concept definitions and verified frameworks that represent Product School's institutional knowledge. Everything else (evidence, signal) is measured against whether it strengthens, challenges, or invalidates the canonical layer.

---

### The Guardrails — What breaks when this scales?

> *"Your governance framework is a sales asset, not a compliance burden."*
> — AI Product Strategy, M5 provocation

#### Content Governance Model

**Who can create atoms?** Anyone — course authors, instructors, the content team, the CPTO. Low barrier to entry ensures the library captures signal from everywhere.

**Who can promote atoms to Validated?** Content leads with domain expertise. Promotion requires: source verification, at least one peer review, and a decision on which courses should reference the atom.

**Who can deprecate atoms?** The CPTO and course leads jointly. Deprecation triggers: the atom is factually outdated, superseded by a better atom, or no longer referenced by any course. Deprecated atoms are archived, not deleted — they retain their history and rationale for deprecation.

**Cross-Course Consistency Protocol:**

When a concept appears in multiple courses (e.g., Agent Spectrum in AI Agents and AI for PMs), the library holds the canonical definition. Course-specific adaptations are allowed — the AI Agents course may go deeper into multi-agent patterns than the AI for PMs course — but the core definition must be consistent. If a course author wants to change a canonical definition, the change is proposed in the library, reviewed against all referencing courses, and either accepted globally or rejected.

This is the "compounding system" from M5 applied to content: quality improves with usage because every course that references an atom also stress-tests it. Inconsistencies surface as instructor or student confusion and get routed back to the atom for resolution.

#### External Signal Quality Gates

Not everything from the internet enters the library. The ingestion pipeline has gates:

```
Raw Signal (podcast, post, thread)
    ↓
Extraction: What is the core insight? Is it novel or already covered?
    ↓
Source Evaluation: Is the source credible? Is there corroboration?
    ↓
Relevance Check: Which courses would benefit? Is there a specific module fit?
    ↓
Atom Creation (at Speculative or Emerging confidence)
    ↓
Curation Review: Content lead promotes to Validated or flags for further research
```

#### Feedback Loop Architecture

The AI Product Strategy course teaches that "the system learns from every interaction, not just the ones in your silo." The content library operationalizes this:

| Signal Source | What It Generates | How It Routes |
|--------------|------------------|---------------|
| **Student surveys** | Satisfaction scores per topic, free-text feedback | NLP extraction of topic mentions → mapped to atoms → flagged for review if negative signal |
| **Customer Success** | Enterprise customer requests, pain points, feature asks | CS team tags atoms relevant to each conversation → demand signal informs atom priority |
| **Instructor observations** | In-class adaptations, questions that reveal gaps, concepts that land well | Post-cohort debrief creates atom annotations: "works well when explained as X" or "students consistently confused by Y" |
| **Enterprise demand** | What enterprise customers want in custom programs, what topics they prioritize | Demand patterns inform atom investment priority and new atom creation |
| **External sources** | Podcast transcripts, newsletter posts, LinkedIn/Substack, Reddit threads | Ingestion pipeline (see above) creates new atoms or enriches existing ones |

#### The Compounding System Design

The M5 concept of "recursive learning" applies directly: the library doesn't just store content — it gets smarter. Each feedback loop feeds back into atom quality. Each new cohort generates signal that refines existing atoms and surfaces gaps for new ones. Each external source captured enriches the library's coverage. The system compounds.

The specific compounding mechanisms:

1. **Usage frequency** reveals importance — atoms referenced by many courses get more maintenance attention
2. **Negative feedback** reveals staleness — student dissatisfaction with a topic triggers atom review
3. **Positive feedback** reveals what works — "aha moment" annotations help other instructors teach the same concept effectively
4. **External signal** reveals market movement — new frameworks, new case studies, new evidence keep the library ahead of the industry
5. **Enterprise demand** reveals market needs — what enterprise customers ask for shapes which atoms get invested in next

---

### The Pitch — How this gets funded, shipped, and adopted

> *"The roadmap is an output, not your job description."*
> — AI Product Strategy, M6 provocation

#### The Narrative for Each Stakeholder

**To the CEO and Board:**

"Product School teaches nine certifications in a market where the underlying knowledge changes weekly. Our competitors — Reforge, Maven, Coursera — maintain each course independently. When a framework evolves or a new industry standard emerges, they update one course at a time. We are building a system where a single update propagates across all nine certifications instantly. Every cohort we teach makes the library richer. Every external signal we capture makes our content more current. This is not a content management project — it is a structural moat. Within 12 months, our content freshness and cross-course coherence will be a measurable competitive advantage that no competitor can replicate without rebuilding their entire content infrastructure."

**To Instructors:**

"You will never teach stale content again. Before each cohort, you will see exactly which atoms have been updated since your last delivery. New case studies, refreshed stats, refined frameworks — all available without you needing to personally monitor the entire AI landscape. Your in-class observations and adaptations feed back into the library, so your teaching experience directly improves the next instructor's materials. You are not consumers of content — you are contributors to a living system."

**To Enterprise Customers:**

"Our curriculum is not a frozen document. It is a living knowledge system where every concept, framework, and case study carries a verification date, source attribution, and confidence level. We can show you exactly when each element of your program was last validated. We can customize your program by composing from our library of verified content atoms, ensuring your team gets the most current, most relevant material — not a generic off-the-shelf course."

**To the Content Team:**

"You build atoms, not courses. Your work reaches all nine certifications. When you research a topic deeply, that research compounds across the entire portfolio. When you verify a stat, that verification benefits every course that uses it. Your impact is multiplicative, not additive."

---

## Implementation: The Confidence Line

The Vibe Coding certification teaches that every product initiative starts in ambiguity and needs to move toward confidence. The implementation of the content library follows the same arc.

```
Phase 1-2: High Ambiguity      →  Phase 3-4: Gaining Clarity     →  Phase 5-6: Production Confidence
(Foundation + Seeding)             (Wiring + Curation)                (Compounding + Ecosystem)
```

### Phase 1: Foundation (Weeks 1–3)

> *Confidence Line position: Far left. Maximum ambiguity. Build the structure, learn by doing.*

**What we build:**
- Repository structure for the content library with atom schema and metadata standards
- Seed the library with atoms extracted from the four existing course repos (AI Product Strategy, Vibe Coding, AI Agents, AI for PMs)
- Create the initial content inventory: what exists, where, what overlaps

**What we learn:**
- How many unique atoms exist across the four courses vs. how many are duplicates or near-duplicates
- Which concepts are foundational (referenced by 3+ courses) and which are course-specific
- What the natural taxonomy looks like when content is decomposed into atoms

**Success signal:** We can answer: "How many canonical concepts does Product School teach, and which courses use each one?"

### Phase 2: Ingestion Pipelines (Weeks 3–6)

> *Confidence Line position: Still left, but with methodology. We can capture signal systematically.*

**What we build:**
- Ingestion workflow for external sources: Lenny's podcast/newsletter, Product School event transcripts, LinkedIn trending posts, Substack, Reddit
- Feedback routing: student survey responses mapped to atoms, CS conversation tagging, instructor debrief templates
- Quality gates for new atoms entering the library

**What we learn:**
- Which external sources generate the most high-value atoms per unit of effort
- How to balance ingestion volume against curation quality
- What the right cadence is for processing external signal (daily? weekly?)

**Success signal:** The library receives at least 10 new atoms per week from external sources, with clear source attribution and confidence levels assigned.

### Phase 3: Course Wiring (Weeks 6–10)

> *Confidence Line position: Gaining clarity. We know the library works. Now we connect courses to it.*

**What we build:**
- Refactor AI Product Strategy and Vibe Coding (the two most architecturally mature courses) to reference library atoms instead of inline content
- Create canonical definitions for the top 20 most cross-referenced concepts
- Build the first cross-course consistency report: where do current courses diverge from canonical definitions?

**What we learn:**
- How much course-specific adaptation is appropriate vs. how much should be standardized
- Whether instructors find the library workflow natural or burdensome
- What the right balance is between atom-level modularity and course-level narrative coherence

**Success signal:** Two courses are wired to the library. Instructors for those courses can see, in one view, which atoms changed since their last cohort delivery.

### Phase 4: Curation Workflow (Weeks 10–14)

> *Confidence Line position: The inflection point. From exploration to committed process.*

**What we build:**
- Formal curation roles: who reviews new atoms, who promotes from Emerging to Validated, who depreciates stale atoms
- Freshness SLA monitoring: automated alerts when atoms exceed their verification window
- Enterprise content dashboard: a view for enterprise customers showing content freshness and last-verified dates

**What we learn:**
- What the sustainable curation throughput is (atoms reviewed per week per content lead)
- Whether freshness SLAs are realistic or need adjustment
- How enterprise customers respond to content transparency

**Success signal:** 90% of Validated atoms are within their freshness SLA. Enterprise sales team can demo the content freshness dashboard in pitches.

### Phase 5: Compounding Systems (Weeks 14–20)

> *Confidence Line position: Right side. High confidence, hardening for scale.*

**What we build:**
- Automated cross-course impact analysis: when an atom is updated, flag all courses that reference it and surface the change to course authors
- Feedback loop analytics: which atoms generate the most student confusion (negative signal), which generate the most "aha moments" (positive signal)
- AI-assisted ingestion: automated extraction of insights from podcast transcripts, newsletter posts, and other text sources, with human review before promotion

**What we learn:**
- Which compounding loops generate the most value: cohort feedback, external signal, or cross-course citation
- Whether AI-assisted ingestion maintains quality standards
- What the compound growth rate of the library is — how many high-quality atoms per month

**Success signal:** The library is growing at 20+ validated atoms per month. Cross-course consistency is measurable and improving. Student satisfaction in piloted courses trends upward correlated with content freshness.

### Phase 6: Ecosystem (Weeks 20–30)

> *Confidence Line position: Far right. Production confidence. The system is self-sustaining.*

**What we build:**
- All nine certifications wired to the library
- Instructor contribution workflow: post-cohort, instructors annotate atoms with teaching observations
- Enterprise co-creation: enterprise customers can request custom atom compositions and provide domain-specific content for inclusion
- Community-sourced examples: a pathway for the broader PM community to suggest case studies, evidence, and signal

**What we learn:**
- Whether the library model fundamentally changes course creation speed for new certifications
- How enterprise customers value content transparency and customization
- Whether community contribution adds signal or noise

**Success signal:** New certification creation time is reduced by 40%+. Enterprise customers cite content freshness as a purchasing factor. The library is the default starting point for any content decision.

---

## Metrics: How We Know It's Working

### Leading Indicators (Operational Dashboard)

| Metric | Target | Signal If Missed |
|--------|--------|-----------------|
| Atoms within freshness SLA | 90%+ of Validated atoms | Curation throughput too low; add reviewers or adjust SLAs |
| New atoms per week (from all sources) | 15+ | Ingestion pipeline is clogged or under-resourced |
| Cross-course atom usage | Average 2.5+ courses per atom | Library is too course-specific; review atom granularity |
| Feedback-to-atom routing rate | 80%+ of actionable feedback mapped to atoms | Routing workflow is unclear; simplify the tagging process |

### Lagging Indicators (Quarterly Review)

| Metric | Target | Why It Matters |
|--------|--------|---------------|
| Student NPS trend (courses using library) | Upward trend vs. courses not yet wired | Validates that library-sourced content is better than siloed content |
| Time to create a new certification | 40% reduction from baseline | The fundamental efficiency promise of the library |
| Cross-course consistency score | <5% definitional variance for canonical concepts | The coherence promise |
| Enterprise content freshness inquiries | Tracked | Whether freshness is becoming a market differentiator |

### Impact Indicators (Annual)

| Metric | Target | How to Measure |
|--------|--------|---------------|
| Enterprise deal win rate citing content quality | Tracked qualitatively | Sales team debriefs |
| Instructor preparation time reduction | 30%+ | Instructor surveys |
| Content duplication ratio | Decreasing quarter-over-quarter | Automated library analysis |
| Repeat enrollment across certifications | Upward trend | Internal enrollment data |

---

## What Exists Today: The Starting Inventory

### Discovered Course Repositories

| Course | Location | Structure | Content Maturity |
|--------|----------|-----------|-----------------|
| AI Product Strategy | `/Product School - AI Product Strategy/` | 6 module slide pairs (HTML + speaker notes), 11 interactive HTML tools, Living Strategy Builder, Pitch deck, meeting notes, insights folder | High — full course architecture, storyline, status tracker, Lenny mapping, design principles |
| Vibe Coding | `/AI Prototyping : Vibe Coding/` | 6 module slide/lab pairs, instructor guide, final project spec, 19 insight files, feedback synthesis | High — full strategy document with Confidence Line, competitive analysis, content reuse map, success metrics |
| AI Agents | `/AI Agents speaker notes/` | Single markdown file with all 6 modules, icebreaker bank, legacy text export | Medium — complete content but minimal supporting strategy or feedback infrastructure |
| AI for PMs | `/AI for Product Managers Speaker Notes/` | 6 separate module files under `Insights/` | Medium — complete content, slide-ordered, with threaded scenario (Juno/RocketShip) |

### Key Frameworks Identified Across Courses

| Framework | Courses Where It Appears | Canonical Candidate? |
|-----------|--------------------------|---------------------|
| Agent Spectrum (autonomy levels) | AI Agents, AI for PMs | Yes — needs canonical definition reconciled across both |
| AWSpec (Agent Workflow Spec) | AI Agents, AI for PMs | Yes — taught in both, similar but not identical |
| Eval methodology (3-layer stack) | AI Product Strategy (M4), AI for PMs (M6), likely AI Evals | Yes — high cross-course value |
| RAG architecture and PM ownership | AI Product Strategy (M4), AI for PMs (M3), AI Agents (M4) | Yes — pattern repeated with different depth |
| Confidence UX (probabilistic output design) | AI Product Strategy (M4), Vibe Coding (Confidence Line) | Yes — related but distinct applications |
| 5 AI Value Archetypes | AI Product Strategy (M1) | No — currently single-course, but high reuse potential |
| 8 Moats (Gokul/Helmer) | AI Product Strategy (M2) | No — currently single-course, but high reuse potential |
| Build-Show-Learn-Decide | Vibe Coding (M1) | No — course-specific pedagogy |
| Living Strategy concept | AI Product Strategy (throughline) | No — course-specific artifact |
| Kill Switch (vendor portability) | AI Product Strategy (M2) | Yes — applicable to AI Agents and AI for PMs |

### Key External Sources Already Curated

From `lenny-insights.md` in the AI Product Strategy repo:

| Source | Type | Modules Mapped |
|--------|------|---------------|
| "Counterintuitive advice for building AI products" — Lenny, Jul 2024 | Newsletter | M1 |
| "Beyond vibe checks: A PM's guide to evals" — Aman Khan, Apr 2025 | Newsletter | M4 |
| "Building eval systems that improve your AI product" — Husain & Shankar, Sep 2025 | Newsletter | M4 |
| "Pricing your AI product: Lessons from 400+ companies" — Madhavan Ramanujam, Jul 2025 | Podcast | M3 |
| "Business strategy with Hamilton Helmer (7 Powers)" — May 2024 | Podcast | M2 |
| "25 proven tactics to accelerate AI adoption" — Aug 2025 | Newsletter | M5 |
| "OpenAI's CPO on moats, evals, and startup playbooks" — Kevin Weil, Apr 2025 | Podcast | M1, M4, M6 |
| Gokul Rajaram — "The 8 Moats Companies Need" — 20VC, Mar 2026 | Podcast | M2, M3, M6 |

These represent the first atoms to migrate from course-specific notes into the shared library.

---

## Open Questions

| Question | Options | Owner | Status |
|----------|---------|-------|--------|
| Which five courses beyond the four discovered repos need to be inventoried? | PM, GTM, Experimentation, Leadership, AI Evals — need access to content repos or materials | CPTO | Open |
| What is the right tooling for the library? | Git-based markdown (current approach) vs. structured CMS vs. knowledge graph tool | CPTO + Engineering | Open — recommend starting with Git-based markdown for speed, evaluate tooling upgrade at Phase 4 |
| Who owns curation operationally? | Dedicated content ops role vs. distributed across course leads vs. hybrid | CPTO | Open — recommend hybrid: CPTO sets standards, course leads curate within their domain |
| How deep should AI-assisted ingestion go? | Manual extraction only vs. AI extraction with human review vs. fully automated with spot checks | CPTO + Content Team | Open — recommend AI extraction with human review starting in Phase 2 |
| Should enterprise customers see the library directly? | Full transparency vs. curated view vs. metadata only (freshness dates, not raw atoms) | CPTO + Enterprise Sales | Open — recommend metadata view initially, expand based on customer feedback |

---

## Non-Goals

These are deliberately excluded from this strategy:

1. **Building a CMS or LMS.** The library is a knowledge layer, not a delivery platform. Courses are still delivered through Product School's existing channels. The library feeds content into courses; it does not replace the course delivery infrastructure.

2. **Replacing instructor judgment.** Atoms provide the canonical knowledge; instructors adapt delivery to their cohort's level, energy, and needs. The library makes better content available — it does not script delivery.

3. **Automating course creation end-to-end.** The library enables faster, higher-quality course creation. It does not replace the human editorial judgment required to compose atoms into a coherent learning arc. The AI Product Strategy course's "six sequential questions" and the Vibe Coding course's "Confidence Line" are narrative structures that require human design.

4. **Public-facing content platform.** The library is an internal operational asset. It may inform public-facing content (blog posts, marketing materials, enterprise proposals), but it is not itself a public product — at least not in the first implementation.

---

## Closing: Why This Is The Bet

The AI Product Strategy course opens with a provocation: "You can't predict which AI feature wins. Stop pretending you can." And then it teaches a process for making bets under irreducible uncertainty — probabilistic prioritization, not deterministic commitments.

This content library is that kind of bet. We cannot predict which external signal will reshape a module, which student feedback will surface a critical gap, or which enterprise customer will demand a topic we haven't covered. But we can build a system that captures, curates, and compounds all of that signal — systematically, across all nine certifications, continuously.

The Confidence Line maps our journey: we start in ambiguity (Phase 1–2), gain clarity as we wire courses and build curation workflows (Phase 3–4), and reach production confidence when the system compounds on its own (Phase 5–6).

The AI Product Strategy course tells participants: "They don't leave with a certificate. They leave with a weapon." Product School's weapon is a living content library that gets sharper with every cohort, every signal, every feedback loop.

We build the library. The library builds the courses. The courses build the library.

That is the compounding system.
