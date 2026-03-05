# AEO Strategist — Claude Cowork Skill

> **The first open-source enterprise AEO skill for Claude.**  
> Turn Claude into a fully-equipped Answer Engine Optimization strategist — with deep compliance awareness, 12 industry verticals, and 8 global markets built in.

Built by **[Indranil "Neel" Banerjee](https://linkedin.com/in/indranilbanerjee)** — Head of AI Transformation, [INT TechShu Digital](https://inttechshu.com).

---

## What This Skill Is — and What It Is Not

This is a **prompt file**. It loads into Claude's context and instructs Claude to behave as a specialist AEO strategist. It generates frameworks, content briefs, schema markup, strategies, reports, and canonical descriptions — based on information you provide combined with Claude's training knowledge of AEO, platforms, and industry compliance.

### What the skill cannot do

**It cannot query AI platforms.** The skill has no ability to open ChatGPT, Gemini, or Perplexity and check what those platforms return for a query. That is platform-locked. No prompt file can do it.

**It cannot check your client's robots.txt, GA4, or Wikidata** on its own. It tells you what to check and how to act on what you find. You do the checking.

**`/research` is a web search mode** — it searches publicly available web pages (news, directories, G2, LinkedIn, Wikidata). It does not test AI platforms.

### The right mental model

You bring observations. The skill structures them into strategy and production outputs.

**You bring:** what you see when you manually test AI platforms, your GA4 numbers, robots.txt findings, directory coverage, competitive observations.  
**The skill generates:** strategy, content briefs, schema, tracking templates, reports — compliance-aware and structured.

---

## Why This Still Saves Enormous Time

Even without execution capability, this is where the value sits:

- A compliant content brief for a Pharma client that takes a senior strategist 2 hours → 5 minutes
- Valid physician JSON-LD with NMC and NABH stacking → 3 minutes
- A structured competitive gap analysis from your manual observations → 8 minutes
- A monthly SOV report formatted for a CMO, from the numbers you paste in → 6 minutes

---

## 16 Modes

| Mode | What It Produces |
|------|-----------------|
| `/audit` | Gap assessment structured from your manual observations — P1/P2/P3 priorities, compliance section |
| `/strategy` | Layer A (parametric, 12–24mo) + Layer B (RAG, immediate) full strategy |
| `/roadmap` | Week-by-week 20-week implementation plan |
| `/onboard` | New client intake checklist + first-month deliverable schedule |
| `/competitor` | Competitive gap map structured from your observations + displacement path |
| `/brief` | 8-element AEO-optimized content brief for writers |
| `/rewrite` | Restructure existing content (which you paste in) for AI extraction |
| `/schema` | Valid JSON-LD ready to copy-paste into the page `<head>` |
| `/llms-txt` | Complete llms.txt under 500 words, ready to deploy |
| `/query-library` | 30+ tracked queries across 3 intent tiers — your manual testing list |
| `/canonical` | Canonical brand description to deploy identically across all platforms |
| `/report` | Monthly AEO report for clients — you paste in the data, skill formats it |
| `/track` | SOV snapshot template + GA4 setup instructions + manual testing protocol |
| `/pr-brief` | PR outreach plan targeting AI-licensed publications by vertical + market |
| `/research` | Web search — public coverage, directories, entity signals (not AI platform results) |
| `/explainer` | AEO business case for CMO/CEO — no jargon, honest timelines |

---

## How to Use Each Mode — Real Scenarios

### Before Any Mode: Set Client Context

```
Client: Fibe (formerly EarlySalary)
Industry: BFSI — Fintech lending (NBFC)
Market: India
Business model: B2C consumer loans
Competitive position: Challenger (vs CASHe, KreditBee)
AEO maturity: Zero
Goal today: Understand why we don't appear in AI answers and build a plan
```

Claude carries this context forward through all mode calls in the session.

---

### Scenario 1: Pharma Client — Audit + Brief

**Client:** Mankind Pharma (OTC consumer health, India)  
**Prerequisite — you manually test first:**
- Open Gemini: type *"best OTC medicine for mild fever India"* — record which brands appear, which sources are cited
- Check `mankind.in/robots.txt` — is CCBot blocked?
- Check Wikidata — does an entry exist?
- Check 1mg/Practo/Apollo — are OTC products listed with disease-state categorisation?

**Then run the audit, bringing your findings:**

```
/audit
Client: Mankind Pharma
Vertical: Pharma (OTC consumer health)
Market: India
Competitors: Cipla OTC, Himalaya, Sun Pharma

What I checked manually:
- Gemini "best OTC fever medicine India": Crocin and Himalaya appear.
  Mankind not mentioned. Both cited via structured product pages.
- ChatGPT same query: Cipla paracetamol cited via Netmeds article.
  Mankind not mentioned.
- robots.txt: CCBot blocked. GPTBot blocked.
- Wikidata: No Mankind Pharma entry found.
- 1mg: Products listed but no disease-state categorisation.
- Website: React SPA, no server-side rendering detected.
```

**What Claude produces — structured from your observations:**
- 5-category gap assessment with P1/P2/P3 priority list
- Technical fixes ranked by effort/impact (CCBot unblock = P1, 30 mins)
- ⚠️ CDSCO compliance section: OTC content only, Schedule H drugs must never carry efficacy claims, medico-legal review required before any content goes live

**Then generate the content brief:**

```
/brief
Client: Mankind Pharma
Topic: What are safe OTC options for mild fever in adults?
Audience: General consumer, tier-2 India
Compliance: CDSCO — OTC only, standard disclaimer, no Rx drug mention
Target: Gemini primary, ChatGPT secondary
```

Output: Answer-first opener, 6 FAQ pairs, 3 grounding hooks, schema recommendation, and a hard compliance flag flagging any Schedule H reference risks. Goes to your writers, then through the client's medico-legal team before publishing.

---

### Scenario 2: Fintech — Competitor Analysis

**Client:** Fibe vs CASHe  
**Prerequisite — you check manually:**
- Open Perplexity: type *"best instant loan app India"* — does CASHe appear? What source does Perplexity cite?
- Check BankBazaar: review count for CASHe vs Fibe (publicly visible)
- Check Wikidata: does CASHe have an entry? Does Fibe?

**Then run competitor analysis, supplying your observations:**

```
/competitor
Client: Fibe (formerly EarlySalary)
Competitor: CASHe
Market: India
Vertical: BFSI — Fintech lending (NBFC)

My observations:
- Perplexity "best instant loan app India": CASHe appears via
  BankBazaar and a recent Moneycontrol roundup. Fibe not mentioned.
- BankBazaar: CASHe ~290 reviews, profile 100% complete.
  Fibe ~18 reviews, profile ~60% complete, no EMI calculator.
- Wikidata: CASHe has an entry. Fibe has none.
- Content: CASHe blog has ~14 recent loan-topic articles.
  Fibe blog: 3 articles, none structured answer-first.
- Earned media: CASHe has 3 Inc42 articles in past year. Fibe: none recent.
```

**What Claude produces — structured from what you reported:**
```
COMPETITIVE FOOTPRINT MAP: CASHe vs Fibe

Signal 1 — Technical crawlability: [Based on what you reported]
Signal 2 — Content extraction:     CASHe leads per your count.
                                    14 articles vs 3. Fibe content
                                    not structured for AI extraction.
Signal 3 — Entity authority:        CASHe leads per your check.
                                    Wikidata confirmed. Fibe absent.
Signal 4 — Earned media recency:    CASHe leads per your finding.
                                    3 articles in past year vs none.
Signal 5 — Directory completeness:  CASHe leads per your check.
                                    BankBazaar 100%, 290+ reviews.
                                    Fibe 60%, 18 reviews.

STRONGEST ANCHOR driving CASHe citations (per your Perplexity test):
BankBazaar profile completeness + recent earned media. Perplexity
is pulling from BankBazaar for this query.

DISPLACEMENT PATH:
1. Create Wikidata entry for Fibe [2–4 hours — P1]
2. Complete BankBazaar profile + 50 new reviews [4 weeks]
3. Publish 8 answer-first loan articles [4–6 weeks]
→ Expected: Perplexity RAG change visible 6–8 weeks after sources
  are indexed. ChatGPT parametric: 12+ months — tell client upfront.
```

**Then lock the brand entity:**

```
/canonical
Client: Fibe (formerly EarlySalary)
Key facts: RBI-registered NBFC, 35L+ loans disbursed, avg disbursal
  under 8 minutes, credit limit up to ₹5 lakh, founded 2015 Pune
```

Output: One canonical paragraph to deploy identically to website About, Wikidata, LinkedIn, BankBazaar, Crunchbase. Identical wording everywhere — variation fragments the entity in AI systems.

---

### Scenario 3: Real Estate — Schema + Bengali AEO

**Client:** Ambuja Neotia Group (Kolkata, premium developer)

**Prerequisite — test Bengali queries manually:**  
Open Gemini, type *"রাজারহাটে ফ্ল্যাট কিনতে চাই"* — does any coherent Bengali real estate content appear? If your test confirms near-zero optimised Bengali answers, you have a first-mover opportunity — but verify before briefing writers.

**Generate schema with HIRA compliance:**

```
/schema
Client: Ambuja Neotia
Page: "The Condor" luxury apartments
Location: Action Area II, Rajarhat New Town, Kolkata 700156
HIRA: HIRA/P/NOR/2023/000XXX
Price: ₹1.8 Cr – ₹3.5 Cr | Units: 180 | 3BHK + 4BHK
Status: Under construction
```

Output: Valid JSON-LD with HIRA number in `hasCredential`, address at locality level for hyperlocal geo-signal.  
⚠️ Compliance note included: "Do not commit possession date as a schema value — use 'expected December 2026' in description field until HIRA schedule is confirmed."

**Query library with Bengali variants:**

```
/query-library
Client: Ambuja Neotia
Market: Kolkata
Include: Bengali language variants
```

Output: 35+ queries across 3 tiers including Bengali variants — this is your monthly manual testing list, not automated monitoring.

---

### Scenario 4: B2B SaaS — Audit Surfaces Real Blockers

**Client:** Leena AI (HR automation, US market)

**Prerequisite — manual checks:**
- Open Perplexity: type *"best HR automation software 2025"* — does Leena AI appear? What does Perplexity cite?
- Check G2: Leena AI review count vs ServiceNow (publicly visible on g2.com)
- Run `site:docs.leena.ai` in Bing — is documentation indexed?
- Check r/humanresources on Reddit — any organic Leena AI mentions?

**Run audit with your findings:**

```
/audit
Client: Leena AI
Vertical: SaaS-Tech (HR automation)
Market: US primary + India secondary
Certifications: SOC 2 Type II, ISO 27001, GDPR

What I checked:
- Perplexity "best HR automation software": ServiceNow and Moveworks
  appear. Perplexity cites Gartner MQ page and G2 category listing.
  Leena AI not mentioned.
- G2: Leena AI has 47 reviews. ServiceNow 4,200+. Leena AI is
  "High Performer" not "Leader".
- Bing site:docs.leena.ai — documentation not indexed.
- Reddit r/humanresources: No Leena AI organic mentions found.
```

**What the audit identifies from your data:**
> *"Perplexity is citing G2's category page (per your test). At 47 reviews, Leena AI doesn't appear in G2's 'top products' section — that is what Perplexity extracts. A 90-day G2 review drive targeting 100 reviews is the fastest single action to shift Perplexity citation behaviour. docs.leena.ai not indexed in Bing means it's invisible to Bing-grounded ChatGPT. Submit to Bing Webmaster Tools today."*

---

### Scenario 5: Healthcare — Doctor Profiles + Compliance

**Client:** Manipal Hospitals  
**Key principle:** Named clinicians with verifiable credentials are the #1 AI trust signal for healthcare. Doctor profiles come before any other content type.

```
/schema
Client: Manipal Hospitals
Page type: Physician profile
Doctor: Dr. Ramesh Babu — Senior Interventional Cardiologist
Qualifications: MBBS Manipal, MD Cardiology, DM AIIMS Delhi,
  Fellowship Cleveland Clinic
NMC Registration: Karnataka Medical Council #XXXXX
Experience: 22 years, 5000+ cardiac procedures
Hospital: Manipal Hospital, Old Airport Road, Bangalore
```

Output — copy-paste ready JSON-LD with stacked Physician + Person schema, NABH credential in `worksFor`, NMC registration in `hasCredential`. Validate in Rich Results Test before deploying.

---

## Installation

### Option 1 — Claude Cowork (Recommended)
1. Download the `.skill` file from [Releases](../../releases)
2. Drop into your Cowork skills folder
3. Start a session → `/onboard [client name]`

### Option 2 — Claude.ai
1. `git clone https://github.com/indranilbanerjee/aeo-strategist-claude-skill.git`
2. Paste `SKILL.md` contents as your first message in a new Claude conversation
3. Load the relevant industry + market file
4. Set client context, run any mode

### Option 3 — API
```python
import anthropic
from pathlib import Path

def load_skill(base_path, industry, market):
    base = Path(base_path)
    skill = (base / "SKILL.md").read_text()
    ind_file = base / "industries" / f"{industry.lower().replace(' ','-')}.md"
    mkt_file = base / "markets" / f"{market.lower().replace(' ','-')}.md"
    return "\n\n---\n\n".join([
        skill,
        ind_file.read_text() if ind_file.exists() else "",
        mkt_file.read_text() if mkt_file.exists() else ""
    ])

client = anthropic.Anthropic()
response = client.messages.create(
    model="claude-opus-4-5",   # sonnet-4-6 for /brief, /schema, /rewrite
    max_tokens=4096,
    system=load_skill("./aeo-strategist", "pharma", "india"),
    messages=[{"role": "user", "content": """/audit
Client: Cipla Limited
Vertical: Pharma (OTC + branded generics)
Market: India
Competitive position: Established

What I checked manually:
- [paste your platform test observations here]
- [robots.txt findings]
- [Wikidata check]"""}]
)
print(response.content[0].text)
```

Note: The API code formats and structures your audit inputs. The actual platform testing (opening ChatGPT, Gemini, Perplexity and recording what they return) is manual work done before calling the API.

---

## Repository Structure

```
aeo-strategist/
├── SKILL.md                    ← Main brain — always load this
├── USAGE_GUIDE.md              ← Complete guide with full scenarios (start here)
├── industries/                 ← Load only what your client needs
│   ├── pharma.md               CDSCO/FDA/EMA compliance + 8 sub-verticals
│   ├── bfsi.md                 SEBI/RBI/IRDAI/FCA/SEC + 9 sub-verticals
│   ├── healthcare.md           NABH/JCI/NMC/CQC
│   ├── real-estate.md          RERA/HIRA, hyperlocal, vernacular India
│   ├── saas-tech.md            G2/Gartner, SOC 2, DPDP Act, Reddit strategy
│   ├── retail-ecommerce.md     BIS mandatory, FSSAI, Google Shopping
│   ├── edtech.md               UGC/AICTE/NAAC
│   ├── legal-professional.md   Bar Council, ICAI, advertising rules
│   ├── manufacturing.md        ISO, BIS, export credentials
│   ├── hospitality-travel.md   FSSAI, TripAdvisor, Ministry of Tourism
│   ├── automotive.md           ARAI, BNCAP, FAME II EV
│   ├── media-publishing.md     AI licensing deals, DAVP
│   └── _ADD_NEW_INDUSTRY.md    Template — add any vertical in 30 mins
├── markets/                    ← Load only the market(s) for your client
│   ├── india.md                20+ regulators, all directories, vernacular guide
│   ├── us.md                   Reddit strategy, Gartner, AI Overviews
│   ├── uk.md                   FCA, Companies House, CQC
│   ├── uae-mena.md             Dubai, KSA, Qatar, Arabic AEO
│   ├── sea.md                  SG, ID, MY, PH, TH, VN
│   ├── europe.md               DACH, France, EU AI Act
│   ├── australia-nz.md         TGA, ASIC, ABN signals
│   ├── africa.md               NG, ZA, KE, WhatsApp AI
│   └── _ADD_NEW_MARKET.md      Template — add any market in 30 mins
├── references/
│   ├── tracking-protocols.md   6-layer SOV measurement system
│   ├── onboarding-checklist.md New client intake SOP
│   ├── monthly-workflow.md     Week-by-week retainer rhythm
│   ├── pr-targets.md           AI-licensed publications by tier + market
│   ├── platform-matrix.md      All AI platforms: crawlers, signals, checklists
│   ├── glossary.md             50+ terms for team training
│   └── troubleshooting.md      8 common failures + diagnostic fixes
└── evals/evals.json
```

---

## Monthly Retainer Rhythm

```
WEEK 1 — MEASURE (you do this manually)
  Open ChatGPT, Gemini, Perplexity — type each tracked query — record results
  Pull GA4 AI referral channel | Check GSC branded search trend

WEEK 2 — PRODUCE (skill + you)
  Run /brief for 2 content pieces → send to writers
  Validate schema in Rich Results Test | Update directory listings

WEEK 3 — EARN (skill for the brief, you for the outreach)
  /pr-brief → your team sends the pitches
  Reddit / LinkedIn / Quora community participation

WEEK 4 — REPORT + PLAN (you paste the data, skill formats it)
  /report with your SOV numbers + GA4 data → client delivery
  Queue next month content briefs with /brief
```

Every quarter: `/audit` refresh (with fresh manual tests) + `/competitor` re-run + expand query library.

---

## Common Mistakes

| Mistake | Why It Matters | Fix |
|---------|---------------|-----|
| Running modes with no manual observations | Generic output with no specificity | Do the platform tests and checks first. Bring the data. |
| Treating `/competitor` output as independently verified | Every claim traces back to what you told Claude | Verify your observations yourself before including in a client deliverable |
| Promising results in 60 days | Sets wrong expectations | RAG: 4–8 weeks. Parametric: 12–18 months. Use `/explainer` on Day 1. |
| CCBot blocked in robots.txt | Removes brand from AI training data | P1 fix, 30 minutes. Check every new client on Day 1. |
| GA4 shows zero AI traffic = "AEO not working" | WhatsApp AI, Copilot, private ChatGPT leave no GA4 trace | SOV snapshot + GSC branded search are the right proxies |

---

## Read the Full Guide

**→ [USAGE_GUIDE.md](./USAGE_GUIDE.md)** — complete walkthroughs for all 5 client scenarios, every mode with exact inputs and sample outputs, team structure, API examples, common mistakes in detail, 20+ FAQ.

---

## License & Contributing

MIT license. PRs welcome for new industries, markets, updated regulatory info, and eval cases.  
Use `_ADD_NEW_INDUSTRY.md` / `_ADD_NEW_MARKET.md` templates.

---

## Author

**Indranil "Neel" Banerjee** — Head of AI Transformation, INT TechShu Digital  
[LinkedIn](https://linkedin.com/in/indranilbanerjee) · [GitHub](https://github.com/indranilbanerjee) · [NeelVerse](https://indranil.in)
