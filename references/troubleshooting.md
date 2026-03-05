# Troubleshooting Guide — Why Isn't X Working?
## Diagnostic framework for common AEO failures
## INT TechShu Internal

---

## Problem 1: "Brand doesn't appear at all in AI responses"

**Diagnostic steps:**
1. Check robots.txt — is CCBot allowed? Is GPTBot allowed? (Use robotstxt.org checker)
2. Check if site is React/Vue/Angular SPA without SSR — if yes, AI crawlers see blank pages
3. Check Bing Webmaster Tools — is the site indexed? (ChatGPT uses Bing)
4. Check Brave Search — is the site indexed? (Claude uses Brave)
5. Check Wikidata — does the brand have an entry?
6. Run brand name search on Perplexity — does it show any web results for the brand?

**Most common culprit**: CCBot blocked in robots.txt (removes from training data) + React SPA with no SSR (invisible to all AI crawlers)

**Fix order**: robots.txt (1 day) → SSR/SSG migration (2–8 weeks) → Wikidata entry (2–4 hours) → content restructuring (ongoing)

---

## Problem 2: "AI says wrong things about the brand"

**Types of wrong:**
A. Wrong category ("Cipla is a healthcare platform" when it's a pharma manufacturer)
B. Wrong facts (wrong founding year, wrong founder, wrong HQ)
C. Outdated information (old product range, old pricing, old leadership)
D. Negative framing based on outdated news

**Diagnostic:**
- Which platform is getting it wrong? (They draw from different training data and retrieval)
- Is the correct information on the official website, structured clearly?
- Is there a Wikipedia article? (Wikipedia is very influential for parametric facts) Is it accurate?
- Is there a Wikidata entry? Is it current?
- Is the Google Knowledge Panel showing wrong info? (Update via Knowledge Panel feedback)

**Fix by type:**
A. Wrong category: Create explicit content using the correct category language. Multiple authoritative sources must use the same category association. Wikidata `instance of` property.
B. Wrong facts: Update Wikipedia (if editable), Wikidata, official website, Google Knowledge Panel. PR outreach with correct information.
C. Outdated info: Publish updated content with date stamps. Schema with `dateModified`. Earned media coverage with current information.
D. Negative framing: Long-term only — can't force AI to forget. Build overwhelming positive signal volume. Crisis PR to generate corrective coverage.

---

## Problem 3: "Competitor is always in AI responses, we're not"

**Diagnostic:**
1. Run `/competitor` mode — map their full AEO footprint across 5 signal categories
2. Identify the strongest anchor (usually one signal explains 60-70% of their advantage)
3. Assess how hard/fast that anchor can be replicated

**Most common competitor advantages:**
- They have a Wikipedia article. You don't.
- They've been covered by AI-licensed publications. You haven't.
- They have a Gartner MQ placement / G2 Leader status. You don't.
- They have significantly more Google Reviews / G2 reviews (volume matters).
- Their content uses answer-first structure. Yours doesn't.

**Fix strategy**: Don't try to replicate everything. Find the anchor. Build a plan to address the anchor specifically.

---

## Problem 4: "AI is citing us, but it's citing the wrong page"

**Situation**: AI cites your blog from 2021 instead of your current product page, or cites a third-party directory instead of your own site.

**Diagnostic:**
- Which URL is being cited? Why is that URL more "trustworthy" to the AI than your preferred page?
- Is the cited page better structured for extraction? (Often yes — third-party directories use clean, structured formats)

**Fix:**
- Restructure your preferred pages to be more extraction-friendly (answer-first, chunks, FAQ, schema)
- Add schema markup to preferred pages
- Increase authority of preferred pages via internal linking + external link building
- If a directory page is always cited, ensure it links prominently to your preferred URL

---

## Problem 5: "AI appeared for us last month, now it doesn't"

**Causes (most common):**
1. **Real-time retrieval shift** — Perplexity and Bing-based platforms serve live results; a newer page outranked yours
2. **AI model update** — Major model updates (GPT-4o → GPT-5, etc.) reshuffle parametric knowledge
3. **Negative press coverage** — A negative article published and AI now surfaces it
4. **Competitor published new content** — A competitor's new asset is now being retrieved instead of yours
5. **Your content was outdated** — Freshness signal degraded on your page

**Diagnostic**: Run the query again 3× in incognito across platforms. If it's consistent absence, it's structural. If it's intermittent, it's retrieval variance (normal).

**Fix**: Refresh the content on the page that was being cited (update stats, date, add new FAQ). Run IndexNow to push the update to Bing. Republish with new date.

---

## Problem 6: "Schema is deployed but Google Rich Results Test shows errors"

**Common errors:**
- Missing required properties: Check Google's documentation for that schema type — some properties are mandatory
- Price data outdated: `Offer` schema with old price fails validation
- Multiple conflicting schema blocks: Remove duplicate JSON-LD scripts
- Incorrect nesting: Parent/child type relationships must be properly structured
- Using deprecated properties: Check schema.org for current property names

**Diagnostic tool**: https://search.google.com/test/rich-results
**Schema validator**: https://validator.schema.org

---

## Problem 7: "Tracking shows AI traffic in GA4 but conversions are near zero"

**This is expected behaviour, not a failure.** AI-referred traffic behaves differently from SEO traffic:
- AI users have already consumed the answer — they're visiting to verify or go deeper, not to start a purchase journey
- AI referral sessions are often shorter and have lower immediate conversion rates
- The valuable metric is influenced conversions — users who saw brand in AI, then searched brand directly, then converted (dark social AI attribution problem)

**Fix for measurement**: Set up a multi-touch attribution model. Compare branded search volume trend to AI SOV growth. The correlation is the evidence of influence.

---

## Problem 8: "Client wants results in 60 days but AEO is showing no impact"

**The expectation problem — address proactively in onboarding.**

Reality: RAG layer results (content cited by Perplexity, Bing-grounded ChatGPT) can appear in 2–4 weeks if content is well-structured and site is indexed. Parametric layer results take 12–18+ months.

**What to show at 60 days:**
- Technical fixes deployed (robots.txt, schema, SSR — verifiable)
- Directory listings completed (count of ✅ vs ❌ at start vs now)
- Content pieces live that are structured for extraction (show the actual URLs)
- SOV baseline established + any early movement on Perplexity (fastest-moving platform)
- Wikidata entry created (tangible entity work)

Frame it: "We've built the infrastructure. The visibility impact on parametric models takes 12–18 months by definition. Here's what we can show right now in the retrieval layer."
