# AEO Strategist — Claude Cowork Skill

> **Enterprise Answer Engine Optimization (AEO) for Claude.**  
> A production-grade skill for SEO/AEO practitioners managing retainer clients across industries and global markets.

Built by **[Indranil "Neel" Banerjee](https://linkedin.com/in/indranilbanerjee)** — Head of AI Transformation, INT TechShu Digital.

---

## What This Skill Does

AEO (Answer Engine Optimization) is the practice of ensuring AI systems — ChatGPT, Gemini, Perplexity, Claude, Copilot — accurately and positively cite your brand in their responses.

This skill turns Claude into a fully-equipped AEO strategist capable of:

| Mode | What It Produces |
|------|-----------------|
| `/audit` | Full 5-category AEO readiness audit with P1/P2/P3 gap list |
| `/strategy` | Layer A (parametric, 12–24mo) + Layer B (RAG, immediate) strategy |
| `/roadmap` | Week-by-week 20-week implementation plan |
| `/brief` | 8-element AEO-optimized content brief ready for writers |
| `/rewrite` | Restructure existing content for AI extraction |
| `/schema` | Valid JSON-LD with stacked types + entity linking |
| `/llms-txt` | Brand's llms.txt file under 500 words |
| `/query-library` | 30+ tracked queries across 3 intent tiers |
| `/canonical` | Canonical brand description for cross-platform deployment |
| `/competitor` | 5-signal competitive footprint map + displacement plan |
| `/report` | Monthly AEO performance report for clients |
| `/onboard` | New client intake — full 7-section checklist workflow |
| `/track` | GA4 setup, SOV baseline, manual query testing protocol |
| `/pr-brief` | PR outreach plan targeting AI-licensed publications |
| `/research` | Live web intelligence — what AI says about a brand right now |
| `/explainer` | AEO business case for CMO/CEO — no jargon |

---

## Coverage

### 12 Industry Verticals
Each with deep trust signal hierarchies, compliance constraints by market, full query taxonomy, schema types, and India-specific signals.

| Vertical | Key Compliance |
|----------|---------------|
| 💊 Pharma & Life Sciences | CDSCO, FDA, EMA, ABPI — medico-legal gate required |
| 🏦 BFSI | SEBI, RBI, IRDAI, FCA, SEC — investment advice rules |
| 🏥 Healthcare | NABH, NABL, NMC, JCI, CQC |
| 🏠 Real Estate | RERA (state-wise), PCPNDT, Consumer Protection Act |
| 🎓 EdTech | UGC, AICTE, NAAC, FTC (US) |
| ⚖️ Legal & Professional Services | Bar Council, ICAI, SRA |
| 🏭 Manufacturing | BIS, ISO 9001/14001, REACH, RoHS |
| 🏨 Hospitality & Travel | FSSAI, Ministry of Tourism, TripAdvisor signals |
| 🚗 Automotive | ARAI, BNCAP/NCAP, FAME II EV |
| 💻 SaaS & Tech | GDPR, DPDP Act 2023, SOC 2, ISO 27001 |
| 🛒 Retail & E-commerce | BIS mandatory, FSSAI, Legal Metrology Act |
| 📰 Media & Publishing | AI licensing deals, DAVP, Press Council |

### 8 Regional Markets
Deep files with AI platform landscape, AI-citation-worthy publications, directories by vertical, and regulatory anchors.

| Market | Coverage |
|--------|---------|
| 🇮🇳 India | All 8 regions, 20+ regulatory bodies, vernacular opportunity guide |
| 🇺🇸 United States | Reddit strategy, AI Overviews, all major verticals |
| 🇬🇧 United Kingdom | FCA, CQC, Companies House, post-Brexit notes |
| 🇦🇪 UAE / MENA | Dubai, Saudi Arabia, Qatar, Arabic AEO opportunity |
| 🌏 Southeast Asia | Singapore, Indonesia, Malaysia, Philippines, Thailand, Vietnam |
| 🇪🇺 Europe | Germany, France, Netherlands, EU AI Act compliance |
| 🇦🇺 Australia & NZ | TGA, ASIC, ABN trust signals |
| 🌍 Africa | Nigeria, South Africa, Kenya, WhatsApp AI note |

---

## Repository Structure

```
aeo-strategist/
├── SKILL.md                          ← Main routing brain (load this in Claude)
├── industries/
│   ├── pharma.md                     ← 8 sub-verticals, all market compliance
│   ├── bfsi.md                       ← Banking, insurance, MF, fintech
│   ├── healthcare.md                 ← Hospitals, diagnostics, healthtech
│   ├── real-estate.md                ← RERA-first, hyperlocal, vernacular
│   ├── saas-tech.md                  ← G2, Gartner, SOC 2, DPDP
│   ├── retail-ecommerce.md           ← D2C, FMCG, BIS, Google Shopping
│   ├── edtech.md                     ← Test prep, upskilling, universities
│   ├── legal-professional.md         ← Law firms, CA firms, consulting
│   ├── manufacturing.md              ← ISO, BIS, export credentials
│   ├── hospitality-travel.md         ← Hotels, OTAs, F&B, MICE
│   ├── automotive.md                 ← ARAI, BNCAP, EV, dealerships
│   ├── media-publishing.md           ← AI licensing, DAVP, creator economy
│   └── _ADD_NEW_INDUSTRY.md          ← Template to extend the skill
├── markets/
│   ├── india.md                      ← Deepest file — tier-2/3, vernacular guide
│   ├── us.md                         ← Reddit strategy, AI Overviews, all verticals
│   ├── uk.md                         ← FCA, CQC, Companies House
│   ├── uae-mena.md                   ← Dubai, KSA, Arabic AEO
│   ├── sea.md                        ← SG, ID, MY, PH, TH, VN
│   ├── europe.md                     ← DACH, France, EU AI Act
│   ├── australia-nz.md               ← TGA, ASIC, ABN signals
│   ├── africa.md                     ← NG, ZA, KE — WhatsApp AI note
│   └── _ADD_NEW_MARKET.md            ← Template to extend the skill
├── references/
│   ├── eval-criteria.md              ← Quality gates per mode
│   ├── platform-matrix.md            ← All AI platforms: crawlers, source prefs, checklists
│   ├── query-taxonomy.md             ← Intent proximity framework + generation rules
│   ├── tracking-protocols.md         ← 6-layer measurement: SOV, GA4, dark social
│   ├── onboarding-checklist.md       ← 7-section new client intake SOP
│   ├── monthly-workflow.md           ← Week-by-week retainer delivery rhythm
│   ├── pr-targets.md                 ← AI-licensed pubs by tier and market
│   ├── glossary.md                   ← 50+ terms — for team training
│   ├── troubleshooting.md            ← 8 common failure patterns + fixes
│   └── regional-markets.md           ← Legacy reference (superseded by markets/)
└── evals/
    └── evals.json                    ← Test cases for skill evaluation
```

---

## Installation

### Option 1 — Claude Cowork (Recommended)

If you use [Claude Cowork](https://claude.ai) with the skills system:

1. Download the `.skill` file from [Releases](../../releases)
2. Drop it into your Cowork skills folder
3. Claude will auto-detect and load it

### Option 2 — Manual (Claude.ai or API)

1. Clone this repo:
   ```bash
   git clone https://github.com/indranil21/aeo-strategist-claude-skill.git
   ```

2. Start a Claude session. Paste the contents of `SKILL.md` as your system prompt, or reference it at the top of your conversation.

3. Load relevant industry and market files as context when needed:
   ```
   "Load industries/pharma.md and markets/india.md for this client."
   ```

### Option 3 — API / Code Integration

Use the files as a structured prompt system in your own application:

```python
import anthropic

# Load skill files
with open("SKILL.md") as f:
    skill_prompt = f.read()

with open("industries/pharma.md") as f:
    industry_context = f.read()

with open("markets/india.md") as f:
    market_context = f.read()

client = anthropic.Anthropic()

response = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=4096,
    system=f"{skill_prompt}\n\n---\n\n{industry_context}\n\n---\n\n{market_context}",
    messages=[{
        "role": "user",
        "content": "/audit Client: Cipla | Vertical: Pharma | Market: India | Competitive Position: Established"
    }]
)

print(response.content[0].text)
```

### Option 4 — MCP Server Integration

For teams running Claude via MCP (Model Context Protocol), you can serve these files as context resources from your MCP server and reference them in tool responses.

---

## Usage Examples

### Run an AEO Audit
```
/audit
Client: HDFC Bank
Vertical: BFSI (Retail Banking)
Market: India
Competitive Position: Market Leader
Current AEO Maturity: Zero
Target Platforms: All
```

### Generate a Content Brief
```
/brief
Client: Cipla
Topic: What is the treatment for asthma in adults?
Target: HCP-facing, India market
Compliance: CDSCO — disease-state content only, no brand promotion
```

### Build Schema Markup
```
/schema
Client: Prestige Group
Page type: Residential project page
RERA: PRM/KA/RERA/1251/309/PR/171223/006267
Location: Whitefield, Bangalore
```

### Run Competitive Intelligence
```
/competitor
Client: Zoho CRM
Competitor: Salesforce
Market: India, Mid-market B2B
```

### Onboard a New Client
```
/onboard
New client: [client name and industry]
```

---

## Extending the Skill

### Add a New Industry
1. Copy `industries/_ADD_NEW_INDUSTRY.md`
2. Rename to `industries/[your-industry].md`
3. Fill all 8 sections following the template
4. Add the industry name to `SKILL.md` description field and client intake options
5. Add 2 eval cases to `evals/evals.json`
6. Submit a PR — contributions welcome

### Add a New Market
1. Copy `markets/_ADD_NEW_MARKET.md`
2. Rename to `markets/[your-market].md`
3. Fill all 6 sections
4. Update `SKILL.md` description and intake options
5. Submit a PR

---

## Compliance Notice

This skill contains compliance guidance for regulated industries (Pharma, BFSI, Healthcare, Real Estate, Legal). This guidance is for AEO content strategy purposes only and does not constitute legal, medical, financial, or regulatory advice. Always pass content for regulated industries through your client's compliance/medico-legal review before publication.

---

## Contributing

PRs welcome for:
- New industry vertical files
- New market files
- Additional eval test cases
- Updated regulatory information
- Platform matrix updates as AI landscape evolves

Please follow the templates in `_ADD_NEW_INDUSTRY.md` and `_ADD_NEW_MARKET.md`.

---

## License

MIT License — free to use, modify, and distribute. Attribution appreciated.

---

## Author

**Indranil "Neel" Banerjee**  
Head of AI Transformation — INT TechShu Digital  
Building AI-powered systems for enterprise digital marketing.

- LinkedIn: [linkedin.com/in/indranilbanerjee](https://linkedin.com/in/indranilbanerjee)  
- GitHub: [@indranil21](https://github.com/indranil21)

---

*Built as part of the [NeelVerse](https://indranil.in) ecosystem.*
