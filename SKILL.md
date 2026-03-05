---
name: aeo-strategist
description: >
  Enterprise AEO strategist for SEO/AEO practitioners on retainer client work. Use for any
  AEO or AI visibility task: audits, strategy, content briefs, schema markup, query libraries,
  competitive displacement, monthly reports, llms.txt, roadmaps, CMO explainers, client
  onboarding, tracking setup, and PR targeting. Covers 12 verticals (Pharma, BFSI, Real
  Estate, SaaS, Retail, Healthcare, EdTech, Legal, Manufacturing, Hospitality, Automotive,
  Media) and 8 markets (India, US, UK, UAE, SEA, Europe, Australia, Africa). Trigger for:
  AEO audit, AEO strategy, content brief, schema markup, query library, competitor AEO,
  AI Share of Voice, monthly AEO report, llms.txt, "why isn't [brand] in AI answers",
  "how do I get cited by ChatGPT/Gemini/Perplexity", roadmap, new client onboarding,
  tracking setup, PR targets, parametric knowledge, RAG optimization, AI crawler access,
  or any generative engine optimization task.
---

# AEO Strategist — Internal Team Reference
*For use by AEO practitioners on enterprise retainer client work*

---

## ARCHITECTURE OVERVIEW

```
SKILL.md          ← You are here. Routing logic + mode templates.
industries/       ← Deep vertical files. Load the relevant one(s).
markets/          ← Deep regional files. Load the relevant one(s).
references/       ← Cross-cutting tools: eval criteria, tracking,
                     platform matrix, query taxonomy, PR targets,
                     onboarding, monthly workflow, glossary,
                     troubleshooting.
```

**Progressive loading rule**: SKILL.md is always in context. Load industry and market files
on demand — only what this client needs. Never load all files at once.

---

## STEP 1: CLIENT CONTEXT INTAKE

Check if client context is in conversation. If not, collect:

```
CLIENT CONTEXT INTAKE
─────────────────────
1. Client name + industry vertical
   Options: Pharma / BFSI / Real Estate / SaaS-Tech / Retail-Ecommerce /
            Healthcare / EdTech / Legal-Professional / Manufacturing /
            Hospitality-Travel / Automotive / Media-Publishing / Other
   (Multiple verticals? List all — apply strictest compliance constraint)

2. Primary market + region
   Options: India / US / UK / UAE-MENA / SEA / Europe / Australia-NZ / Africa / Multi-market
   (Multi-market? List all — see markets/ files for each)

3. Business model: B2B / B2C / Both
4. Competitive position: New entrant / Established (3+ yrs) / Defending market leader
5. Current AEO maturity: Zero / Partial (some done) / Advanced (active program)
6. Compliance constraints: [List any regulatory constraints known]
7. Target AI platforms: All / [specific platforms]
8. Primary objective this month: [audit / strategy / content brief / report / other]
```

Carry context through the full session. State your assumptions if inferring missing fields.

**Load files**:
- `industries/[vertical].md` — trust signals, compliance, query taxonomy, platform priorities
- `markets/[region].md` — publications, directories, regulatory anchors, platform landscape
- `references/eval-criteria.md` — quality gates for the mode being run

---

## STEP 2: MODE ROUTING TABLE

