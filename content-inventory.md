# Content Inventory — Cross-Course Atom Mapping

**Purpose:** Map every teachable concept, framework, case study, and evidence point across the four discovered course repositories. Identify cross-course overlaps that need canonical definitions and unique anchors that define each course's identity.

**Scope:** AI Product Strategy, Vibe Coding, AI Agents, AI for PMs. The remaining five certifications (PM, GTM, Experimentation, Leadership, AI Evals) require separate access and inventory.

---

## Cross-Course Overlaps (Canonical Candidates)

These concepts appear in 2+ courses and need a single canonical definition in the shared library. Course-specific depth and examples can vary, but the core definition must be consistent.

### High-Priority Canonicalization

| Concept | AI Product Strategy | Vibe Coding | AI Agents | AI for PMs | Canonical Action |
|---------|:------------------:|:-----------:|:---------:|:----------:|-----------------|
| **Agent Spectrum / Autonomy Levels** | — | — | M1: Helper → Teammate → Operator; L0–L3 | M5: L0–L3 with PM-risk framing | Reconcile level definitions and examples. AI Agents goes deepest; AI for PMs adds PM accountability lens. Single canonical ladder, two teaching depths. |
| **AWSpec (Agent Workflow Spec)** | — | — | M2: Nine-question spec | M5: Four-section blueprint (Actors, Patterns, Memory, Tools) | Merge into single canonical spec. AI Agents version is fuller (nine questions vs. four sections). |
| **Eval Methodology (Multi-Layer Stack)** | M4: Eval dashboard spec, LLM-as-Judge, golden datasets | — | M5: Four eval types (Functional, Reliability, Safety, Factual), trust pipeline | M6: Three-layer stack (Automated, Human, User), human eval rubric | Create canonical eval framework with three views: strategic (AI Product Strategy), technical (AI Agents), operational (AI for PMs). |
| **RAG Architecture & PM Ownership** | M4: Golden datasets, ground truth | — | M4: RAG pipeline, PM ownership (Retriever, KB, Generator) | M3: RAG steps, AI PRD sections, three trade-offs, architecture options | Canonical RAG overview with PM decision points. AI for PMs goes broadest; AI Agents adds memory context; AI Product Strategy frames strategically. |
| **Confidence / Trust UX** | M4: Three-tier confidence UX (>90%, 50–90%, <50%), trust ≠ accuracy | Confidence Line (ambiguity → production) | M1: Autonomy evaluation; M5: Trust pipeline | M4: Three trust gaps (Black Box, Hallucination, Control), AI-UX readiness | Related but distinct: AI Product Strategy = product confidence UX; Vibe Coding = learning confidence arc; AI for PMs = user trust design. Canonical "trust in AI outputs" atom with course-specific applications. |
| **MCP (Model Context Protocol)** | — | M3/M5: Brief demo, design system connection | M2/M4: "USB-C for AI", scoped connectivity, MCP vs. A2A | — | Canonical MCP definition. AI Agents goes deepest. Vibe Coding uses it applied (design systems). |
| **Kill Switch / Vendor Portability** | M2: Model Dependency Kill Switch, 48h swap, abstraction layers | — | — | — | Currently single-course but high reuse potential for AI Agents (multi-model routing) and AI for PMs (vendor selection). |
| **Living PRD / Spec Concept** | Living Strategy (five components across M1–M5) | M4: Living PRD extracted from prototype; M5: Engineering handoff | M6: Deployment Handoff PRD sections | M3: AI PRD with seven new sections | Each course has a different "living document" output. Canonical atom for "why specs should be living" + course-specific spec templates. |
| **Responsible AI / Governance** | M5: Responsible AI maturity ladder, governance as GTM | — | M5: Agent failure modes, debugging stack; M6: Trust layers, governance metrics | M2: Four guardrails (Oversight, Transparency, Bias, Privacy); M6: Governance framework (hard/soft gates) | Canonical governance principles. AI Product Strategy = strategic (sales asset); AI Agents = operational (agent-specific); AI for PMs = foundational (awareness). |
| **Pricing / AI Economics** | M3: Full module — margin war, cascading, hybrid/outcome pricing | — | — | — | Currently single-course but foundational for any PM understanding AI products. High reuse potential. |
| **Shadow AI Audit** | M5: Spotify 1000→15 tools, 5-min checklist | — | — | — | Currently single-course. Relevant for AI Agents (tool sprawl) and enterprise programs. |

### Medium-Priority Canonicalization

