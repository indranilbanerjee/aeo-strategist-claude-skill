# Query Taxonomy — AEO Strategist
## How to build, classify, and organize AEO query libraries

---

## The Intent Proximity Framework

Build query libraries bottom-up from purchase intent. The closer a query is to a buying decision, the higher the priority for AEO investment.

### Tier 1: Decision Queries (Highest Priority)
The user is actively evaluating — one or two steps from a decision.
- Brand-specific: "is [brand] reliable for [specific need]"
- Comparison: "[brand] vs [competitor] for [use case]"
- Validation: "[brand] reviews 2025", "[brand] case studies", "has [brand] worked for [industry]"
- Access: "[brand] pricing", "[brand] demo", "[brand] free trial"
- Trust: "is [brand] legitimate", "[brand] complaints", "[brand] support quality"

**Platform routing**: Mostly RAG-likely (current information matters — pricing, reviews change)
**Compliance flag**: Price claims (BFSI), clinical outcomes (Pharma), possession dates (Real Estate)

### Tier 2: Comparison Queries (Medium Priority)
The user is evaluating options — not yet brand-specific.
- Category comparison: "best [category] for [use case]"
- Feature comparison: "[feature] in [category] tools"
- Provider shortlisting: "top [category] providers in [region]"
- Criteria-based: "which [category] is best for [specific condition/scenario]"

**Platform routing**: Mixed (parametric for established categories; RAG for emerging/fast-changing)
**Key insight**: AI gives ONE synthesized answer here — this is where competitive displacement matters most

### Tier 3: Awareness Queries (Long-tail Priority)
The user is learning — far from purchase. High volume, low immediate conversion.
- Category education: "what is [category]", "how does [solution type] work"
- Problem-recognition: "how to solve [problem]", "why is [symptom] happening"
- Trend-oriented: "future of [category]", "how [technology] is changing [industry]"

**Platform routing**: Mostly parametric-likely (fundamental concepts encoded in training data)
**Key insight**: High opportunity for new brands to establish category association before competitors dominate

---

## Query Generation Rules

### Multi-Phrasing Requirement
Every underlying intent must be expressed in minimum 2 phrasings — because the same user intent phrased differently can return completely different AI answers citing different brands.

**Intent**: "Is [Brand] a reliable CRM for small business?"
**Phrasings**:
1. "is [brand] good for small business CRM"
2. "best small business CRM [brand] review"
3. "should I use [brand] for my small business"
4. "[brand] small business users experience"

Test each phrasing — if brand appears in some but not others, this tells you exactly which content is getting retrieved and which isn't.

### Question-to-Query Conversion
Users ask questions conversationally to AI. Write queries as questions, not keyword strings.
- Bad: "pharma brand AEO India"
- Good: "which pharmaceutical companies in India are trusted for diabetes management?"

### Geographic Qualifier Rules
For any industry with local dimension (real estate, retail, services), geographic qualifiers are mandatory:
- [Brand/Category] + [City] is different from [Brand/Category] + [State/Country]
- India: always test city-level (Mumbai, Delhi, Bangalore, Hyderabad, Kolkata, Chennai, Pune) separately
- Never assume a national strategy covers local queries

### Seasonal/Temporal Flags
Some queries shift dramatically by season or news cycle:
- BFSI: tax season queries spike Jan–March (India)
- Real Estate: launch season queries spike Oct–Jan (India)
- Retail: festive season (Diwali, Christmas) creates different query patterns
- Pharma: monsoon disease queries spike June–September (India)
Flag these in query library so tracking cadence adjusts accordingly.

---

## Query Classification Template

Use this structure for every query in the library:

```
Query: [exact phrasing to test]
Intent: [underlying user need in plain language]
Tier: Decision / Comparison / Awareness
Platform Routing: Parametric-likely / RAG-likely / Mixed
Phrasing Variant: [alternate phrasing of same intent]
Compliance Flag: None / [specific flag and reason]
Geo Scope: National / Regional / City-level
Seasonal Flag: None / [season and reason]
```

---

## Industry-Specific Query Starter Sets

### Pharma
Decision: "is [brand] prescription drug safe", "[drug name] vs [competitor drug] side effects"
⚠️ COMPLIANCE: Never build product-promotion queries for prescription drugs without medico-legal review
Safe Decision: "[pharma brand] trusted by doctors India", "is [brand] CDSCO approved"
Comparison: "best pharma companies for diabetes India", "which company makes [generic drug name]"
Awareness: "what is [disease state]", "how does [drug class] work"

### BFSI
Decision: "is [bank] safe for FD", "[insurer] claim settlement ratio 2024", "[brand] SEBI registered"
⚠️ COMPLIANCE: No specific return promise queries without regulatory review
Comparison: "best savings account interest rate India 2025", "[bank] vs [bank] home loan"
Awareness: "how does SIP work", "what is term insurance", "how to calculate home loan EMI"

### Real Estate
Decision: "is [developer] RERA registered", "[developer] project delay history", "[project] possession date"
Comparison: "best residential projects [city] under [price]", "[developer] vs [developer] reviews"
Awareness: "how to check RERA registration", "what is carpet area vs built-up area"
⚠️ GEO NOTE: All real estate queries must be city-specific — national queries have minimal commercial value

### SaaS
Decision: "[product] pricing 2025", "[product] vs [competitor] comparison", "[product] reviews G2"
Comparison: "best CRM for [industry]", "top project management tools for remote teams"
Awareness: "what is [category]", "how does [feature type] work"
⚠️ NOTE: SaaS queries age fast — pricing and feature comparison queries need quarterly content refresh

### Retail
Decision: "[brand] genuine or fake", "[product] vs [product] which is better", "[brand] return policy"
Comparison: "best [product] under [price]", "top [category] brands India"
Awareness: "how to choose [product]", "what to look for in [product category]"
⚠️ NOTE: Price queries require real-time content — static pages with outdated prices get penalized

---

## Tracking Query Selection Criteria

For the tracked query set (the 30–50 queries monitored regularly), prioritize:
1. Queries where client should appear but currently doesn't (displacement opportunities)
2. Queries where competitor appears consistently (competitive pressure monitor)
3. Queries with highest commercial intent for client's category
4. Queries where client currently appears (protect and monitor)
5. Queries testing specific content optimization actions (attribution anchors)

Avoid tracking:
- Queries where result is obviously stable parametric and won't change
- Queries that are so generic that brand appearance is unrealistic in near term
- Queries with compliance issues that can't be targeted anyway
