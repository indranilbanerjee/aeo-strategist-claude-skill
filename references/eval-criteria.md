# AEO Strategist — Eval Criteria
## What "good" looks like for every mode

This file defines the verifiable success criteria for each mode output.
Use during skill testing, benchmarking, and regression checks.

---

## /audit — AEO Readiness Assessment

**Must contain all 5 audit categories:**
1. Technical crawlability (robots.txt, JS rendering risk, Bing/Brave indexing, schema presence)
2. Content extraction readiness (answer-first structure, 40–60 word chunk compliance, FAQ sections)
3. Entity & external authority (Wikidata/Wikipedia status, directory presence, earned media footprint)
4. Parametric vs RAG visibility gap (what AI currently says vs what it should say)
5. Competitive displacement gap (what competitor trust signals exist that client lacks)

**Must produce:**
- Priority tiered gap list: P1 (≤30 days), P2 (this quarter), P3 (this year)
- Effort/impact score per gap (High/Med/Low × High/Med/Low)
- Compliance flag section if regulated industry
- JS rendering warning if client uses SPA without SSR
- At least one platform-specific finding per major platform

**Must NOT contain:**
- Generic tips without client-specific context
- Recommendations without effort/impact assessment

---

## /strategy — Full AEO Strategy Document

**Must branch at competitive position:**
- New entrant → RAG-first track
- Established brand → Correction + amplification track
- Defending → Moat-building track (original research architecture)

**Must contain:**
- Layer A strategy (parametric influence, 12–24 month horizon)
- Layer B strategy (RAG/retrieval, immediate)
- Platform prioritization with rationale
- Intent proximity framework (decision → comparison → awareness)
- Brand search volume growth track (explicit, not just measurement)
- Industry trust signal hierarchy (from industry module)
- Regional authority targets
- Realistic timeline with parametric lag stated
- AEO-SEO cannibalization note for high-traffic organic clients
- B2B vs B2C framing applied correctly

---

## /brief — AEO Content Brief

**Must contain all 8 required elements:**
1. Target queries (≥5, across ≥2 intent tiers)
2. Answer-first opener (2–3 sentence direct answer)
3. ≥3 grounding hooks (stat + citation + expert quote placeholder)
4. FAQ section (≥6 Q&A pairs, each answer 40–60 words)
5. Schema type recommendation (≥2 types with rationale)
6. Chunk structure guidance (which paragraphs are extraction units)
7. Optimal word count range with rationale
8. Compliance flag section

**Must NOT contain:**
- Marketing superlatives without evidence
- FAQ answers >80 words
- Missing compliance section for pharma/BFSI

---

## /rewrite — Content Restructuring for AEO

**Must demonstrate all structural transformations:**
- Answer-first opener added
- Paragraphs split into labeled 40–60 word extraction units
- FAQ section added (≥4 pairs)
- Grounding hook placeholders inserted
- Schema recommendation appended
- Original meaning and citations preserved

---

## /schema — JSON-LD Schema Generation

**Must produce:**
- Valid deployable JSON-LD (no syntax errors)
- ≥2 schema types stacked
- Organization schema for brand pages
- sameAs entity linking (≥LinkedIn + one industry directory)
- No deprecated properties
- Pharma: MedicalWebPage, no promotional claims
- BFSI: FinancialService type, regulatory ref where applicable
- Real Estate: LocalBusiness + RERA reference

---

## /llms-txt — Brand LLM Summary File

**Must contain all 5 sections:**
1. Brand identity block
2. What we offer (declarative, non-promotional)
3. Who we serve
4. Key pages with URLs
5. Preferred description (canonical 2–3 sentence text)

Under 500 words, declarative language, no superlatives.

---

## /report — Monthly AEO Performance Report

**Must contain 6 sections:**
1. Executive summary (3–4 sentences, non-technical)
2. AI Share of Voice trend (platform breakdown)
3. Citation rate and sources
4. Sentiment and accuracy check (inaccuracies flagged)
5. Attribution (actions → visibility correlations with date anchors)
6. Next month priorities (≤5, ordered, with owner + deadline)

---

## /competitor — Competitive Displacement Analysis

**Must map 5 signal categories:**
1. Earned media coverage
2. Directory/review presence
3. Wikipedia/Wikidata status
4. Reddit presence
5. Parametric strength estimate

**Must produce:**
- Gap vs competitor table
- Priority displacement targets
- Displacement timeline estimate
- "Strongest anchor" identification

---

## /roadmap — Customized 20-Week Implementation Plan

Week-by-week across 4 phases. Must include:
- Compliance checkpoint timing for regulated industries
- Resource allocation (who does what)
- Quick wins (<30 days)
- Dependency mapping

---

## /query-library — Tracked Query Set

≥30 queries across 3 tiers (≥10 each):
- Decision tier: brand-specific, purchase-proximate
- Comparison tier: category evaluation
- Awareness tier: discovery-stage

Each query: ≥2 phrasing variants, platform routing label, compliance flag if applicable.

---

## /canonical — Brand Description

**Must produce:**
- 2–3 sentence canonical description
- 1-sentence ultra-short variant
- Category association statement
- Entity linking block (sameAs targets)

No superlatives, factual entity language, category ownership explicit.

---

## /explainer — Non-Technical AEO Explanation

**Must contain:**
- Business case (revenue risk + competitive position)
- 1–2 plain-language analogies for LLM mechanics
- Honest timeline expectations
- Investment framing
- Risk of inaction

No jargon without plain-language translation.

---

## Universal Quality Gates (all modes)

1. Client-specific (references industry, region, competitive position)
2. Compliance-aware (flags regulated constraints before recommending)
3. Honest complexity (states 12–18 month timelines when true)
4. No marketing language in technical outputs
5. Action-oriented (every finding → next action)
6. No fabrication (no invented competitor names, statistics, or platform data)
