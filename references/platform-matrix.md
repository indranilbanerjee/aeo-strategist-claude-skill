# Platform Matrix — AEO Strategist
## Per-platform optimization rules, source preferences, and crawler requirements

---

## ChatGPT (OpenAI)

**Primary Search Index**: Microsoft Bing
**Crawlers to allow in robots.txt**: GPTBot, OAI-SearchBot, ChatGPT-User
**Query Routing**: ~31% of queries trigger web search; ~69% answered parametrically
**Training Data Frequency**: GPT-4 knowledge cutoff varies; RAG via Bing is real-time

**Source Type Preferences (ranked)**:
1. Curated listicles and "best of" lists from high-DA domains
2. Directories: Yelp, TripAdvisor, G2, Clutch, Capterra, industry-specific
3. Wikipedia and Wikidata (entity grounding)
4. AI-licensed publisher content: News Corp, Condé Nast, Financial Times, Reuters, Associated Press
5. Reddit (formal data agreement with OpenAI — $60–70M annually)
6. Brand-owned content (lower priority than earned media)

**Key Partnership Impact**: Licensed publishers get priority placement. If a client has been covered by FT, Reuters, or News Corp properties, flag this as a high-value citation asset.

**Schema Weight**: Moderate — Bing's structured data guidelines apply
**Content Freshness**: Moderate preference — not as strong as Perplexity

**Optimization Priority**:
- Bing Webmaster Tools verification is non-negotiable
- IndexNow implementation for faster content propagation
- Reddit presence matters more here than other platforms
- "Best of" list placements are highest-ROI action for ChatGPT visibility

**Regional Notes**:
- India: Bing index coverage is lower than Google — prioritize IndexNow
- US/UK: Bing coverage strong; focus on licensed publisher relationships

---

## Google Gemini

**Primary Search Index**: Google Search
**Crawlers**: Googlebot (standard; already in most robots.txt)
**Query Routing**: Deep integration with Google AI Overviews (2B+ monthly users)
**Training Data**: Internal Google data; also uses live Google Search for grounding

**Source Type Preferences (ranked)**:
1. Brand-owned sites (higher weight than other platforms — Google trusts verified brand sources)
2. Google Business Profile and Knowledge Graph (unique to Gemini)
3. Google-verified entities (structured data, verified by Search Console)
4. Google-licensed content sources
5. YouTube (cited in 25% of AI Overview responses — critical for Gemini specifically)
6. High-DA independent sites

**Key Differentiator**: Google Business Profile weight. For local businesses, real estate, and any brand with physical presence, GBP optimization is the #1 Gemini AEO action.

**Schema Weight**: HIGHEST — Google's structured data guidelines directly feed Knowledge Graph
**Content Freshness**: Standard — not as real-time as Perplexity

**Optimization Priority**:
- Google Search Console verification
- Knowledge Panel claim and completion
- Google Business Profile (where applicable): 100% complete, Q&A populated, reviews active
- YouTube content creation (transcripts essential for AI Overview citation)
- Schema markup: Google's rich result guidelines + entity markup
- Wikidata entry: Google uses this for Knowledge Graph entity grounding

**Regional Notes**:
- India: Google dominates search (>95% share) — Gemini is therefore most important platform for Indian clients
- European clients: GDPR-aware content framing may affect AI Overview inclusion

---

## Perplexity AI

**Primary Search Index**: Own hybrid index (Bing API + Google API + proprietary crawl)
**Crawlers**: PerplexityBot
**Query Routing**: Near-100% web-grounded (Perplexity is a live search engine at core)
**Training Data**: Real-time retrieval; parametric base model is Sonar/custom

**Source Type Preferences (ranked)**:
1. High-authority niche/specialist sites (beats general DA sites for category-specific queries)
2. Academic and research publications (highly cited in Perplexity answers)
3. Reddit threads (strong signal, especially for product/brand sentiment queries)
4. Technical documentation sites
5. Live news and recent content (freshness is more important here than other platforms)
6. Industry publications and trade press

**Key Differentiator**: Perplexity has the highest citation density — it cites more sources per answer than any other platform. Content freshness (pages updated in last 30 days) gets meaningful boost.

**Schema Weight**: Moderate — less reliant on schema than Gemini
**Content Freshness**: HIGHEST — most important platform for content recency

**Optimization Priority**:
- Content update cadence (regular updates beat one-time optimization)
- Technical documentation depth (developer and researcher audiences)
- Reddit presence is especially important here
- Specialist niche site coverage (trade press, vertical-specific publications)
- Perplexity's Publishers Program — apply if client has content operation

**Regional Notes**:
- Perplexity is strongest with US technical/research audiences
- Growing fast in India among tech-savvy and startup audiences
- Less dominant in markets where Google is overwhelming (Southeast Asia, South Asia general consumer)

---

## Claude (Anthropic)