| Concept | Courses | Notes |
|---------|---------|-------|
| Deterministic vs. probabilistic software | AI Product Strategy (M1 thesis), AI for PMs (M1 opening) | Both open with this distinction. Needs one canonical framing. |
| Agentic patterns (ReAct, Planner-Executor, etc.) | AI Agents (M2: full playbook of 6 patterns), AI for PMs (M5: two patterns) | AI Agents is authoritative. AI for PMs uses a subset. |
| Memory types (Episodic, Semantic, Vector, External) | AI Agents (M4), AI for PMs (M5) | Nearly identical taxonomy. Merge examples. |
| PM role evolution in AI era | AI Agents (M1: three pillars), AI for PMs (M1: four evolutions) | Different framings of the same shift. Reconcile into one canonical view. |
| Prompt engineering techniques | Vibe Coding (M3: context layering, prompt chaining, living prompt packs), AI for PMs (M1: four dimensions, three layers, strategy matrix) | Different depth and framing. Vibe Coding = applied product prompting; AI for PMs = foundational prompt literacy. |

---

## Course-Specific Anchors (Unique Value Per Course)

These frameworks define each course's identity and are not candidates for cross-course canonicalization. They should exist as atoms tagged to a single primary course.

### AI Product Strategy — Unique Anchors

| Framework | Module | What Makes It Unique |
|-----------|--------|---------------------|
| Six Strategic Questions (Bet → Moat → Margin → Contract → Guardrails → Pitch) | Course arc | The entire course structure; no other course uses this arc |
| Living Strategy (five interconnected components) | Throughline | Course-specific cumulative artifact |
| 5 AI Value Archetypes (Automator, Copilot, Oracle, Creator, Orchestrator) | M1 | Product-type classification with margin/governance profiles |
| 8 Moats (Gokul/Helmer adaptation) | M2 | Investor-grade defensibility scoring |
| Data Flywheel (interaction → capture → improve loops) | M2 | Moat-specific compounding system |
| Model Cascading (cheap triage → frontier model) | M3 | Cost architecture for AI products |
| CPO-level LLMOps levers | M3 | Operational margin management |
| Reliability Contract (promise, measurement, escalation, feedback) | M4 | User-facing trust commitments |
| Compounding vs. Scaling Systems | M5 | Recursive learning design |
| Multi-horizon Roadmap (quick wins / bets / moonshots) | M6 | Board-ready AI roadmap format |
| AI Bet Evaluator | M6 | Meta-tool: use AI to evaluate AI strategy |

### Vibe Coding — Unique Anchors

| Framework | Module | What Makes It Unique |
|-----------|--------|---------------------|
| Confidence Line (ambiguity → clarity → production confidence) | Course arc | The entire course narrative spine |
| Build-Show-Learn-Decide cycle | M1 | Rapid iteration loop; unique to this course's lab format |
| Tool vs. Toy prototypes (Ravi Mehta / Reforge) | M1–M2 | Decision-instrument framing for prototypes |
| Transition Point / 73% failure stat | M4 | When to stop vibing and start structuring |
| Comprehension Debt (8x duplication) | M4 | Why AI-generated code needs structure |
| PM-Engineering Handoff (three artifacts) | M5 | Working prototype + living PRD + hacked-vs-real list |
| Break It exercise format | M1–M6 | Deliberate failure-path pedagogy every module |
| Validation Evidence Brief | M6 | Course deliverable: assumption → build → learn → recommend |

### AI Agents — Unique Anchors

| Framework | Module | What Makes It Unique |
|-----------|--------|---------------------|
| Six Agent System Archetypes (Sequential, Parallel, Critic-Executor, Delegation, Negotiation, Hierarchical) | M3 | Multi-agent topology classification |
| Agentic Pattern Playbook (Planner-Executor, ReAct, Reflection, Tree of Thoughts, Routing, Multi-Agent) | M2 | Complete pattern catalog |
| SMART Memory Governance (Scoped, Monitored, Auditable, Retrievable, Timed) | M4 | Agent-specific memory policy |
| Agent Debugging Stack (Governance → Action → Reasoning) | M5 | Layered diagnosis for agent failures |
| Tooling Fabric (permissions, schemas, rate limits) | M2 | Tool-calling architecture |
| Multi-Agent Collaboration Spec Template | M3 | Design exercise for agent teams |
| MCP vs. A2A distinction | M4 | Vertical tool vs. horizontal agent protocol |
| Deployment Handoff PRD (Logic Spec, Data, Failure Protocol, Autonomy Level) | M6 | Agent-specific production handoff |

### AI for PMs — Unique Anchors

