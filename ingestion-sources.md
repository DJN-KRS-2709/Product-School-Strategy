# Ingestion Sources — Signal Capture Strategy

**Purpose:** Document every source of information that should feed the living content library, how to capture signal from each source, expected volume and value, and quality gates for entry.

---

## Source Categories

```
Internal Sources                    External Sources
(what we learn from our own ops)    (what the industry is saying)
                 ↓                                ↓
         ┌──────────────┐               ┌─────────────────┐
         │ Student       │               │ Podcasts &       │
         │ Surveys       │               │ Newsletters      │
         ├──────────────┤               ├─────────────────┤
         │ Customer      │               │ LinkedIn &       │
         │ Success       │               │ Social           │
         ├──────────────┤               ├─────────────────┤
         │ Instructor    │               │ Substack &       │
         │ Observations  │               │ Blogs            │
         ├──────────────┤               ├─────────────────┤
         │ Enterprise    │               │ Reddit &         │
         │ Customer      │               │ Communities      │
         │ Demand        │               ├─────────────────┤
         ├──────────────┤               │ Product School   │
         │ Cohort        │               │ Events &         │
         │ Transcripts   │               │ Conferences      │
         └──────────────┘               └─────────────────┘
                 ↓                                ↓
         ┌────────────────────────────────────────┐
         │          Content Library                │
         │    (atoms with confidence levels)       │
         └────────────────────────────────────────┘
```

---

## Internal Sources

### 1. Student Surveys

**What it captures:** Post-cohort satisfaction data, per-module ratings, free-text feedback on what worked, what confused, and what felt outdated.

**Current state:** Surveys exist but are processed within individual courses. The Vibe Coding redesign was driven by "three cohorts of feedback" surfacing five core problems. This signal stayed within Vibe Coding's repo and influenced only that course's redesign.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Collect | Post-cohort surveys across all 9 certifications | After each cohort |
| Extract | Identify specific topics, frameworks, and modules mentioned in feedback | Within 1 week of cohort end |
| Map | Tag each feedback item to relevant content atoms in the library | Within 1 week |
| Route | Negative signal → atom flagged for review; Positive signal → atom annotated with "what worked" | Ongoing |
| Aggregate | Cross-cohort trend analysis: which atoms are consistently praised or criticized across courses | Monthly |

**Expected volume:** 9 certifications × ~4–6 cohorts/year each = ~40–54 survey batches per year. Each batch yields 5–15 actionable feedback items.

**Value signal:** High. Student feedback is the most direct signal about content quality and relevance. The Vibe Coding strategy document (`Vibe Coding Certification - Course Strategy and Outline.md`) demonstrated that systematically processing student feedback drives the highest-impact content improvements.

---

### 2. Customer Success Feedback

**What it captures:** Patterns from CS conversations with students and enterprise buyers: recurring questions, confusion points, requests for topics not covered, complaints about outdated material.

**Current state:** CS feedback is handled operationally but not systematically routed to content teams. Enterprise CS teams know what customers want but lack a structured way to inform curriculum.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Tag | CS team tags each conversation with relevant topic areas and certification(s) | Per interaction |
| Summarize | Weekly digest of recurring themes and new topic requests | Weekly |
| Map | Map recurring themes to existing atoms (enrichment) or flag as potential new atoms | Weekly |
| Escalate | Topics requested by 3+ enterprise customers → fast-track for atom creation | As they occur |
| Close loop | When an atom is updated based on CS feedback, notify the CS team so they can confirm to the customer | Within 2 weeks |

**Expected volume:** Moderate. CS interactions are lower volume than student surveys but higher signal-to-noise ratio for enterprise-relevant content.

**Value signal:** High for enterprise content strategy. CS is the closest proxy for "what the market wants next."

---

### 3. Instructor Observations

**What it captures:** In-class adaptations, questions that reveal student confusion, concepts that consistently land well, delivery techniques that improve comprehension.

**Current state:** Some instructor feedback captured in meeting notes and working sessions. The AI Product Strategy course has meeting notes (`meeting-notes/2025-03-10-working-session.md`, `2025-03-13-working-session.md`) that record decisions and feedback. The Vibe Coding course has Carlos working session notes, Dana kickoff transcript, and per-module Carlos briefs. But these are course-specific and not structured for cross-course learning.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Debrief | Post-cohort structured debrief with each instructor: what worked, what didn't, what they adapted | After each cohort |
| Annotate | Instructor adds teaching notes to specific atoms: "works well when explained as X" or "students consistently confused by Y" | After each cohort |
| Share | Cross-instructor digest: what adaptations are other instructors making? | Monthly |
| Promote | Instructor adaptations that consistently improve comprehension → update the canonical atom | Quarterly |

