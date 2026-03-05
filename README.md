# AEO Strategist — Claude Cowork Skill

> **The first open-source enterprise AEO skill for Claude.**  
> Turn Claude into a fully-equipped Answer Engine Optimization strategist — with deep compliance awareness, 12 industry verticals, and 8 global markets built in.

Built by **[Indranil "Neel" Banerjee](https://linkedin.com/in/indranilbanerjee)** — Head of AI Transformation, [INT TechShu Digital](https://inttechshu.com).

---

## Why This Exists

30–50% of informational search queries in 2025 never reach a website. They get answered directly inside ChatGPT, Gemini, Perplexity, or Copilot. If your client's brand isn't being cited in those AI answers — they're invisible to a fast-growing segment of their audience.

**SEO gets you ranked. AEO gets you cited.**

This skill gives Claude everything it needs to run an enterprise AEO practice:
- Deep compliance knowledge for regulated industries (Pharma, BFSI, Healthcare)
- Trust signal hierarchies per vertical — what AI actually weights, not what people assume
- Measurement systems for something with no Search Console equivalent
- Production-ready outputs: schema, content briefs, llms.txt, query libraries, PR briefs
- Complete retainer delivery workflow from client onboarding to monthly reporting

---

## 16 Modes — What You Can Do

| Mode | What It Produces |
|------|-----------------|
| `/audit` | Full AEO readiness assessment — 5 categories, gap list P1/P2/P3, compliance section |
| `/strategy` | Layer A (parametric, 12–24mo) + Layer B (RAG, immediate) full strategy |
| `/roadmap` | Week-by-week 20-week implementation plan |
| `/onboard` | New client intake — 7-section checklist, quick wins, first deliverable timeline |
| `/competitor` | 5-signal competitive footprint map + displacement strategy with timeline |
| `/brief` | 8-element AEO-optimized content brief ready for writers |
| `/rewrite` | Restructure existing content for AI extraction |
| `/schema` | Valid JSON-LD with stacked types + entity linking — copy-paste ready |
| `/llms-txt` | Complete llms.txt under 500 words, ready to deploy |
| `/query-library` | 30+ tracked queries across 3 intent tiers for SOV measurement |
| `/canonical` | Canonical brand description for cross-platform entity consolidation |
| `/report` | Monthly AEO performance report — client-ready |
| `/track` | GA4 setup, SOV baseline protocol, 6-layer measurement system |
| `/pr-brief` | PR outreach plan targeting AI-licensed publications by vertical + market |
| `/research` | Live web search — what AI says about any brand right now |
| `/explainer` | AEO business case for CMO/CEO — no jargon, honest timelines |

---

## Real-World Scenarios

### Scenario 1: Pharma Client — "Why aren't we in AI answers?"

**Client:** Mankind Pharma (Indian OTC pharma)  
**Problem:** User asks *"best OTC medicine for mild fever India"* — Crocin and Himalaya appear. Mankind doesn't.

**Step 1 — Check what AI is actually saying right now:**
```
/research
Brand: Mankind Pharma
Category: OTC medicines India — fever, pain, digestive health
Competitors: Cipla OTC, Himalaya, Sun Pharma OTC
```

Claude searches live and returns:
> *"ChatGPT cites Cipla via a 2024 Moneycontrol article and Himalaya via their structured OTC product pages. Mankind appears in 1 of 5 test queries via an old 2022 Pharmabiz article. Three primary gaps: CCBot likely blocked in robots.txt (removing them from AI training data), no Wikidata entity entry, no structured disease-state content."*

**Step 2 — Full audit:**
```
/audit
Client: Mankind Pharma
Vertical: Pharma (OTC consumer health)
Market: India
Competitive position: Established
Competitors: Cipla OTC, Himalaya, Sun Pharma
Note: Website appears to be React SPA — suspect no server-side rendering
```

Produces 5-category assessment with compliance section that flags:
> *"⚠️ CDSCO: OTC content only for consumer-facing pages. Schedule H prescription drugs must never appear with efficacy claims. Medico-legal review required before any content goes live."*

**Step 3 — Generate the first content brief:**
```
/brief
Client: Mankind Pharma
Topic: What are safe OTC options for mild fever in adults?
Audience: General consumer, tier-2 India
Compliance: CDSCO — OTC only, include standard disclaimer, no Rx drug mention
Target: Gemini primary, ChatGPT secondary
```

Output includes answer-first opener, 6 FAQ pairs at 40–60 words each, grounding hooks with CDSCO-compliant references, schema recommendation (MedicalWebPage + FAQPage), and a hard compliance flag:
> *"Do not reference Dolo 650 — it is Schedule H1. Confirm medico-legal clearance before publishing."*

---

### Scenario 2: Fintech Startup — Competitor owns every AI answer

**Client:** Fibe (formerly EarlySalary — instant personal loans, India)  
**Problem:** *"Best instant loan app India"* returns CASHe, KreditBee, MoneyTap. Fibe doesn't appear.

**Run competitor analysis:**
```
/competitor
Client: Fibe (formerly EarlySalary)
Competitor: CASHe
Market: India
Vertical: BFSI — Fintech lending (NBFC)
```

**Output:**
```
COMPETITIVE FOOTPRINT MAP: CASHe vs Fibe
─────────────────────────────────────────
Signal 1 — Technical:     EQUAL. Both indexed. Both have basic schema.
Signal 2 — Content:       CASHe WINS. 14 answer-first loan articles.
                          Fibe has 3, none structured for AI extraction.
Signal 3 — Entity:        CASHe WINS. Wikidata entry (QID Q116486229).
                          Wikipedia redirect exists. Fibe: neither.
Signal 4 — Earned media:  EQUAL. Both covered in Moneycontrol + ET.
Signal 5 — Directories:   CASHe WINS. BankBazaar profile 100% complete.
                          Fibe profile: 60% complete, no EMI calculator.

STRONGEST ANCHOR: Wikidata + Wikipedia entity presence.

FASTEST DISPLACEMENT PATH:
1. Create Wikidata entry for Fibe [2–4 hours]
2. Complete BankBazaar profile + 50 new reviews [4 weeks]
3. Publish 8 answer-first personal loan articles [4–6 weeks]
→ Perplexity citation: 6–8 weeks. ChatGPT parametric: 12+ months.
```

**Lock the brand entity with `/canonical`:**
```
/canonical
Client: Fibe (formerly EarlySalary)
Category: Instant personal loan app for salaried professionals
Key facts: RBI-registered NBFC, 35L+ loans disbursed, avg disbursal
  under 8 minutes, credit limit up to ₹5 lakh, founded 2015 Pune
```

Output is one paragraph deployed identically to website About, Wikidata, LinkedIn, BankBazaar, Crunchbase — everywhere. Identical wording is what builds entity coherence.

---

### Scenario 3: Real Estate — Hyperlocal + Bengali AEO

**Client:** Ambuja Neotia Group (premium Kolkata developer)  
**Insight:** Bengali real estate queries are completely unoptimized. Near-zero competition.

```
/query-library
Client: Ambuja Neotia | Market: Kolkata | Include: Bengali variants
```

**Output includes:**
```
DECISION-STAGE (track on Gemini):
• "Ambuja Neotia HIRA registered Kolkata"
• "luxury apartments Rajarhat New Town price 2025"

BENGALI VARIANTS — first-mover opportunity:
• "রাজারহাটে ফ্ল্যাট কিনতে চাই"   [Want to buy flat in Rajarhat]
• "আম্বুজা নিওটিয়া নতুন প্রজেক্ট" [Ambuja Neotia new project]
• "কলকাতায় বাড়ি কেনা গাইড"        [Guide to buying home in Kolkata]

NOTE: Gemini supports Bengali AI Overviews. These have near-zero
optimized competition. First structured Bengali content wins and
holds position for 12+ months.
```

---

### Scenario 4: B2B SaaS — Breaking into US Market

**Client:** Leena AI (HR automation SaaS)  
**Key audit finding:**
```
/audit
Client: Leena AI
Vertical: SaaS-Tech (HR automation)
Market: US
```

> *"G2 profile has 47 reviews. ServiceNow has 4,200+. AI systems treat G2 review volume as a proxy for market legitimacy. A 90-day G2 review drive targeting 100 reviews directly shifts Perplexity citation behavior — Perplexity reads G2 as a trusted source.*
> 
> *Reddit gap: No presence on r/humanresources (340K members). OpenAI has a licensing deal with Reddit — this directly affects ChatGPT parametric responses."*

---

### Scenario 5: Healthcare — Doctor Profiles Drive AI Citations

**Client:** Manipal Hospitals  
**Insight:** Named clinicians with verifiable credentials outperform hospital brand claims in AI answers.

```
/schema
Client: Manipal Hospitals
Page: Physician profile — Dr. Ramesh Babu, Senior Interventional Cardiologist
Qualifications: MBBS Manipal, MD Cardiology, DM AIIMS Delhi, Fellowship Cleveland Clinic
NMC Registration: Karnataka Medical Council #XXXXX
Experience: 22 years, 5000+ cardiac procedures
```

**Output — copy-paste ready JSON-LD:**
```json
{
  "@context": "https://schema.org",
  "@type": ["Physician", "Person"],
  "name": "Dr. Ramesh Babu",
  "jobTitle": "Senior Interventional Cardiologist",
  "worksFor": {
    "@type": "Hospital",
    "name": "Manipal Hospitals",
    "hasCredential": {"@type": "EducationalOccupationalCredential",
                      "credentialCategory": "NABH Accreditation"}
  },
  "hasCredential": [
    {"@type": "EducationalOccupationalCredential",
     "credentialCategory": "DM Cardiology",
     "recognizedBy": {"@type": "Organization", "name": "AIIMS Delhi"}},
    {"@type": "EducationalOccupationalCredential",
     "name": "NMC Registration", "identifier": "KMC-XXXXX"}
  ],
  "medicalSpecialty": "Interventional Cardiology",
  "sameAs": ["https://www.practo.com/bangalore/doctor/dr-ramesh-babu"]
}
```

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

### Option 3 — API / Code
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
    model="claude-opus-4-5",
    max_tokens=4096,
    system=load_skill("./aeo-strategist", "pharma", "india"),
    messages=[{"role": "user", "content": """/audit
Client: Cipla Limited
Vertical: Pharma (OTC + branded generics)
Market: India
Competitive position: Established
AEO maturity: Zero"""}]
)
print(response.content[0].text)
```

**Model guide:** `claude-opus-4-5` for `/audit`, `/strategy`, `/competitor`, `/report` — `claude-sonnet-4-6` for `/brief`, `/schema`, `/rewrite`, `/canonical`

---

## Repository Structure

```
aeo-strategist/
├── SKILL.md                    ← Main brain — always load this
├── USAGE_GUIDE.md              ← Complete guide with all scenarios (start here)
├── industries/                 ← Load only what your client needs
│   ├── pharma.md               CDSCO/FDA/EMA + 8 sub-verticals
│   ├── bfsi.md                 SEBI/RBI/IRDAI/FCA/SEC + 9 sub-verticals
│   ├── healthcare.md           NABH/JCI/NMC/CQC
│   ├── real-estate.md          RERA/HIRA, hyperlocal, vernacular India
│   ├── saas-tech.md            G2/Gartner, SOC 2, DPDP Act, Reddit
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
WEEK 1 — MEASURE
  SOV snapshot: 20 queries × 3 platforms × 3 tests
  GA4 AI referral channel review | GSC branded search trend

