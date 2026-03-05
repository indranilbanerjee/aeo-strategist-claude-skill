# AEO Glossary — Internal Team Reference
## Terms, concepts, and frameworks used in this skill
## INT TechShu Internal

---

## Core AEO Concepts

**AEO (Answer Engine Optimization)**
The practice of optimizing content, entities, and authority signals so that AI systems (ChatGPT, Gemini, Perplexity, Claude, Copilot) accurately and positively reference a brand in their generated responses. Distinct from SEO in that the goal is AI citation, not search engine ranking.

**GEO (Generative Engine Optimization)**
Interchangeable term for AEO. Used more in academic and US industry literature. Same meaning.

**Parametric Knowledge**
Information encoded into an AI model's weights during training. When you ask ChatGPT "who makes the best CRM software?" and it answers without searching the web, it's drawing on parametric knowledge. This is the hardest thing to influence because it requires the training data ecosystem, not just a web page.

**RAG (Retrieval-Augmented Generation)**
The mechanism by which AI systems fetch current information from the web at query time and incorporate it into responses. When Perplexity answers a question and shows citations, it's using RAG. This is the more immediately actionable AEO layer — you can influence it by optimising live content.

**AI Share of Voice (AI SOV)**
Metric: For a defined set of category queries, what percentage of AI responses mention the brand? Formula: (Queries where brand appears ÷ Total tracked queries) × 100. Tracked per platform.

**Extraction Unit**
A self-contained paragraph of 40–60 words that answers exactly one question completely. AI systems extract these as answer atoms. Content structured as extraction units is cited at higher rates than content in long, flowing paragraphs.

**Grounding Hook**
A piece of evidence within content that tethers an AI system's retrieval to a factual source. Types: statistics with source citation, expert quotes with credentials, government or regulatory references, clinical trial numbers, company registration numbers. Grounding hooks reduce the probability of AI hallucinating alternative facts.

**Parametric Lag**
The delay between building external trust signals and seeing them reflected in AI responses. Training data lags real-world changes by months to years. A brand that starts building earned media today won't see parametric influence until the next major model training cycle — typically 12–18+ months.

**Entity**
In AEO/SEO, an entity is a uniquely identifiable thing (a person, company, place, product) with a stable real-world identity. Entities have properties (name, industry, location, services) and relationships (sameAs links to Wikidata, Wikipedia, LinkedIn). AI systems recognize brands as entities, not just keywords.

**Entity Fragmentation**
When a brand's name, description, category, or facts are described inconsistently across different sources. "Cipla — pharmaceutical company" on LinkedIn but "Cipla — healthcare brand" on JustDial creates fragmentation. AI averages these inconsistencies into a blurry entity representation.

**sameAs**
Schema.org property linking a brand's website to its equivalent entries on Wikidata, Wikipedia, LinkedIn, Crunchbase, and industry directories. This merges fragmented entity signals into a coherent representation. Critical for entity building.

**Trust Signal Hierarchy**
The ranked order of signal types that AI systems weight when determining how authoritative a source is. Different for every vertical — a NABH accreditation is top of the hierarchy for hospitals but irrelevant for SaaS. See industry files for vertical-specific hierarchies.

**Dark Social AI**
AI responses that don't generate observable traffic or citations. When a user gets an AI answer inside WhatsApp, Microsoft Office, or a private ChatGPT session and the brand is mentioned, there is no referral traffic, no trackable click, no audit trail. The influence happened — it just can't be measured. Estimate: 40–60% of AI brand influence is dark.

**AI Overviews (formerly SGE)**
Google's integration of Gemini-powered answers directly into search results pages. Appears above organic results for an increasing proportion of queries. Separate from gemini.google.com — but content optimized for Gemini AI Overviews follows the same structural principles.

**Canonical Brand Description**
A 2–3 sentence factual, declarative description of a brand that is deployed identically across all web properties (website About page, LinkedIn summary, Wikidata description, directory profiles). When AI encounters this identical description repeatedly across trusted sources, it encodes it as the authoritative entity description.