**Expected volume:** Low volume but extremely high value. Instructor observations are the most practical signal about teaching effectiveness.

**Value signal:** Critical for the "Teaching Notes" section of every atom.

---

### 4. Enterprise Customer Demand

**What it captures:** What enterprise customers request in custom programs, which topics they prioritize, what gaps they identify between their org's needs and the standard curriculum.

**Current state:** Enterprise demand is captured in sales conversations and custom program scoping but not systematically fed back to content. Enterprise customers represent the highest-value signal about market direction because they are committing budget to specific topics.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Log | Enterprise sales and CS log topic requests with customer context (industry, company size, role level) | Per engagement |
| Aggregate | Monthly demand report: which topics are most requested, which are under-served | Monthly |
| Prioritize | Topics requested by 3+ enterprise customers → atom creation or enrichment priority | As threshold met |
| Validate | New atoms created from enterprise demand are tagged with demand source for ROI tracking | Per atom |

**Expected volume:** Lower volume but highest commercial signal. Each enterprise request carries budget authority.

**Value signal:** Directly tied to revenue. Enterprise demand should be a weighted input in atom priority.

---

### 5. Cohort Transcripts and Session Recordings

**What it captures:** Verbatim class discussions, student questions, instructor explanations, lab interactions — the raw material of what happens in the classroom.

**Current state:** Some transcripts exist embedded in meeting notes (e.g., the Dana-Dejan kickoff meeting in the Vibe Coding repo includes a raw transcript section). Class session recordings may exist but are not systematically processed for content insights.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Record | All live sessions are recorded (already standard for most certifications) | Every session |
| Transcribe | AI-assisted transcription of each session | Within 24 hours |
| Extract | AI-assisted extraction of: new questions raised, concepts that needed extra explanation, examples that resonated, student-contributed insights | Within 1 week |
| Map | Map extracted insights to atoms: enrichment for existing atoms, signals for potential new atoms | Within 1 week |

**Expected volume:** High volume (6 sessions per cohort × 40+ cohorts per year). AI-assisted processing is essential — manual review at this scale is not feasible.

**Value signal:** Medium-high. Transcripts are noisy but contain gems: student questions reveal gaps, instructor adaptations reveal improvements, class discussions reveal real-world applications.

---

### 6. Course Build and Content Ops Working Sessions

**What it captures:** Decisions made while courses are created, audited, converted into repos, prepared for LMS access, or repackaged for enterprise. These sessions surface source-of-truth rules, module dependencies, course-specific references that need cleanup, and the operational constraints that do not show up in slide decks.

**Current state:** These decisions are often made in meetings and Slack threads, then applied manually by the content owner. The signal is high value but easy to lose because it is about how the content should be maintained, not just what the course teaches.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Record | Capture working sessions where content structure, course conversion, LMS needs, or enterprise packaging decisions are made | Per session |
| Extract | Identify source-of-truth decisions, module dependency rules, generated output needs, and repackaging constraints | Within 48 hours |
| Map | Route decisions to module contracts, atom metadata, or operating docs | Within 1 week |
| Close loop | Confirm with the content owner that the extracted rules match how they actually build and maintain courses | Within 1 week |

**Expected volume:** Low to moderate. Each session can produce multiple durable operating rules.

**Value signal:** Very high for implementation. These sessions define the "course API" that lets one source generate slides, speaker notes, student notes, LMS views, and enterprise packages.

---

## External Sources

### 7. Lenny's Newsletter and Podcast

**What it captures:** PM-focused analysis on AI products, pricing, evals, adoption, strategy. Already proven as a high-value source — `lenny-insights.md` in the AI Product Strategy repo maps 10+ sources to specific modules with actionable integration notes.

**Current state:** Manually curated by the AI Product Strategy course author. Insights benefit one course.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Monitor | Subscribe and track new posts and episodes | Ongoing (2–4 per month) |
| Screen | Evaluate each publication for curriculum relevance: does it relate to any of the 120+ frameworks in the inventory? | Within 3 days of publication |
| Extract | For relevant items: extract key insights, data points, quotes, and frameworks with full citation | Within 1 week |
| Create atom | Create signal atom with extracted takeaway and potential course applications | Within 1 week |
| Route | Tag with relevant courses and modules | Per atom |

**Expected volume:** 2–4 high-value items per month. Already demonstrated as the highest-signal external source.

**Value signal:** Very high. Lenny's audience is our audience. His sources are often the same practitioners our students aspire to learn from.

**Pre-existing curation to migrate:**

The following sources from `lenny-insights.md` should be the first external signal atoms in the library:

- "Counterintuitive advice for building AI products" — 20+ builders interviewed
- "Beyond vibe checks: PM's guide to evals" — Aman Khan
- "Building eval systems that improve your AI product" — Husain & Shankar
- "Pricing your AI product: Lessons from 400+ companies" — Madhavan Ramanujam
- "Business strategy with Hamilton Helmer (7 Powers)"
- "25 proven tactics to accelerate AI adoption"
- "OpenAI's CPO on moats, evals, and startup playbooks" — Kevin Weil
- Gamma: "$100M ARR from the dumbest idea" — Grant Lee
- "What AI means for your product strategy" — Paul Adams, Intercom

---

### 8. Product School Events and Conferences

**What it captures:** Keynotes, panels, workshops, and speaker content from Product School's own events. Product School hosts significant events with industry leaders — this content is proprietary and should be a competitive advantage.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Record | All Product School events are recorded | Per event |
| Transcribe | AI-assisted transcription of keynotes and panels | Within 48 hours |
| Extract | Key frameworks, data points, provocative claims, and expert opinions | Within 1 week |
| Create atoms | New signal atoms for novel insights; enrichment for existing atoms where speakers validate or challenge current content | Within 1 week |
| Flag | Speaker insights that contradict current canonical atoms → escalate for review | Immediately |

**Expected volume:** Depends on event calendar. Each event typically yields 3–8 actionable content signals.

**Value signal:** High and proprietary. This is content no competitor can access.

---

### 9. LinkedIn (High-Traction Posts and Thought Leadership)

**What it captures:** Emerging frameworks, contrarian takes, new tools, real-world case studies shared by PM practitioners and AI leaders. LinkedIn is where new PM thinking surfaces first — often before it appears in newsletters or podcasts.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Monitor | Track high-engagement posts (500+ reactions) from a curated list of PM and AI thought leaders | Daily scan (5 minutes) |
| Screen | Does the post introduce a new framework, challenge an existing one, or provide a novel case study? | Per post |
| Extract | Core insight, author + credentials, engagement metrics (as social proof), date | For relevant posts |
| Create atom | Signal atom with low confidence (speculative); note engagement as validation signal | Within 3 days |
| Promote | If corroborated by another source or validated by internal expertise → promote to emerging | When evidence found |

**Curated thought leader list (starter):**

Category: PM and AI product leaders with consistently high-quality, curriculum-relevant posts. Build this list over time based on signal quality, not follower count.

**Expected volume:** 3–5 relevant posts per week from the PM/AI ecosystem. Most will stay at speculative level; 1–2 per month may warrant emerging status.

**Value signal:** Medium. High noise, but the signal — when found — is extremely current. LinkedIn surfaces trends 2–4 weeks before they appear in newsletters.

---

### 10. Substack and Independent Blogs

**What it captures:** Long-form analysis from independent PM and AI thinkers. Substacks often go deeper than LinkedIn posts and provide more rigorous analysis. Key publications include Lenny's (covered separately), but also Stratechery (Ben Thompson), The Pragmatic Engineer (Gergely Orosz), and emerging AI-focused PM publications.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Subscribe | Maintain subscriptions to 10–15 high-signal Substack publications | Ongoing |
| Screen | Weekly scan for posts relevant to any of the nine certification domains | Weekly |
| Extract | Key insights, frameworks, data points with full attribution | For relevant posts |
| Create atom | Signal or evidence atom depending on depth and sourcing | Within 1 week |

**Expected volume:** 2–3 relevant articles per week across all subscriptions.

**Value signal:** Medium-high. Substacks are higher quality than LinkedIn but lower frequency. Often provide the depth needed to promote a signal from speculative to emerging.

---

### 11. Reddit (r/ProductManagement, r/artificial, r/MachineLearning, etc.)

**What it captures:** Practitioner discussions, real-world challenges, tool comparisons, failure stories, and emerging practices. Reddit surfaces problems and solutions that polished publications don't cover — the messy reality of AI product work.

**Capture strategy:**

| Step | Action | Frequency |
|------|--------|-----------|
| Monitor | Track top posts (100+ upvotes) in relevant subreddits | Weekly scan |
| Screen | Does the discussion reveal a real-world pattern, challenge, or tool/technique our curriculum should address? | Per thread |
| Extract | Core pattern, representative quotes (anonymized), community consensus | For relevant threads |
| Create atom | Signal atom at speculative level; Reddit is unverified by definition | Within 1 week |
| Validate | Cross-reference with other sources before any promotion | Required before emerging |

**Expected volume:** 1–2 relevant threads per week.

**Value signal:** Low-medium individually, but collectively reveals practitioner pain points that formal sources miss. Particularly valuable for identifying what confuses PMs in the field — which directly informs teaching notes on atoms.

---

## Ingestion Pipeline — Quality Gates

Not every signal becomes an atom. The pipeline has four gates:

### Gate 1: Relevance

**Question:** Does this signal relate to any of the nine certifications' domains?