WEEK 2 — PRODUCE
  2 content pieces (run /brief before each)
  Schema validation | Directory updates

WEEK 3 — EARN
  2–3 PR pitches from /pr-brief output
  Reddit / LinkedIn / Quora community participation

WEEK 4 — REPORT + PLAN
  /report → internal review → client delivery
  Queue next month content briefs
```

Every quarter: `/audit` refresh + `/competitor` re-run + expand query library.

---

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| No client context before running modes | Always set 7-field context first — Claude uses it for compliance routing |
| Promising results in 60 days | RAG: 4–8 weeks. Parametric: 12–18 months. Use `/explainer` to set this on Day 1 |
| CCBot blocked in robots.txt | P1 fix, 30 minutes, removes brand from AI training data — check every new client Day 1 |
| GA4 shows zero AI traffic = "AEO failing" | Dark social AI (WhatsApp, Copilot, private ChatGPT) has no traffic trace. Use SOV + branded search |

---

## Read the Full User Guide

**→ [USAGE_GUIDE.md](./USAGE_GUIDE.md)** — complete walkthroughs, all 5 client scenarios fully expanded, every mode with exact inputs + sample outputs, team roles, Python API examples, 20+ FAQs.

---

## License & Contributing

MIT license. PRs welcome for new industries, markets, updated regulatory info, and eval cases.  
Use `_ADD_NEW_INDUSTRY.md` / `_ADD_NEW_MARKET.md` templates.

---

## Author

**Indranil "Neel" Banerjee** — Head of AI Transformation, INT TechShu Digital  
[LinkedIn](https://linkedin.com/in/indranilbanerjee) · [GitHub](https://github.com/indranilbanerjee) · [NeelVerse](https://indranil.in)