**Intent Proximity Framework**
INT TechShu's prioritization framework for AEO query targeting. Build bottom-up from purchasing intent: Decision → Comparison → Awareness. Never start with awareness content if decision-stage queries are unoptimized.

**Layer A (Parametric Layer)**
The long-term (12–24 month) strategy component: building distributed presence across earned media, directories, databases, and community signals to influence future AI training data.

**Layer B (RAG Layer)**
The immediate (days–weeks) strategy component: structuring live web content for AI retrieval systems to extract and cite right now.

**Displacement (Competitive)**
The act of replacing a competitor in AI responses. Occurs when a brand builds stronger trust signals in the categories where a competitor currently dominates AI responses. Takes months of sustained effort — not a one-time campaign.

**Strongest Anchor**
In competitive analysis, the single signal most responsible for a competitor's AEO dominance. Could be a Gartner MQ placement, a Wikipedia article, a Reddit thread that went viral, or a branded data study. Identifying the anchor focuses displacement efforts.

---

## Technical Terms

**JSON-LD (JavaScript Object Notation for Linked Data)**
The preferred format for Schema.org structured data implementation. A `<script type="application/ld+json">` block in HTML that marks up entity and content type data for search engines and AI systems to read.

**robots.txt**
A text file at yourwebsite.com/robots.txt that instructs web crawlers on which pages to access. For AEO, it must explicitly allow AI crawlers: GPTBot, ClaudeBot, PerplexityBot, CCBot, OAI-SearchBot, GoogleOther.

**IndexNow**
A protocol that allows websites to notify search engines (Bing, Yandex) immediately when content changes, rather than waiting for scheduled crawl. Speeds up content propagation through the Bing ecosystem (which feeds ChatGPT and Copilot).

**llms.txt**
A proposed standard (similar to robots.txt but for LLMs) where brands publish a concise, structured summary of their identity, offerings, and preferred descriptions at yourdomain.com/llms.txt for AI systems to read.

**Wikidata**
A free, structured knowledge base that Wikipedia and most major AI systems use for entity data. If a brand has a Wikidata entry (Q-number / QID), AI systems have a verified entity anchor for it. Missing Wikidata = entity fragmentation risk.

**SSR (Server-Side Rendering)**
Web application architecture where HTML is generated on the server before sending to the browser. AI crawlers can read SSR content. Client-side-only React/Vue SPAs cannot be read by AI crawlers without SSR.

**CCBot**
Common Crawl crawler. Common Crawl is the internet archive that most LLM training datasets are built on. Blocking CCBot in robots.txt effectively removes a brand from most AI training data. A common mistake — should be explicitly allowed.

**Schema.org**
The vocabulary standard for structured data markup. Provides types (Organization, Product, FAQPage, etc.) and properties that give AI systems and search engines machine-readable metadata about page content.

---

## Regulatory Shorthand (Quick Reference)

| Term | Full Name | Market | Industry |
|------|-----------|--------|---------|
| CDSCO | Central Drugs Standard Control Organisation | India | Pharma |
| SEBI | Securities and Exchange Board of India | India | BFSI |
| RBI | Reserve Bank of India | India | Banking |
| IRDAI | Insurance Regulatory and Development Authority of India | India | Insurance |
| RERA | Real Estate Regulatory Authority | India | Real Estate |
| NABH | National Accreditation Board for Hospitals | India | Healthcare |
| NABL | National Accreditation Board for Testing Labs | India | Diagnostics |
| BIS | Bureau of Indian Standards | India | Manufacturing |
| FSSAI | Food Safety and Standards Authority of India | India | F&B |
| ARAI | Automotive Research Association of India | India | Automotive |
| NAAC | National Assessment and Accreditation Council | India | Education |
| FDA | Food and Drug Administration | US | Pharma/Food |
| SEC | Securities and Exchange Commission | US | BFSI |
| FCA | Financial Conduct Authority | UK | BFSI |
| EMA | European Medicines Agency | EU | Pharma |
| GDPR | General Data Protection Regulation | EU/UK | Data/Tech |
| DFSA | Dubai Financial Services Authority | UAE | BFSI |
| MAS | Monetary Authority of Singapore | Singapore | BFSI |