| Framework | Module | What Makes It Unique |
|-----------|--------|---------------------|
| Fake Good vs. Boring Killer | M2 | Counter-intuitive value framing |
| Three-Layer Model (Workflow → Technical AI → Business outcome) | M2 | Line-of-sight from PM work to business results |
| AI Strategy One-Pager (six pillars) | M2 | Compact strategic artifact |
| Strategic Scorecard (Data Readiness, UX Complexity, Risk, Impact) | M2 | 1–5 scoring for AI readiness |
| AI "Iceberg" user flow (Trigger, Processing, Presentation, Feedback) | M4 | UX architecture for AI products |
| Three Trust Gaps (Black Box, Hallucination, Control) | M4 | User-facing trust deficit taxonomy |
| AI-UX Readiness Checklist (L1 functional → L2 verification → L3 magical) | M4 | UX maturity hierarchy |
| Intelligence Tax (Latency, Privacy) | M4 | Hidden costs of AI-native UX |
| Optimization Decision Framework (inconsistent → few-shot; missing knowledge → RAG; wrong voice → fine-tune) | M1 | Diagnostic triage for AI improvement |

---

## Case Studies & Evidence Inventory

### Named Case Studies (Potential Shared Atoms)

| Case Study | Course(s) | Module(s) | Reuse Potential |
|------------|-----------|-----------|----------------|
| Klarna Automator (overcorrection arc) | AI Product Strategy | M3 | High — AI economics lesson applicable to multiple courses |
| Jasper vs. ChatGPT (encroachment) | AI Product Strategy | M2 | High — moat/defensibility lesson |
| Air Canada chatbot liability | AI Product Strategy | M4 | High — trust/governance lesson |
| Samsung data leak | AI Product Strategy | M5 | High — governance lesson |
| Duolingo AI transformation | AI Product Strategy (M6), AI Agents (M5) | M5–M6 | Already shared; canonicalize |
| Spotify examples (Discover Weekly, AI DJ, 1000→15 tools, playlist agents) | AI Product Strategy (M5), AI Agents (M1, M6), AI for PMs (M2) | Multiple | High overlap — consolidate Spotify atoms |
| Salesforce Agentforce | AI Agents (M1, M2) | M1–M2 | Moderate — agent-specific |
| Shopify (non-consumption market; Magic → Sidekick) | AI Product Strategy (Gokul), AI Agents (M1) | M1 | Already shared; canonicalize |
| Notion AI (workspace grounding) | AI for PMs (M3) | M3 | Moderate — RAG/context engineering example |
| Gamma ($100M ARR, non-consumption) | AI Product Strategy (Lenny) | M1 | High — board narrative + non-consumption |
| Figma AI (invisible operator, HITL) | AI Agents (M1), AI for PMs (M4 context) | M1, M4 | Already shared |
| Microsoft Copilot / M365 | AI Agents (M1–M2, M6), AI for PMs (M4) | Multiple | High overlap — consolidate Microsoft atoms |

### Key External Sources (Pre-Curated)

| Source | Course | Module Mapping | Library Status |
|--------|--------|---------------|---------------|
| Lenny: "Counterintuitive advice for AI products" (Jul 2024) | AI Product Strategy | M1 | Migrate to library |
| Lenny: "PM's guide to evals" — Aman Khan (Apr 2025) | AI Product Strategy | M4 | Migrate to library |
| Lenny: "Building eval systems" — Husain & Shankar (Sep 2025) | AI Product Strategy | M4 | Migrate to library |
| Lenny: "Pricing AI products" — Madhavan Ramanujam (Jul 2025) | AI Product Strategy | M3 | Migrate to library |
| Lenny: "25 tactics to accelerate AI adoption" (Aug 2025) | AI Product Strategy | M5 | Migrate to library |
| 20VC: Gokul Rajaram — 8 Moats (Mar 2026) | AI Product Strategy | M2, M3, M6 | Migrate to library |
| Hamilton Helmer — 7 Powers (May 2024) | AI Product Strategy | M2 | Migrate to library |
| OpenAI CPO Kevin Weil (Apr 2025) | AI Product Strategy | M1, M4, M6 | Migrate to library |

---

## Summary Statistics

| Metric | Count |
|--------|-------|
| Total unique frameworks identified | ~120+ |
| Cross-course overlaps requiring canonicalization | 15–20 high and medium priority |
| Named case studies | 25+ |
| Pre-curated external sources | 10+ (from lenny-insights.md alone) |
| Courses with full content access | 4 of 9 |
| Courses requiring separate inventory | 5 (PM, GTM, Experimentation, Leadership, AI Evals) |

---

## Next Steps

1. Resolve high-priority canonical definitions (start with Agent Spectrum, AWSpec, Eval Stack, RAG)
2. Obtain access to remaining 5 course repositories for inventory
3. Begin atom creation for the top 20 cross-referenced concepts
4. Migrate existing external sources (lenny-insights.md, Gokul summary) into library format