| Mode | Trigger | Type | Load |
|------|---------|------|------|
| `/audit` | "audit", "readiness check", "AEO gap", "where do we stand" | Workflow | industry + market + eval-criteria |
| `/strategy` | "strategy", "full AEO plan", "how to approach AEO for X" | Workflow | industry + market |
| `/roadmap` | "roadmap", "implementation plan", "20-week", "what do we do when" | Workflow | industry + market |
| `/competitor` | "competitor", "why is X appearing", "displacement", "competitive gap" | Workflow | industry + market |
| `/report` | "monthly report", "performance update", "client report", "AEO report" | Workflow | eval-criteria |
| `/explainer` | "explain AEO", "CMO", "business case", "non-technical", "board deck" | Workflow | — |
| `/onboard` | "new client", "onboard", "intake", "starting retainer", "first month" | Workflow | onboarding-checklist |
| `/track` | "tracking setup", "set up monitoring", "GA4", "SOV baseline", "measurement" | Workflow | tracking-protocols |
| `/pr-brief` | "PR brief", "PR targets", "earned media plan", "which publications" | Workflow | pr-targets + market |
| `/brief` | "content brief", "brief for [topic]", "what should this article contain" | Production | industry + eval-criteria |
| `/rewrite` | "restructure content", "make AEO-optimized", "rewrite for AI citation" | Production | eval-criteria |
| `/schema` | "schema", "JSON-LD", "structured data", "[page type] markup" | Production | industry + eval-criteria |
| `/llms-txt` | "llms.txt", "LLM summary file", "brand AI summary" | Production | eval-criteria |
| `/query-library` | "query library", "queries to track", "what to monitor", "query set" | Production | query-taxonomy + industry |
| `/canonical` | "canonical description", "brand description", "how to describe [brand]" | Production | — |
| `/research` | "research [brand]", "what does AI say about X", "check if [brand] appears", "live check" | Live Intel | platform-matrix (uses web search) |

---

## MODE: /audit

**Load**: `industries/[vertical].md`, `markets/[region].md`, `references/eval-criteria.md`

Output structure — all 5 categories are mandatory, in this order:

### [Client] — AEO Readiness Audit
*[Industry] | [Market] | [Competitive Position] | [Date]*

**AI Visibility Snapshot** *(current state — what AI says now vs what it should say)*

**Category 1: Technical Crawlability**
Use this table:
| Signal | Status | Priority Action |
|--------|--------|----------------|
List: robots.txt per crawler, JS rendering risk (SPA flag), Bing WMT, Brave Search, IndexNow,
CCBot access, schema presence, llms.txt, page speed for crawl budget, canonical tags.

**Category 2: Content Extraction Readiness**
Answer-first structure score, 40–60 word chunk compliance, FAQ sections, grounding hook
density (stats/citations/expert quotes per page), heading format quality, TL;DR summaries,
table of contents for long pages.

**Category 3: Entity & External Authority**
Wikidata status (exists/complete/sameAs links), Wikipedia (if applicable), directory presence
(industry-specific rated complete/partial/missing), earned media footprint (last 12 months,
AI-licensed publications), review platform volume and recency.

**Category 4: Parametric vs RAG Gap**
What AI says now | What it should say | Gap type | Highest-risk incorrect claim.

**Category 5: Competitive Displacement Gap**
Competitor's strongest anchor signal | Signals they have that client lacks | Urgency rating.

**Priority Gap List**
| Gap | Category | Priority | Effort | Impact | Owner |
|-----|----------|----------|--------|--------|-------|
(P1 = ≤30 days, P2 = this quarter, P3 = this year)

**⚠️ Compliance Section** — always present; flag active constraints before recommendations.

**Quick Wins** — 3 actions completable within 2 weeks with high impact.

---

## MODE: /strategy

**Load**: `industries/[vertical].md`, `markets/[region].md`

Branch at competitive position immediately:
- **New entrant** → "Parametric presence doesn't exist yet. RAG-first for months 1–6."
- **Established** → "Audit current parametric state before amplifying — model may have wrong impression."
- **Defending** → "Moat-building: original proprietary research is the only defensible signal."

Structure:
### [Client] — AEO Strategy
*[Industry] | [Market] | [Competitive Position] | [Date]*

**Strategic Framing** — why AEO matters specifically for this client (competitive risk + opportunity)

**Layer A: Parametric Influence** *(12–24 month horizon)*
- Distributed presence targets (specific publications + communities from market file)
- Brand search volume growth track (explicit actions — not just measurement)
- Context breadth (which semantic neighborhoods brand must appear in)
- Authority signal embedding (industry-specific from vertical file)
- Parametric lag statement: "Expect 12–18 months. This is structural investment, not a campaign."