**Primary Search Index**: Brave Search (86.7% overlap with Brave's top non-sponsored results)
**Crawlers**: ClaudeBot (relies on Brave; no independent crawler currently)
**Query Routing**: Variable; Claude searches when needed for current information

**Source Type Preferences (ranked)**:
1. Independent, diverse sources (Claude explicitly values source diversity over repetition)
2. High-trust non-commercial sources
3. Brave Search's indexed content (Brave has privacy-first index, less commercial bias)
4. Technical and research content
5. Earned media from non-AI-licensed publications (Brave doesn't have same licensing deals)

**Key Differentiator**: Claude weights independent verification most heavily. A brand mentioned in 5 independent high-quality sources is more credible to Claude than a brand with one major licensing deal.

**Schema Weight**: Low-moderate — Brave's index is less structured-data-forward
**Content Freshness**: Moderate

**Optimization Priority**:
- Brave Search indexing verification (often overlooked)
- Diversity of independent sources (not just AI-licensed publishers)
- Clean, factual, declarative content (Claude penalizes promotional language)
- Avoid content that reads as marketing — Claude's training emphasizes epistemic honesty

**Regional Notes**:
- Claude is strongest with enterprise, technical, and research users
- Growing in India among AI-native professional segment
- Less dominant for consumer mass-market queries in any region

---

## Microsoft Copilot

**Primary Search Index**: Bing
**Crawlers**: Same as ChatGPT (Bing ecosystem)
**Query Routing**: Bing-powered; strong Microsoft 365 integration

**Key Differentiator**: Enterprise deployment. M365 Copilot reaches users inside Word, Outlook, Teams, and Excel — the "dark social AI" problem. These responses are unobservable by any tracking tool.

**Optimization Priority**:
- Same as ChatGPT/Bing optimization applies
- Enterprise case studies and B2B credibility signals matter more here
- LinkedIn company page optimization (Microsoft owns LinkedIn)
- Bing Places for Business (local equivalent of GBP)

---

## Platform Selection by Use Case

| Client Type | Priority Order |
|---|---|
| Local/Regional India (general) | Gemini → ChatGPT → Perplexity |
| Enterprise B2B India | Gemini → Perplexity → Claude → Copilot |
| Consumer E-commerce | Gemini → ChatGPT → Perplexity |
| Pharma HCP | Perplexity → Claude → Gemini |
| BFSI Consumer | Gemini → ChatGPT → Perplexity |
| SaaS/Tech Global | Perplexity → ChatGPT → Claude |
| Real Estate India | Gemini → ChatGPT → (local queries dominate) |

---

## Crawler robots.txt Template

```
# AI Crawler Access — Standard Configuration
User-agent: GPTBot
Allow: /

User-agent: OAI-SearchBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: CCBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: GoogleOther
Allow: /

User-agent: Googlebot
Allow: /

# Block if content is NOT for AI training
# User-agent: GPTBot
# Disallow: /
```

---

## Emerging Platforms (Monitor — No Direct Optimization Yet)

### Meta AI (WhatsApp / Facebook / Instagram)
- Uses Bing as search engine backend
- Highest penetration in India, Africa, Southeast Asia, Brazil
- Same Bing optimization (IndexNow, Bing WMT) applies
- Dark social: no observable referral traffic. Influence is real but unmeasured.
- Growing rapidly for consumer queries in vernacular languages

### Apple Intelligence / Siri
- Uses web results + private Apple Knowledge Graph
- Important for iOS-heavy consumer segments (urban India, US, UK)
- No direct optimization path beyond standard Bing + rich content

### Amazon Alexa
- Voice-first
- Local business queries, product queries, general knowledge
- Schema markup (especially `speakable` property) helps voice extraction
- Declining relative market share but still significant for US homes

### Google Assistant
- Voice queries: structured content + featured snippet optimization overlaps with AEO
- Local business queries: Google Business Profile is the dominant signal
- Growing in regional Indian languages

### LinkedIn AI (CoPilot for LinkedIn / AI features in feed)
- B2B brand signals are highly weighted
- Company page completeness, employee expertise, LinkedIn articles
- Microsoft parent = Bing index integration
- Important for B2B SaaS, professional services, BFSI enterprise

### Grok (X/Twitter AI)
- Uses X (Twitter) data primarily
- Relevant for brands with strong Twitter/X presence
- Growing US market; limited India relevance currently

---

## Platform-Specific Content Freshness Windows

| Platform | How Fresh Should Content Be? |
|----------|------------------------------|
| Perplexity | Updates in last 30 days get boost. Update key pages monthly. |
| ChatGPT (Bing-grounded) | Bing crawl lag 1–7 days with IndexNow. Without IndexNow: 2–4 weeks. |
| Gemini (Google AI Overviews) | Google crawl lag: 1–14 days for known sites. Use Sitemap ping. |
| Claude (Brave Search) | Brave crawl: 2–4 weeks typical. No IndexNow support. |
| Parametric (all platforms) | Training data: months to years. Not a freshness play. |

---

## Quick Technical Checklist Per Platform

### For ChatGPT/Copilot visibility:
- [ ] Bing Webmaster Tools verified
- [ ] IndexNow implemented (immediate Bing propagation)
- [ ] GPTBot, OAI-SearchBot allowed in robots.txt
- [ ] Content on key pages structured for extraction (no SPA blocking)
- [ ] Reddit presence active in relevant subreddits

### For Gemini/AI Overviews visibility:
- [ ] Google Search Console verified
- [ ] Sitemap submitted to GSC
- [ ] Google Business Profile complete (where applicable)
- [ ] Schema markup deployed (Google reads this directly)
- [ ] YouTube content with transcripts (cited in ~25% of AI Overviews)
- [ ] GoogleOther user-agent allowed in robots.txt

### For Perplexity visibility:
- [ ] PerplexityBot allowed in robots.txt
- [ ] Publishers Program application submitted (if content-heavy brand)
- [ ] Content freshness: key pages updated in last 30 days
- [ ] Specialist niche publications covering brand
- [ ] Reddit presence (Perplexity pulls Reddit significantly)

### For Claude visibility:
- [ ] ClaudeBot allowed in robots.txt
- [ ] Brave Search indexing verified
- [ ] Independent source diversity (Brave values source breadth)
- [ ] Declarative, factual content tone (Claude penalises promotional language)
