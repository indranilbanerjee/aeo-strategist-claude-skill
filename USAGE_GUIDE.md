# AEO Strategist — Complete User Guide
## How to use every mode, with real client scenarios and step-by-step walkthroughs

---

## Table of Contents

1. [What is This Skill and Why You Need It](#1-what-is-this-skill-and-why-you-need-it)
2. [How to Load and Start the Skill](#2-how-to-load-and-start-the-skill)
3. [The 16 Modes — Quick Reference](#3-the-16-modes--quick-reference)
4. [Real-World Scenario: Pharma Client (India)](#4-real-world-scenario-pharma-client-india)
5. [Real-World Scenario: BFSI — Fintech Startup](#5-real-world-scenario-bfsi--fintech-startup)
6. [Real-World Scenario: Real Estate Developer (Kolkata)](#6-real-world-scenario-real-estate-developer-kolkata)
7. [Real-World Scenario: B2B SaaS — US Market](#7-real-world-scenario-b2b-saas--us-market)
8. [Real-World Scenario: Healthcare Chain (India)](#8-real-world-scenario-healthcare-chain-india)
9. [Mode Deep-Dives — What to Type, What You Get](#9-mode-deep-dives--what-to-type-what-you-get)
10. [The Monthly Retainer Workflow](#10-the-monthly-retainer-workflow)
11. [Team Training: Who Does What](#11-team-training-who-does-what)
12. [Common Mistakes to Avoid](#12-common-mistakes-to-avoid)
13. [Using the Skill via API / Code](#13-using-the-skill-via-api--code)
14. [FAQ](#14-faq)

---

## 1. What is This Skill and Why You Need It

### The Problem It Solves

Your clients pay you for SEO. But in 2025, 30–50% of informational queries never reach a website anymore — they get answered directly by ChatGPT, Gemini, or Perplexity. If your client's brand isn't being cited in those AI answers, they're invisible to a growing chunk of their audience.

AEO (Answer Engine Optimization) is how you fix that. But doing it properly requires:
- Knowing which trust signals each AI platform actually uses (different for each)
- Understanding 12 different industry compliance frameworks
- Building measurement systems for something with no equivalent of Search Console
- Producing structured content, schema markup, llms.txt files, query libraries
- Managing all of this across multiple retainer clients simultaneously

This skill is the complete operating system for doing all of that inside Claude — fast, at client-ready quality, with compliance awareness built in.

### What "Skill" Means

A Claude Cowork skill is a structured prompt system loaded into Claude's context. Once loaded, Claude behaves like a specialist — it knows the frameworks, terminology, compliance constraints, platform behaviors, and output formats without you having to explain them every time.

Think of it like hiring an expert consultant who has already read every brief, knows every client type, and just needs to know which client and which task you're working on right now.

---

## 2. How to Load and Start the Skill

### Method A — Claude Cowork (Recommended for Teams)

1. Install the `.skill` file from the [Releases page](../../releases) into your Cowork skills folder
2. Open a new Claude Cowork session
3. The skill auto-loads. Start with:

```
/onboard
New client: [Client Name]
Industry: [Vertical]
Market: [Region]
```

That's it. Claude will run through the full intake and tell you what it needs.

### Method B — Claude.ai (Free / Pro / Team)

1. Open claude.ai
2. Start a new conversation
3. Paste the full contents of `SKILL.md` as your first message, then follow with:

```
I've loaded the AEO Strategist skill. 

Client context:
- Client: Cipla Limited
- Industry: Pharma
- Market: India
- Business model: B2C (OTC) + B2B (prescription channel)
- Competitive position: Established market leader
- AEO maturity: Zero — never worked on this before
```

4. Claude will confirm it has loaded the context and ask what mode to run.

### Method C — Via API (Developers / Integration)

See [Section 13](#13-using-the-skill-via-api--code) for full code examples.

### First Thing to Always Do: Give Client Context

The skill works best when it knows exactly who the client is. Before running any mode, set context with these 7 fields:

```
Client: [Brand name]
Industry: [Vertical from the list]
Market: [Region]
Business model: B2B / B2C / Both
Competitive position: New entrant / Established / Defending leader
AEO maturity: Zero / Partial / Advanced
Primary goal this session: [what you want to produce today]
```

You only need to set this once per session. Claude carries it forward.

---

## 3. The 16 Modes — Quick Reference

| # | Mode | Type | Time to Run | Best Used When |
|---|------|------|------------|----------------|
| 1 | `/audit` | Strategy | 5–10 min | Starting a new client / quarterly review |
| 2 | `/strategy` | Strategy | 10–15 min | After audit, building the full plan |
| 3 | `/roadmap` | Strategy | 5–8 min | After strategy, scheduling execution |
| 4 | `/onboard` | Strategy | 10–15 min | First week with any new retainer client |
| 5 | `/competitor` | Strategy | 5–8 min | Anytime client asks "why is X appearing not us" |
| 6 | `/report` | Strategy | 5–8 min | Monthly — before client call |
| 7 | `/explainer` | Strategy | 3–5 min | CMO / CEO doesn't understand AEO yet |
| 8 | `/brief` | Production | 5–8 min | Before each new content piece |
| 9 | `/rewrite` | Production | 5–8 min | Optimizing existing pages |
| 10 | `/schema` | Production | 3–5 min | Any new page type or schema update |
| 11 | `/llms-txt` | Production | 3–5 min | First month setup for any client |
| 12 | `/query-library` | Production | 5–8 min | Setting up tracking baseline |
| 13 | `/canonical` | Production | 2–3 min | Entity consolidation work |
| 14 | `/track` | Operations | 5–8 min | Setting up measurement for new client |
| 15 | `/pr-brief` | Operations | 5–8 min | Monthly PR outreach planning |
| 16 | `/research` | Live Intel | 2–5 min | Quick check of what AI says about anyone |

---

## 4. Real-World Scenario: Pharma Client (India)

### Client Profile
**Mankind Pharma** — Indian pharma company, OTC consumer health + prescription portfolio.  
Market: India | AEO Maturity: Zero | Goal: Appear in AI answers for OTC health queries.

---

### Step 1 — Onboard the Client (`/onboard`)

On Day 1, before anything else:

```
/onboard
Client: Mankind Pharma
Industry: Pharma
Market: India
Business model: B2C (OTC) + B2B (prescription channel to HCPs)
Sub-verticals: OTC consumer health, branded generics, reproductive health
Website: mankind.in
```

**What Claude produces:**
- Full 7-section intake checklist pre-filled with what you know
- Gap list: what information is still needed (CDSCO licence numbers, robots.txt access, GSC data)
- First-month priorities: robots.txt fix (CCBot likely blocked), Wikidata entry, FSSAI-compliant disease-state content
- Week 1 deliverables schedule

---

### Step 2 — Run the Audit (`/audit`)

```
/audit
Client: Mankind Pharma
Vertical: Pharma (OTC + branded generics)
Market: India
Competitive position: Established (strong in tier-2/3 cities)
Key competitor: Cipla, Sun Pharma for OTC; Himalaya for wellness
Current AEO maturity: Zero
Note: Website is built on React (SPA) — need to check SSR status
```

**What Claude produces:**

```
MANKIND PHARMA — AEO Readiness Audit
Pharma (OTC + Generics) | India | Established | [Date]

AI Visibility Snapshot
Gemini: "Mankind Pharma is an Indian pharmaceutical company known for 
affordable generic medicines." — Partial. Correct category, missing OTC 
brand strengths, no product-category association.
ChatGPT: Not mentioned in most OTC health queries. Cipla and Himalaya 
dominate consumer health answers.
Perplexity: Not cited. No earned media in last 6 months indexed.

Category 1: Technical Crawlability
| Signal              | Status  | Priority Action                          |
| CCBot in robots.txt | BLOCKED | Allow immediately — removes from training |
| React SPA / SSR     | NO SSR  | Migrate to Next.js SSR — 6-8 week project|
| Bing WMT verified   | NO      | Verify today — free, 1 hour              |
...

⚠️ COMPLIANCE SECTION
CDSCO constraint: Prescription drug (Schedule H) content — NEVER 
make efficacy or superiority claims. All OTC content requires 
standard disclaimer. Medico-legal review required before any 
content goes live.
...

PRIORITY GAP LIST
| Gap                      | Priority | Effort | Impact |
| CCBot blocked            | P1       | Low    | High   |
| No Wikidata entry        | P1       | Low    | High   |
| React SPA — no SSR       | P1       | High   | High   |
| No disease-state content | P2       | Medium | High   |
...
```

---

### Step 3 — Build the Strategy (`/strategy`)

```
/strategy
[Context already set from audit above]
Focus: OTC consumer health queries, India, Gemini + ChatGPT priority
Timeline: 12-month plan
```

**What Claude produces:** Full Layer A + Layer B strategy:
- Layer B (immediate): Fix crawlers, restructure existing OTC product pages with answer-first format, add FAQ sections, schema markup for OTC products, Practo/1mg directory completion
- Layer A (12–24 months): Disease-state content program (safe zone — asthma, diabetes, pain management), earned media in ET Healthworld + Express Pharma, Wikidata entity build, IMA/IDMA association mentions

---

### Step 4 — Generate a Content Brief (`/brief`)

For the first content piece:

```
/brief
Client: Mankind Pharma
Topic: What is the best OTC treatment for mild fever in adults?
Target audience: General consumer (not HCP)
Market: India
Compliance: CDSCO — OTC content only, disease-state awareness, no 
prescription drug promotion, include standard disclaimer
Target platforms: Gemini (primary), ChatGPT
```

**What Claude produces:** Full 8-element brief including:
- Answer-first opener (exact sentences ready for the writer)
- 6 FAQ pairs at 40–60 words each
- 3 grounding hooks (stats from ICMR, WHO references, CDSCO-compliant claims)
- Schema recommendation: MedicalWebPage + FAQPage + Drug (paracetamol OTC)
- ⚠️ Red flag: "Do not reference any prescription fever medication. Confirm writer has medico-legal clearance."

---

### Step 5 — Build Schema for the Product Page (`/schema`)

```
/schema
Client: Mankind Pharma
Page: Meftal Spas product page (OTC antispasmodic)
CDSCO status: OTC (Schedule K)
Target: Disease-state awareness page, not promotional
```

**What Claude produces:** Valid JSON-LD ready to paste into the page's `<head>`.

---

### Step 6 — Set Up Tracking (`/track`)

```
/track
Client: Mankind Pharma
Platforms: Gemini, ChatGPT, Perplexity
Query set: [from /query-library output — 20 queries]
GA4 access: Yes
```

**What Claude produces:** Complete tracking setup document — GA4 custom channel group configuration with exact steps, manual query testing schedule, SOV baseline template, attribution log.

---

### Month 2 Onwards — The Rhythm

Every month:
- Week 1: Run SOV snapshot (`/query-library` queries tested manually)
- Week 2: Produce 2 new content pieces (from `/brief`)
- Week 3: PR outreach (`/pr-brief`)
- Week 4: Write client report (`/report`) + plan next month

---

## 5. Real-World Scenario: BFSI — Fintech Startup

### Client Profile
**Fibe (formerly EarlySalary)** — Indian fintech, instant personal loans for salaried professionals.  
Market: India | AEO Maturity: Zero | Goal: Appear when someone asks AI for instant loan options.

---

### The Specific Problem

User query: *"Best instant personal loan app India for salaried employee"*  
AI response (before AEO work): "CASHe, MoneyTap, and PaySense are popular options for instant personal loans..."  
Fibe is not mentioned despite being a market leader.

---

### Step 1 — Quick Competitive Intel (`/research`)

```
/research
Brand: Fibe (EarlySalary)
Category: Instant personal loan India
Competitors to check: CASHe, MoneyTap, KreditBee
```

**What Claude does:** Runs live web searches to check:
- What Perplexity says when asked about instant loans India
- Which sources Perplexity is citing (likely BankBazaar, ET, Moneycontrol articles)
- Whether Fibe appears on any comparison platforms

**Output:** "CASHe appears in 4 of 5 test queries via BankBazaar and Moneycontrol listicle citations. Fibe appears in 1 of 5 — via an old YourStory article from 2022. Primary gap: no recent earned media in AI-licensed publications. BankBazaar listing is incomplete."

---

### Step 2 — Competitor Analysis (`/competitor`)

```
/competitor
Client: Fibe (EarlySalary)
Competitor: CASHe
Market: India
Vertical: BFSI — Fintech lending
```

**Output includes:**
```
COMPETITIVE FOOTPRINT MAP: CASHe vs Fibe

Signal 1 — Technical: Both equal. Both indexed, both have basic schema.
Signal 2 — Content extraction: CASHe WINS. Their blog has 14 answer-first 
  articles on personal loan topics. Fibe has 3, none structured for AI.
Signal 3 — Entity authority: CASHe WINS. Wikidata entry exists (Fibe: none).
  Wikipedia redirect exists. Wikidata QID: Q116486229.
Signal 4 — Earned media: EQUAL. Both have Moneycontrol + ET coverage.
Signal 5 — Directory/reviews: CASHe WINS. BankBazaar profile 100% complete. 
  Fibe profile missing EMI calculator, recent reviews sparse.

Fastest displacement path:
1. Create Wikidata entry for Fibe (2–4 hours, immediate entity anchoring)
2. Publish 8 answer-first personal loan articles (4–6 weeks)
3. Complete BankBazaar profile + drive 50 new reviews (4 weeks)
→ Expect Perplexity citation within 6–8 weeks. ChatGPT parametric: 12+ months.
```

---

### Step 3 — Content Brief for the Critical Query (`/brief`)

```
/brief
Client: Fibe
Topic: Instant personal loan for salaried employees — how to get approved fast
Target: Decision-stage consumer, India
Compliance: RBI digital lending guidelines Sept 2022, no guaranteed approval 
claims, include "subject to eligibility" disclaimer
Target platform: Gemini + ChatGPT (Bing-grounded mode)
```

---

### Step 4 — Canonical Description (`/canonical`)

```
/canonical
Client: Fibe (formerly EarlySalary)
Category: Instant personal loan app for salaried professionals
Key facts: RBI-registered NBFC, 35L+ loans disbursed, avg disbursal 
in 8 minutes, credit limit up to ₹5 lakh
```

**Output:**
```
CANONICAL DESCRIPTION (2–3 sentences):
Fibe, formerly EarlySalary, is an RBI-registered NBFC offering instant 
personal loans of up to ₹5 lakh to salaried professionals, with average 
disbursal in under 8 minutes. Founded in 2015 and headquartered in Pune, 
Fibe has disbursed over 35 lakh loans across India with a fully digital 
application process.

ULTRA-SHORT (1 sentence):
Fibe is an RBI-registered Indian fintech providing instant personal loans 
to salaried employees with sub-10-minute disbursal.

CATEGORY STATEMENT:
instant personal loan app | NBFC India | digital lending

sameAs targets:
- https://www.wikidata.org/wiki/Q[create entry]
- https://www.linkedin.com/company/fibe-india
- https://www.bankbazaar.com/personal-loan/early-salary.html
- https://www.crunchbase.com/organization/earlysalary
```

**This canonical goes onto:** Website About page, Wikidata description, LinkedIn company summary, all directory profiles — identical wording everywhere.

---

## 6. Real-World Scenario: Real Estate Developer (Kolkata)

### Client Profile
**Ambuja Neotia Group** — Premium real estate developer, Kolkata-based, residential + hospitality.  
Market: India (West Bengal) | AEO Maturity: Partial | Goal: Dominate Kolkata luxury apartment queries on Gemini.

---

### The Hyperlocal Priority

Real estate AEO is not national — it is always city-first, locality-second. Queries like "luxury apartments Kolkata" and "new projects Rajarhat New Town 2025" are where this client wins or loses.

---

### Step 1 — Audit Focused on Hyperlocal (`/audit`)

```
/audit
Client: Ambuja Neotia Group
Vertical: Real Estate (residential — premium/luxury)
Market: India (Kolkata, West Bengal)
RERA: WB/HIRA registered
Competitive position: Established (top 3 Kolkata developer)
Competitor: Merlin Group, PS Group
Note: Heavy Google Ads spend — need to distinguish AEO from paid
```

**Key findings Claude will flag:**
- HIRA registration status and project numbers (West Bengal uses HIRA not RERA — must check)
- Google Business Profile completeness for each project site office
- MagicBricks/99Acres listing completeness per project
- Bengali language content gap (huge opportunity — Kolkata real estate queries in Bengali almost zero competition)

---

### Step 2 — Bengali Language Strategy (within `/strategy`)

```
/strategy
[Context from above]
Special requirement: Include vernacular Bengali AEO track
Bengali queries to target: "Kolkata te flat kinte chai", "Rajarhat e noya project"
```

**Claude will produce** a parallel strategy track:
- Bengali content targets (Anandabazar Patrika, Bartaman coverage for earned media)
- Bengali FAQ pages on key project sites
- Bengali Schema markup consideration
- Note: "Google Gemini supports Bengali AI Overviews — this is a first-mover opportunity in WB real estate"

---

### Step 3 — Schema for a Project Page (`/schema`)

```
/schema
Client: Ambuja Neotia
Page type: Residential project page — "The Condor" luxury apartments
Location: Action Area II, Rajarhat New Town, Kolkata
HIRA number: HIRA/P/NOR/2023/000XXX
Status: Under construction, possession Dec 2026
Price range: ₹1.8 Cr to ₹3.5 Cr
Units: 180 apartments, 3BHK and 4BHK
Amenities: Rooftop pool, clubhouse, 24hr security, EV charging
```

**Output:** Complete JSON-LD with:
- `Organization` + `Residence` + `LocalBusiness` stacked
- HIRA number embedded in `hasCredential` — critical trust signal
- `address` at locality level (Rajarhat, not just Kolkata)
- `amenityFeature` array with all amenities
- `numberOfRooms` and `floorSize` ranges
- Compliance note: "Do not include possession date as `datePublished` — use `description` field with 'expected' qualifier pending HIRA schedule confirmation"

---

### Step 4 — Query Library for Hyperlocal Tracking (`/query-library`)

```
/query-library
Client: Ambuja Neotia
Market: India (Kolkata focus)
Coverage: All Ambuja project localities (Rajarhat, EM Bypass, Lake Town, Howrah)
Include: Bengali language variants
```

**Output:** 35+ queries including:
```
Tier 1 — Decision:
- "Ambuja Neotia HIRA registered Kolkata" [Gemini, ChatGPT]
- "The Condor Rajarhat possession date" [Gemini]
- "Ambuja Neotia reviews Kolkata 2025" [All platforms]
- "luxury apartments Rajarhat New Town price" [Gemini]

Bengali variants:
- "রাজারহাটে ফ্ল্যাট কিনতে চাই" (Want to buy flat in Rajarhat) [Gemini]
- "আম্বুজা নিওটিয়া প্রকল্প" (Ambuja Neotia project) [Gemini]

Tier 2 — Comparison:
- "Ambuja Neotia vs Merlin Group Kolkata quality" [All]
- "best luxury developer Kolkata 2025" [All]
```

---

## 7. Real-World Scenario: B2B SaaS — US Market

### Client Profile
**Leena AI** — HR automation SaaS, employee helpdesk and onboarding automation.  
Market: US + India | B2B | AEO Maturity: Partial | Goal: Appear in "best HR automation software" AI answers.

---

### The B2B SaaS AEO Challenge

For B2B SaaS, the trust signal that matters most is **G2 category position**. If you're not on G2's Leader or High Performer list for your category, AI systems largely treat you as unverified. That's the anchor to fix first.

---

### Step 1 — Research First (`/research`)

```
/research
Brand: Leena AI
Category: HR automation software, employee helpdesk
Competitor: ServiceNow, Moveworks, Freshservice
Market: US
```

**What Claude searches for and reports:**
- Current Perplexity response to "best HR automation software 2025"
- Whether Leena AI appears, and if so with which source citation
- Gartner/G2 positioning visible in search results
- Competitor strongest anchor (likely ServiceNow's Gartner MQ position)

---

### Step 2 — Audit (`/audit`)

```
/audit
Client: Leena AI
Vertical: SaaS-Tech (HR automation, enterprise)
Market: US (primary) + India (secondary)
Business model: B2B, mid-market to enterprise
Competitive position: Challenger (growing vs ServiceNow, Moveworks)
Current AEO maturity: Partial — some schema, active blog
Note: SOC 2 Type II certified, ISO 27001, GDPR compliant
```

**Key audit findings to expect:**
- G2 profile completeness and category placement (critical signal for SaaS)
- Technical documentation depth (docs.leena.ai — is it indexed and AI-readable?)
- Case study specificity ("40% reduction in HR ticket resolution time at [Named Company]" vs vague claims)
- Integration directory presence (ServiceNow marketplace, Slack directory, Microsoft Teams)
- Reddit presence on r/humanresources, r/sysadmin

---

### Step 3 — Content Brief for High-Value Query (`/brief`)

```
/brief
Client: Leena AI
Topic: How to automate HR onboarding for enterprise companies
Target: CHRO / VP HR at 1000+ employee companies, US market
Compliance: GDPR mention for EU-HQ companies, SOC 2 compliance claim 
must reference audit date
Tone: Practitioner, not vendor-pitch
Target platform: Perplexity (primary for B2B research), ChatGPT
```

---

### Step 4 — CMO Explainer (`/explainer`)

The CHRO sponsor gets it, but the CEO is asking "why are we spending budget on this":

```
/explainer
Audience: CEO, non-technical, US SaaS company
Context: Justifying AEO retainer investment to board
Competitive risk: ServiceNow and Moveworks already appear in HR 
automation AI answers. Leena AI does not.
Investment being justified: ₹[X]L/month retainer
```

**Output:** Business case in plain English — no AEO jargon, one strong analogy ("like being invisible in Google in 2010"), specific competitive risk framing, honest timeline (parametric 12–18 months, RAG results in 4–8 weeks), and a cost-of-inaction argument.

---

### Step 5 — PR Brief for US Market (`/pr-brief`)

```
/pr-brief
Client: Leena AI
Market: US
Vertical: HR Tech / B2B SaaS
Current coverage: YourStory (India), Inc42 — no US coverage yet
Goal: Break into TechCrunch, VentureBeat, HR Executive tier
Angle: Proprietary data — "State of HR Automation in Enterprise 2025" report
```

**Output:** Prioritised publication list, angle per publication, journalist section identification, pitch template ready to adapt.

---

## 8. Real-World Scenario: Healthcare Chain (India)

### Client Profile
**Manipal Hospitals** — Multi-specialty hospital chain, NABH accredited, 30+ hospitals pan-India.  
Market: India | AEO Maturity: Zero | Goal: Appear in "best hospital for cardiac surgery" type queries.

---

### The Healthcare AEO Complexity

Healthcare has the highest stakes for AEO inaccuracy. AI systems apply "Your Money or Your Life" (YMYL) scoring to healthcare content — meaning they're extremely selective about what they cite. Only NABH-accredited, clinician-attributed, outcomes-backed content gets cited consistently.

---

### Step 1 — Audit (`/audit`)

```
/audit
Client: Manipal Hospitals
Vertical: Healthcare (multi-specialty hospital chain)
Market: India (Bangalore HQ, pan-India)
Accreditations: NABH, JCI (select hospitals), NABL (labs)
CGHS empanelled: Yes
Competitive position: Top 3 India (vs Apollo, Fortis, Max)
Note: Strong doctor brand (Dr. Shetty, Manipal foundation legacy)
```

---

### Step 2 — Doctor Profile Schema (`/schema`)

Individual doctor credibility is the #1 trust signal for healthcare AEO:

```
/schema
Client: Manipal Hospitals
Page type: Physician profile page
Doctor: Dr. Ramesh Babu — Senior Interventional Cardiologist
Qualifications: MBBS (Manipal), MD Cardiology (AIIMS Delhi), 
  DM Cardiology, Fellowship at Cleveland Clinic
NMC Registration: Karnataka Medical Council #XXXXX
Experience: 22 years, 5000+ cardiac procedures
Hospital: Manipal Hospital, Old Airport Road, Bangalore
```

**Output:**
```json
{
  "@context": "https://schema.org",
  "@type": ["Physician", "Person"],
  "name": "Dr. Ramesh Babu",
  "jobTitle": "Senior Interventional Cardiologist",
  "worksFor": {
    "@type": "Hospital",
    "name": "Manipal Hospitals",
    "hasCredential": {
      "@type": "EducationalOccupationalCredential",
      "credentialCategory": "NABH Accreditation"
    }
  },
  "hasCredential": [
    {"@type": "EducationalOccupationalCredential", "credentialCategory": "MBBS"},
    {"@type": "EducationalOccupationalCredential", "credentialCategory": "DM Cardiology, AIIMS Delhi"},
    {"@type": "EducationalOccupationalCredential", 
     "name": "NMC Registration", "identifier": "KMC-XXXXX"}
  ],
  "medicalSpecialty": "Cardiology",
  "knowsAbout": ["Interventional Cardiology", "Angioplasty", "TAVI", "Heart Failure"],
  "sameAs": [
    "https://www.practo.com/bangalore/doctor/dr-ramesh-babu-cardiologist",
    "https://manipalhospitals.com/doctors/dr-ramesh-babu"
  ]
}
```

---

### Step 3 — Content Brief for High-Stakes Query (`/brief`)

```
/brief
Client: Manipal Hospitals
Topic: What are the signs you need bypass surgery and how to choose a hospital?
Audience: Patient / family making a high-stakes decision
Compliance: NMC advertising guidelines — informational only, no 
"best hospital" self-claim, outcomes data must be sourced
Required grounding: Named cardiologist quote, NABH accreditation reference, 
published survival rate data
Target: Gemini (Google Health integration), ChatGPT
```

---

## 9. Mode Deep-Dives — What to Type, What You Get

### `/audit` — The Starting Point for Every Client

**When to use:** Start of retainer, quarterly review, anytime the client says "why aren't we in AI answers."

**Minimum input needed:**
```
/audit
Client: [Name]
Vertical: [Industry]
Market: [Region]
Competitive position: [New / Established / Leader]
```

**What you get:** 5-category assessment (Technical, Content, Entity & Authority, Parametric Gap, Competitive), priority gap list with effort/impact matrix, compliance section, 3 quick wins.

**Pro tip:** Share the robots.txt URL and top 5 competitor names for a more specific audit.

---

### `/research` — Live Intelligence Before the Strategy

**When to use:** Before an audit, before a competitor briefing, when a client asks "what is AI saying about us right now."

**Input:**
```
/research
Brand: [Brand name]
Category: [What they do]
Check: [Specific platforms or competitors to investigate]
```

**What you get:** Live web search findings — what AI platforms are currently saying, which sources are being cited, competitor comparison, immediate recommended action.

**Important caveat:** Claude will label these as live web signals, not guaranteed parametric state. Manual platform testing still needed for full SOV data.

---

### `/brief` — The Most Used Mode in Day-to-Day Work

**When to use:** Before every new content piece your team or client's writers produce.

**Minimum input:**
```
/brief
Client: [Name]
Topic: [Exact topic / question to answer]
Audience: [Who is reading]
Compliance: [Any constraints]
```

**Pro tip — give more for better output:**
```
/brief
Client: Mankind Pharma
Topic: What are safe pain relief options for diabetic patients in India?
Audience: General consumer (not HCP) — tier-2 city, semi-urban
Compliance: CDSCO OTC only, no prescription drug reference, 
  disclaimer required, no comparative drug claims
Existing content URL: mankind.in/blog/pain-management (for reference)
Target: Gemini primary, Perplexity secondary
Word count needed: 1200–1500 words
```

---

### `/schema` — Copy-Paste Ready JSON-LD

**When to use:** Any new page type, schema audit, page redesign.

**Always include:**
- Page type (what kind of page is it)
- Key facts (the specific details that go in the schema)
- Any compliance constraints (don't put price in schema if price changes daily)

**Common schema types by industry:**

| Industry | Primary Schema Types |
|----------|---------------------|
| Pharma | Organization, MedicalWebPage, Drug (OTC), FAQPage |
| BFSI | Organization, FinancialService, BankOrCreditUnion, FAQPage |
| Real Estate | Organization, Residence, LocalBusiness, AggregateRating |
| Healthcare | Hospital, Physician, MedicalClinic, MedicalProcedure |
| SaaS | SoftwareApplication, Organization, FAQPage, TechArticle |
| Retail | Product, Offer, AggregateRating, BreadcrumbList |
| Education | EducationalOrganization, Course, FAQPage |

---

### `/llms-txt` — Set Once, Maintain Quarterly

**When to use:** First month of any new client. Then review quarterly.

**Input:**
```
/llms-txt
Client: [Name]
Category: [What they do in plain language]
Audience: [Who they serve]
Key pages: [5–10 most important URLs]
Preferred description: [How they want to be described]
What they are NOT: [Common misconceptions to correct]
```

**What you get:** Complete `llms.txt` file, under 500 words, in the correct format, ready to place at `yourdomain.com/llms.txt`.

**Why it matters:** When AI systems crawl a website and find an `llms.txt` file, it functions as a direct brief to the model — "here's exactly what we are and how we want to be described." It's the closest thing to direct AEO control currently available.

---

### `/report` — Client-Ready Monthly Report

**When to use:** Week 4 of every month, before client call.

**Input:**
```
/report
Client: [Name]
Month: [Month Year]
SOV data: [Paste your SOV snapshot — queries, platforms, results]
GA4 AI traffic: [Sessions, engagement rate, conversions vs last month]
Brand search: [Impressions trend from GSC]
Actions taken this month: [List what was done]
Upcoming: [What's planned next month]
Stakeholder: [CMO / Marketing Head / CEO]
```

**Pro tip:** The more data you feed in, the less time you spend writing the report. Paste raw numbers — Claude formats them into an executive-ready document.

---

### `/explainer` — For Stakeholders Who Don't Get AEO Yet

**When to use:** First presentation to a new client, board-level budget justification, CMO who keeps asking "is this just SEO?"

**This mode deliberately:**
- Uses zero unexplained jargon
- Opens with competitive risk, not opportunity
- Uses one simple analogy
- Gives honest timelines (doesn't oversell)
- Ends with cost-of-inaction

---

## 10. The Monthly Retainer Workflow

This is the full operating rhythm for managing an AEO client month by month.

```
WEEK 1 — MEASURE
├── Day 1–2: Run SOV snapshot (20 queries × 3 platforms × 3 tests each)
├── Day 3: Pull GA4 AI referral channel data
├── Day 4: Check brand search volume in GSC
└── Day 5–7: Compile measurement summary

WEEK 2 — PRODUCE
├── Day 8–9: Write 2 new content pieces (use /brief for each)
├── Day 10: Validate any schema deployed last month
├── Day 11: Update incomplete directory listings
└── Day 12–14: Deploy technical fixes queued from audit

WEEK 3 — EARN
├── Day 15–17: Send 2–3 PR pitches (/pr-brief output)
├── Day 18–19: Community participation (Reddit / LinkedIn / Quora)
└── Day 20–21: Chase unlinked brand mentions

WEEK 4 — REPORT + PLAN
├── Day 22–24: Write monthly report (/report mode)
├── Day 25: Internal review before client delivery
├── Day 26–28: Client delivery + feedback call
└── Day 29–30: Queue next month (/brief for 2–3 new topics)
```

**Every 3 months:** Full `/audit` refresh, `/competitor` re-run, `/query-library` expansion (+10 new queries), strategy check.

---

## 11. Team Training: Who Does What

### Account Lead / Senior Strategist
Owns: `/onboard`, `/audit`, `/strategy`, `/roadmap`, `/competitor`, `/report`, `/explainer`  
Cadence: Monthly strategy review, quarterly full audit

### Content Team
Uses: `/brief`, `/rewrite`, `/canonical`  
Workflow: Receive brief → write to spec → return for compliance check → publish

### Technical Team
Uses: `/schema`, `/llms-txt`, `/track`  
Workflow: Receive schema output → implement in CMS → validate in Rich Results Test → log deployment date

### Junior Analyst
Owns: Monthly SOV snapshot testing, GA4 data pull, directory listing updates  
Uses: `/query-library` (run the tracking set), `/research` (quick brand intel)

### PR Team / Agency
Uses: `/pr-brief` output as briefing document  
Workflow: Receive PR brief → adapt pitches → outreach → report coverage back to account lead

---

## 12. Common Mistakes to Avoid

### Mistake 1: Running modes without setting client context first
**Problem:** Claude produces generic output without compliance awareness.  
**Fix:** Always set the 7-field client context before your first mode call in a session.

### Mistake 2: Skipping the compliance section in regulated industries
**Problem:** Content goes live with CDSCO/SEBI/NMC violations, creating legal risk.  
**Fix:** For Pharma, BFSI, Healthcare, Legal — read the compliance section of every output before passing to writers. The skill flags it; you enforce it.

### Mistake 3: Telling the client to expect results in 60 days
**Problem:** Parametric influence takes 12–18 months. Overpromising destroys client trust.  
**Fix:** Use `/explainer` mode to set correct expectations before signing the retainer. Be explicit: "RAG results in 4–8 weeks. Parametric influence 12–18+ months. Both are real."

### Mistake 4: Optimising for one platform only
**Problem:** ChatGPT uses Bing; Gemini uses Google; Claude uses Brave. Fixing one doesn't fix all.  
**Fix:** The `/audit` and `/strategy` modes always cover all relevant platforms. Don't skip the platform prioritization section.

### Mistake 5: Using the same canonical description across platforms — inconsistently
**Problem:** If LinkedIn says "AI-powered fintech" and Wikidata says "digital lending platform" and 1mg says "health and wellness brand," AI averages these into a confused entity.  
**Fix:** Run `/canonical` once, deploy that exact description everywhere. Review quarterly.

### Mistake 6: Forgetting that dark social AI is real
**Problem:** "Our GA4 shows zero AI traffic, so AEO isn't working."  
**Fix:** GA4 only captures AI referral clicks. WhatsApp AI, Copilot in Office, and private ChatGPT sessions generate brand influence with no observable traffic. SOV tracking and brand search volume are the right proxies. Explain this to every client early.

### Mistake 7: Blocking CCBot in robots.txt
**Problem:** Common Crawl (CCBot) is the primary source for LLM training data. Blocking it removes the brand from most AI models' parametric knowledge.  
**Fix:** Allow CCBot. Check every new client's robots.txt in Week 1 of onboarding. This is a P1 fix — 30 minutes, high impact.

---

## 13. Using the Skill via API / Code

### Basic Python Integration

```python
import anthropic
from pathlib import Path

def load_skill_files(base_path: str, industry: str, market: str) -> str:
    """Load the skill files needed for a specific client context."""
    base = Path(base_path)
    
    # Always load SKILL.md
    skill_md = (base / "SKILL.md").read_text()
    
    # Load industry-specific file
    industry_file = base / "industries" / f"{industry.lower().replace(' ', '-')}.md"
    industry_context = industry_file.read_text() if industry_file.exists() else ""
    
    # Load market-specific file  
    market_file = base / "markets" / f"{market.lower().replace(' ', '-')}.md"
    market_context = market_file.read_text() if market_file.exists() else ""
    
    return f"{skill_md}\n\n---\n\n{industry_context}\n\n---\n\n{market_context}"


client = anthropic.Anthropic()

# Build system prompt for Cipla (Pharma, India)
system_prompt = load_skill_files(
    base_path="./aeo-strategist",
    industry="pharma",
    market="india"
)

# Run an audit
response = client.messages.create(
    model="claude-opus-4-5",
    max_tokens=4096,
    system=system_prompt,
    messages=[{
        "role": "user",
        "content": """/audit
Client: Cipla Limited
Vertical: Pharma (OTC + branded generics + respiratory)
Market: India
Competitive position: Established market leader
Key competitor: Sun Pharma, Mankind Pharma
AEO maturity: Zero
Note: Heavy React SPA site — suspect no SSR"""
    }]
)

print(response.content[0].text)
```

---

### Generating a Content Brief Programmatically

```python
def generate_aeo_brief(client_name, topic, industry, market, compliance_notes=""):
    system_prompt = load_skill_files("./aeo-strategist", industry, market)
    
    prompt = f"""/brief
Client: {client_name}
Topic: {topic}
Market: {market}
Compliance: {compliance_notes if compliance_notes else "Standard industry guidelines"}
Target: All relevant platforms for this market and vertical"""

    response = client.messages.create(
        model="claude-opus-4-5",
        max_tokens=4096,
        system=system_prompt,
        messages=[{"role": "user", "content": prompt}]
    )
    
    return response.content[0].text


# Generate a brief for Manipal Hospitals
brief = generate_aeo_brief(
    client_name="Manipal Hospitals",
    topic="What to expect during cardiac bypass surgery recovery in India",
    industry="healthcare",
    market="india",
    compliance_notes="NMC guidelines — informational only, NABH accreditation reference required, named physician quote mandatory"
)
print(brief)
```

---

### Building a Schema Generator Tool

```python
def generate_schema(page_type, client_name, page_details, industry, market):
    system_prompt = load_skill_files("./aeo-strategist", industry, market)
    
    prompt = f"""/schema
Client: {client_name}
Page type: {page_type}
Details: {page_details}"""

    response = client.messages.create(
        model="claude-opus-4-5",
        max_tokens=2048,
        system=system_prompt,
        messages=[{"role": "user", "content": prompt}]
    )
    
    return response.content[0].text


# Generate schema for a Prestige Group project page
schema = generate_schema(
    page_type="Residential project page",
    client_name="Prestige Group",
    page_details="""
    Project: Prestige Lakeside Habitat
    Location: Whitefield, Bangalore
    RERA: PRM/KA/RERA/1251/309/PR/171223/006267
    Type: Luxury apartments 2BHK, 3BHK, 4BHK
    Price: ₹1.2 Cr to ₹4.8 Cr
    Status: Ready to move
    Rating: 4.2/5 based on 340 reviews
    """,
    industry="real-estate",
    market="india"
)
print(schema)
```

---

### Multi-Client Batch Processing

```python
clients = [
    {"name": "Cipla", "industry": "pharma", "market": "india"},
    {"name": "HDFC Bank", "industry": "bfsi", "market": "india"},
    {"name": "Leena AI", "industry": "saas-tech", "market": "us"},
]

for c in clients:
    print(f"\n{'='*60}")
    print(f"AUDIT: {c['name']}")
    print('='*60)
    
    system_prompt = load_skill_files(
        "./aeo-strategist", c["industry"], c["market"]
    )
    
    response = client.messages.create(
        model="claude-opus-4-5",
        max_tokens=3000,
        system=system_prompt,
        messages=[{
            "role": "user",
            "content": f"/audit\nClient: {c['name']}\nVertical: {c['industry']}\nMarket: {c['market']}\nAEO maturity: Zero"
        }]
    )
    
    print(response.content[0].text)
```

---

## 14. FAQ

**Q: Do I need all the files loaded for every session?**  
A: No. Always load `SKILL.md`. Then load only the industry and market files relevant to the client you're working on. Loading all files at once wastes context window.

**Q: Can I use this for a client in an industry not listed?**  
A: Yes. Use the `_ADD_NEW_INDUSTRY.md` template to create a new vertical file. The skill works without it — but compliance guidance and trust signal hierarchy will be generic rather than industry-specific.

**Q: What if the client is in two industries (e.g., healthcare + insurance)?**  
A: Load both industry files. Apply the strictest compliance constraint from either. The skill's onboarding intake flags this — "Multiple verticals? List all — apply strictest compliance constraint."

**Q: How long does each mode take to run?**  
A: Most modes produce complete output in 60–90 seconds. `/audit` and `/strategy` are the longest — 2–3 minutes. `/research` depends on live web search speed.

**Q: Can I use this with Claude API on any model?**  
A: Recommended: `claude-opus-4-5` for complex strategy modes (audit, strategy, competitor). `claude-sonnet-4-6` for production modes (brief, schema, rewrite) — faster and cheaper at equivalent quality for structured outputs.

**Q: Is the compliance guidance in this skill legally authoritative?**  
A: No. This is AEO strategy guidance — it tells you what compliance constraints to be aware of. Always pass regulated industry content through the client's actual compliance/medico-legal team before publication.

**Q: How do I track if the skill's recommendations are working?**  
A: Use `/track` to set up your measurement system. The 6-layer protocol (SOV snapshot, GA4 channel, brand search, citation audit, manual testing, competitor SOV) covers everything currently measurable. Expect to see Perplexity/RAG changes in 4–8 weeks. Parametric changes in 12–18 months.

**Q: Can I contribute new industry or market files?**  
A: Yes — PRs welcome. Use the `_ADD_NEW_INDUSTRY.md` or `_ADD_NEW_MARKET.md` templates. Include at least 2 eval cases in `evals/evals.json` when adding a new vertical.

---

*Built by [Indranil "Neel" Banerjee](https://linkedin.com/in/indranilbanerjee) — INT TechShu Digital*  
*Part of the [NeelVerse](https://indranil.in) ecosystem*
