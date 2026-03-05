# Tracking Protocols — AEO Measurement
## How to set up, run, and maintain AEO tracking for retainer clients
## INT TechShu Internal Reference

---

## The Measurement Problem

AEO has no equivalent of Google Search Console. There is no dashboard that shows you your AI Share of Voice (SOV). Tracking is manual, inferential, and requires a structured protocol to be useful. This document tells your team exactly how to do it.

---

## Layer 1: AI Share of Voice (SOV) Baseline

### What to Track
AI SOV = For a defined set of category queries, in how many AI responses does the brand appear?

### Setup Protocol

**Step 1: Seed the query set**
Use the `/query-library` mode output. Take the 30-query set and select:
- Top 10 decision-stage queries (highest commercial value)
- Top 5 comparison queries (competitive intelligence)
- Top 5 brand-specific queries ("is [brand] X")
= 20 tracked queries per client

**Step 2: Platform allocation**
For each query, test on: ChatGPT, Gemini, Perplexity (minimum). Add Claude if relevant vertical. For India clients, add ChatGPT with Bing-grounded mode specifically.

**Step 3: Capture the full response, not just a mention flag**
Document per query per platform:
- Brand mentioned: Yes / No
- Position: Primary recommendation / Listed among options / Mentioned as aside / Not mentioned
- Source cited: Which URL or publication is Perplexity citing? Which source grounds the claim?
- Competitor mentioned: Which competitor appears in the same response?
- Sentiment: Positive / Neutral / Negative / Inaccurate
- Exact phrasing (copy first 2 sentences of how brand is described)

**Step 4: Record in the SOV baseline sheet**
Use this structure:
| Query | Platform | Brand Appears | Position | Source URL | Competitor Named | Sentiment | Date |

**Step 5: Photograph or screenshot every response**
AI responses change. Screenshots with timestamp are the evidence trail for attribution and disputes.

### Cadence
- **Baseline**: Run all 20 queries × all platforms before any optimization work starts
- **Monthly**: Run full set. Compare to previous month. Note changes.
- **Post-action**: Run relevant subset 2–3 weeks after a specific optimization action (new content live, schema deployed, directory updated) to test attribution.

---

## Layer 2: GA4 Custom Channel Group for AEO Traffic

### Purpose
Isolate traffic from AI platforms in GA4 so you can measure referral quality and conversion behaviour.

### Setup Steps

1. In GA4 → Admin → Data Display → Channel Groups → Create custom channel group
2. Name: "AI Referral Traffic"
3. Add rules for each AI platform referrer:
   - Source contains: chat.openai.com
   - Source contains: chatgpt.com
   - Source contains: perplexity.ai
   - Source contains: gemini.google.com
   - Source contains: bard.google.com (legacy)
   - Source contains: copilot.microsoft.com
   - Source contains: bing.com (filter to AI-specific user agents if possible)
   - Source contains: claude.ai

4. Enable channel group as default comparison channel

### What This Tells You
- How many sessions are arriving from AI platforms
- Which pages are being cited (landing pages from AI referrals)
- Engagement quality (bounce rate, pages per session, goal completions vs. SEO traffic)
- Conversion comparison: does AI-referred traffic convert differently?

### Limitation
**The dark social AI problem**: ChatGPT Pro users, Claude.ai, and Copilot inside Office apps often do NOT generate referral traffic even when they cite a brand. AI SOV ≠ GA4 AI referral traffic. Both measurements are needed. GA4 tracks influence that resulted in a click; SOV tracking captures influence that didn't.

---

## Layer 3: Brand Search Volume as AEO Proxy

### Why This Matters
When AI cites a brand, curious users often don't click the AI link — they Google the brand directly. Branded search volume growth is therefore a proxy for AI influence that doesn't show up in referral data.

### Setup
- Google Search Console: Monitor branded query impressions and clicks monthly
- Google Trends: Set alert/track for brand name + key category association terms
- Comparison: Set up [brand] vs [competitor] trend tracking

### Interpretation
If branded search volume grows 20% in a quarter with no paid media increase, that's an indicator of organic AI influence growth. Correlate with SOV snapshots from Layer 1.

---

## Layer 4: Citation Source Audit

### Purpose
Understand which of your content assets are being cited by AI platforms. This tells you what's working and what to replicate.

### How to Run
1. For Perplexity responses (most transparent): note every source URL cited alongside brand mentions
2. For ChatGPT: note when specific pages or publications are referenced (visible in web search mode)
3. Build a "cited assets" list: which pages, which publications, which directories, which content types are generating citations

### Use in Reporting
- "This month, Perplexity cited [page URL] in 4 of 8 responses mentioning [brand]"
- "Healthcare queries are being grounded by Practo listing, not website"
- "Competitor is being cited via ET Healthworld — target same publication"

---

## Layer 5: Manual Query Testing Protocol

### Why Manual Testing?
AI responses are non-deterministic — same query returns different answers in different sessions. A single test doesn't give reliable data. A structured protocol does.

### Rules
- Always use Incognito/Private mode (no personalisation bleed)
- Log out of all Google/ChatGPT accounts before testing
- Run each query minimum 3 times across different sessions
- Note variation — if brand appears in 2/3 tests, SOV = 67% for that query
- Test at consistent time of day (AI responses can shift with real-time data)

### Monthly Testing Workflow
Day 1 of month: Run all 20 tracked queries × all platforms × 3 times each
= ~60 data points per platform per month
= ~180–240 total observations per month (3 platforms minimum)

This is a half-day task. Assign to a junior team member with clear documentation protocol. Review findings in monthly strategy call.

---

## Layer 6: Competitor SOV Tracking

Run the same query set but record competitor mentions rather than client mentions. This gives a competitive SOV ratio.

Client SOV = [Brand appears in X / Total queries tracked]
Competitor SOV = [Competitor appears in X / Total queries tracked]
SOV Delta = Client SOV − Competitor SOV

Track this monthly. The goal is to narrow or reverse the delta, not just improve absolute numbers.

---

## Recommended Tool Stack

| Need | Free Option | Paid Option |
|------|-------------|-------------|
| Query testing | Manual (Incognito) | Scraper for snapshot automation (custom build) |
| SOV logging | Google Sheets template | Airtable or Notion database |
| GA4 AI channel | GA4 native (free) | Looker Studio dashboard |
| Brand search tracking | Google Search Console | SEMrush / Ahrefs brand monitoring |
| Citation monitoring | Manual Perplexity reading | Meltwater / Mention (partial) |
| Screenshot archiving | CleanShot X / Snagit | Loom recording for video evidence |

### Note on Automated SOV Tools
Tools claiming to automate AI SOV tracking (e.g., AthenaHQ, Profound, Trackr) are early-stage as of early 2026. Evaluate them on: query breadth, platform coverage, response sampling methodology. Most are US-centric and miss Indian platforms. Manual protocol above is more reliable for India-first clients.