**Pass criteria:** The signal relates to product management, AI product development, product strategy, prototyping, evaluation, agents, go-to-market, experimentation, or product leadership.

**Fail:** General tech news, company stock performance, hiring trends (unless directly relevant to PM practice).

### Gate 2: Novelty

**Question:** Does this signal add something the library doesn't already cover?

**Pass criteria:** Introduces a new framework, contradicts an existing canonical atom, provides new evidence for an existing concept, or offers a significantly better example/case study.

**Fail:** Restates what the library already captures without adding new perspective or evidence.

### Gate 3: Source Credibility

**Question:** Is the source credible enough for the assigned confidence level?

| Confidence Level | Source Requirements |
|-----------------|-------------------|
| Speculative | Any public source; the signal itself is the value |
| Emerging | Named author with relevant credentials OR publication with editorial standards |
| Validated | 2+ independent credible sources; ideally includes a primary source (company blog, research paper, practitioner with firsthand experience) |

### Gate 4: Actionability

**Question:** Can this signal be used to improve, update, or extend curriculum content?

**Pass criteria:** The signal suggests a specific change: update a stat, add a case study, introduce a new framework, modify a teaching approach, or enrich a concept's explanation.

**Fail:** Interesting but abstract; no clear path to curriculum improvement.

---

## Processing Cadence

| Activity | Cadence | Owner |
|----------|---------|-------|
| LinkedIn daily scan | Daily (5 min) | Content team or automated alerts |
| Weekly external source review (Substack, Reddit, newsletters) | Weekly (30 min) | Content team |
| Student survey processing | Within 1 week of cohort end | Content lead for that certification |
| CS feedback digest | Weekly summary | CS team lead |
| Instructor debrief | After each cohort | Course lead |
| Enterprise demand aggregation | Monthly | Enterprise sales + content lead |
| Lenny/podcast processing | Within 1 week of publication | Content team |
| Event transcript processing | Within 1 week of event | Content team |
| Course build working-session processing | Within 1 week of session | CPTO + content owner |
| Cross-source trend analysis | Monthly | CPTO + content leads |
| Full library freshness audit | Quarterly | CPTO |

---

## Prioritization Framework

When multiple sources generate signals simultaneously, prioritize based on:

1. **Enterprise demand** — directly tied to revenue (weight: highest)
2. **Student feedback patterns** — 3+ cohorts citing the same issue (weight: high)
3. **CS escalations** — specific customer complaints about content accuracy (weight: high)
4. **Instructor observations** — practical teaching improvements (weight: medium-high)
5. **Lenny / high-credibility publications** — industry-shaping insights (weight: medium)
6. **Product School events** — proprietary signal (weight: medium)
7. **LinkedIn / Substack** — emerging signal (weight: medium-low)
8. **Reddit** — practitioner signal (weight: low, but valuable for gap detection)

This priority ranking reflects the principle from the AI Product Strategy course: "Talk to users and understand what they want — you can improve the application way more" than by chasing external trends.

---

## Migration Plan — Existing Sources to Library

### Immediate (Phase 1-2)

| Source | Current Location | Action |
|--------|-----------------|--------|
| Lenny insights mapping | `/Product School - AI Product Strategy/lenny-insights.md` | Migrate each source into a signal atom in the library |
| Gokul 8 Moats summary | `/Product School - AI Product Strategy/insights/gokul-rajaram-8-moats-summary.md` | Migrate as evidence atom (framework + case studies) |
| Vibe Coding student feedback synthesis | `/AI Prototyping : Vibe Coding/Insights/AI Prototyping V3 Refinement.txt` | Extract feedback patterns into relevant atom annotations |
| Carlos working session decisions | Multiple meeting notes across Vibe Coding and AI Product Strategy repos | Extract key content decisions into atom teaching notes |
| Dana kickoff transcript | `/AI Prototyping : Vibe Coding/Insights/2025-02-09 Dana-Dejan Kickoff Meeting.md` | Extract content strategy insights |
| Course API content needs sessions | Working sessions with content, enterprise, and platform stakeholders | Extract module contract rules, LMS output needs, and enterprise packaging constraints |

### Near-Term (Phase 3-4)

| Source | Action |
|--------|--------|
| All module speaker notes across 4 repos | Extract frameworks and teaching notes into canonical atoms |
| Interactive HTML tools (11 in AI Product Strategy, several in Vibe Coding) | Catalog as tool atoms linked to framework atoms |
| Competitive analysis (Vibe Coding Appendix B) | Migrate as evidence atoms tracking competitor positioning |

### Ongoing (Phase 5-6)

| Source | Action |
|--------|--------|
| New cohort surveys | Continuous ingestion per pipeline |
| New external publications | Continuous monitoring per source cadence |
| New enterprise engagements | Continuous demand signal capture |