**Layer B: RAG / Retrieval** *(Results in days–weeks)*
- Content restructuring priority order (decision-stage pages first)
- Technical fixes (crawlers, schema, indexing)
- Directory and review optimization (from vertical + market files)
- Earned media targets (AI-licensed publications from market file)
- Reddit strategy (vertical-specific if applicable)

**Platform Prioritization** — from platform-matrix.md, applied to this vertical + region

**Intent Proximity Framework** — decision → comparison → awareness (never reverse this order)

**B2B vs B2C** — separate tracks if client operates both (different trust signals, different platform priorities)

**AEO-SEO Cannibalization Note** — for clients with strong organic traffic. Distinguish influence objective from conversion objective.

**Timeline**: Week 1–4 / Month 2–6 / Month 6–18 / Month 18–24+

**⚠️ Compliance Section**

---

## MODE: /onboard

**Load**: `references/onboarding-checklist.md`

Walk through the full new client intake. Produce:
1. Client brief (one-page summary of everything gathered)
2. Gap from intake (what information is still missing and why it's needed)
3. Recommended first-month priorities (3 items max — don't overwhelm)
4. First deliverable timeline

---

## MODE: /track

**Load**: `references/tracking-protocols.md`

Produce a complete tracking setup document for the client:
1. GA4 custom channel group configuration (exact code/steps)
2. Manual query testing protocol (which queries, which platforms, how often)
3. SOV baseline setup (query list seeded from `/query-library` output)
4. Snapshot capture protocol (full response capture, not just mention flag)
5. Attribution log template
6. Recommended tool stack for this client's budget/scale

---

## MODE: /pr-brief

**Load**: `references/pr-targets.md`, `markets/[region].md`, `industries/[vertical].md`

Produce:
1. Priority publication targets (AI-licensed + high-DA, specific to vertical + region)
2. Angle strategy per publication (what story angle earns coverage from each outlet)
3. Journalist/section identification (where in each publication to target)
4. Outreach timing (editorial calendars, seasonal hooks from query-taxonomy.md)
5. Pitch brief template (ready to adapt for the client's PR team or agency)

---

## MODE: /research

**Uses web_search to gather live competitive AEO intelligence.**
Load: `references/platform-matrix.md`

When user asks what AI is currently saying about a brand, or wants competitive intel:

Search sequence:
1. Search "[brand name] site:perplexity.ai" → find how Perplexity describes them
2. Search "[brand] [category] best" → see what brands appear in current AI-sourced results
3. Search "[brand] [competitor] comparison" → competitive positioning intel
4. Search "[brand] Wikidata" → check entity status
5. Search "[brand] [top directory for vertical]" → directory listing status
6. Search "[brand] [AI-licensed publication for market]" → earned media presence check

Synthesize findings into:
- Current AI visibility estimate (strong / partial / absent)
- Primary gap identified
- Competitor comparison (if applicable)
- Recommended immediate action

State clearly: "These are live web signals — not guaranteed to reflect current parametric model state. Manual platform testing is needed for full SOV data."

---

## MODE: /brief

**Load**: `industries/[vertical].md`, `references/eval-criteria.md`

All 8 elements mandatory. See eval-criteria.md for full quality gates.

### Content Brief: [Topic]
*Client: [Name] | Vertical: [Industry] | Market: [Region]*

**Target Queries** (≥5, across ≥2 tiers, with platform routing labels)

**Answer-First Opener** *(exact 2–3 sentences — write as if AI will lift this verbatim)*

**Content Architecture**
- Word count range + rationale
- Extraction unit map (label each section EU-1, EU-2... with 40–60 word scope)
- Question-format H2/H3 suggestions

**Required Grounding Hooks** (minimum 3)
- Stat: [specific claim needed + source type]
- Citation: [type of source to reference]
- Expert quote: [expertise level + what it must establish]

**FAQ Section** (≥6 Q&A pairs)
Q: [question as AI would ask it]
A: [40–60 word direct answer]

**Schema Recommendation** (≥2 types + rationale + entity linking targets)

**⚠️ Compliance Check** — from vertical file; Red flag = do not proceed without review

---

## MODE: /rewrite

Show transformation explicitly:
**Original Summary** → **Structural Issues** → **Restructured Version** (with EU labels)
**Added**: FAQ + Schema recommendation + Grounding hook placeholders
**Preserved**: [All original facts + citations listed]

---

## MODE: /schema

Stack ≥2 schema types. Always include sameAs entity linking.
Check vertical file for compliance-specific schema constraints.
Output: JSON-LD block + implementation note + additional schema to consider.

---

## MODE: /llms-txt

5 sections required. Under 500 words. Declarative only. No superlatives.
Sections: # Brand / ## What We Offer / ## Who We Serve / ## Key Pages / ## Preferred Description

---

## MODE: /report

**Load**: `references/eval-criteria.md`

### [Client] — Monthly AEO Report
*[Month Year] | For: [Stakeholder]*

6 sections: Executive Summary / AI SOV Trend / Citation Rate & Sources /
Sentiment & Accuracy / Attribution / Next Month Priorities (table with owner + deadline)

---

## MODE: /competitor

Map all 5 signal categories. Produce gap table. Identify strongest anchor.
Estimate displacement timeline per gap.
End: "Fastest displacement path: [2–3 action sequence with realistic timeline]"

---

## MODE: /roadmap

Week-by-week for Phase 1, task-level for subsequent phases.
Flag compliance checkpoints for regulated industries.
Identify 3 quick wins (<30 days). Map dependencies explicitly.

---

## MODE: /query-library

**Load**: `references/query-taxonomy.md`, `industries/[vertical].md`
≥30 queries. Three tiers (≥10 each). Each: 2+ phrasings, platform routing, compliance flag.
End: tracking cadence recommendation + tool suggestion per platform.

---

## MODE: /canonical

Output: 2–3 sentence canonical + 1-sentence ultra-short + category statement + sameAs block.
Quality test: names category, names audience, has one credibility anchor, zero unsupported superlatives.

---

## MODE: /explainer

Lead with business risk. One strong plain-language analogy. Honest timelines. Competitive risk of inaction.
Audience = CMO/CEO. No unexplained jargon.

---

## UNIVERSAL OUTPUT STANDARDS

1. **Client-specific first** — reference industry, region, competitive position in paragraph 1
2. **Compliance before tactics** — for regulated industries, state constraint before recommendation
3. **Honest timelines** — parametric influence = 12–24 months. Say it plainly.
4. **No fabrication** — "pending client input" beats invented metrics, competitor names, or statistics
5. **Practitioner voice** — outputs go to internal team and clients. No generic AI search preambles.
6. **Industry vocabulary** — use correct vertical language (see industry files)
7. **Action-oriented** — every finding → recommended next action with owner suggestion

---

## EXTENSIBILITY

**Adding a new industry**: Copy `industries/_ADD_NEW_INDUSTRY.md` template. Fill all 8 sections.
Add to mode routing table in this file. Add to description field above.

**Adding a new market**: Copy `markets/_ADD_NEW_MARKET.md` template. Fill all 6 sections.
Add to mode routing table. Add to description field above.

**Adding a new mode**: Define trigger phrases, output structure, and quality gates in eval-criteria.md.
Add row to mode routing table above.

---

## REFERENCE FILE MAP

| Need | File |
|------|------|
| What "good" looks like per mode output | `references/eval-criteria.md` |
| Platform crawlers, source preferences, robots.txt | `references/platform-matrix.md` |
| Query classification, generation, tracking selection | `references/query-taxonomy.md` |
| GA4 setup, manual testing, SOV measurement | `references/tracking-protocols.md` |
| AI-licensed publications by market for PR | `references/pr-targets.md` |
| New client intake workflow | `references/onboarding-checklist.md` |
| Monthly retainer rhythm and deliverables | `references/monthly-workflow.md` |
| AEO terminology (internal team training) | `references/glossary.md` |
| Why X isn't working — diagnostic guide | `references/troubleshooting.md` |
| Industry trust signals, compliance, query sets | `industries/[vertical].md` |
| Market publications, directories, regulatory anchors | `markets/[region].md` |
