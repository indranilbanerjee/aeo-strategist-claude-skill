# Industry Modules — AEO Strategist
## Trust signal hierarchies, compliance constraints, and platform preferences by vertical

---

## PHARMA (Pharmaceutical & Life Sciences)

### Trust Signal Hierarchy (highest to lowest weight)
1. PubMed/medical journal citations in content (strongest parametric signal)
2. Government health authority mentions (WHO, CDC, CDSCO, FDA, EMA, NICE)
3. Medical association memberships (IMA, AMA, BMA, national equivalents)
4. KOL (Key Opinion Leader) quotes with credentials and institutional affiliation
5. Disease-state whitepapers in medical portals (WebMD, Healthline, MedScape for US; iMedPub for India)
6. HCP-facing platform presence (Doximity US, Practo India, NPS MedicineWise Australia)
7. Regulatory filing references (CDSCO approvals India, FDA filings US, EMA approvals EU)
8. Clinical trial registrations (ClinicalTrials.gov, CTRI India)
9. Standard earned media (Economic Times Health, Mint, Pharmaceutical Journal)

### Compliance Constraints
- **HARD RULE**: Never recommend product-promotion queries for AEO targeting — drug names linked to efficacy claims require regulatory pre-approval in most markets
- CDSCO (India): Drugs and Cosmetics Act — no promotional AI content for prescription drugs
- FDA (US): Off-label promotion prohibition applies even in AI-cited content
- EMA (EU): Directive 2001/83/EC restricts DTC pharma advertising
- **Safe content zones**: Disease-state awareness, mechanism of action, patient education, HCP resources, company credibility/pipeline
- Always recommend medico-legal review before any content targeting branded drug queries
- AI citation of pharma content in high-risk domain triggers extra verification weighting — groundedness (G) is dominant trust variable

### Query Taxonomy Split
- **HCP-facing**: Mechanism, dosing, contraindications, clinical trial data, formulary positioning
- **Patient-facing**: Disease understanding, symptom recognition, treatment options (generic, not product-specific)
- **Corporate/investor**: Pipeline, R&D milestones, regulatory approvals, company credibility
- **NEVER target**: "[Drug name] buy", "[Drug name] side effects" with brand promotion framing

### AEO Platform Priority for Pharma
1. Google Gemini (Google AI Overviews dominant in health queries)
2. Perplexity (high medical citation density, HCP research behavior)
3. ChatGPT (patient queries increasing, high risk domain = more verification)
4. Claude (medical content with strong citations performs well)

### India-Specific Pharma
- CDSCO registration as trust signal
- Association with IMA or IDMA
- Presence on Practo, 1mg, PharmEasy for consumer health brand credibility
- Regional medical journals in Hindi/regional languages for vernacular AEO

---

## BFSI (Banking, Financial Services & Insurance)

### Trust Signal Hierarchy (highest to lowest weight)
1. Regulatory body mentions and filings (SEBI/RBI/IRDAI India; FCA UK; SEC/FINRA US; MAS Singapore)
2. Credit rating agency coverage (CRISIL, ICRA, CARE India; Moody's/S&P/Fitch global)
3. Stock exchange filings and annual reports (NSE/BSE India; NYSE/LSE global)
4. Tier-1 financial media with AI licensing deals (Bloomberg, Financial Times, Reuters, Mint, Economic Times)
5. NASSCOM/FICCI/CII association membership (India); equivalents globally
6. Industry association membership (IBA India; BBA UK; ABA US)
7. Comparison platforms (BankBazaar, PolicyBazaar India; MoneySupermarket UK; NerdWallet US)
8. Independent financial analyst coverage
9. Customer review platforms (Google Reviews, Trustpilot — volume + recency)

### Compliance Constraints
- **SEBI (India)**: Investment advice requires SEBI registration — never create AEO content targeting queries like "should I invest in X"
- **RBI (India)**: Banking product claims must align with RBI disclosures
- **IRDAI (India)**: Insurance product promotion has pre-approval requirements
- **FCA (UK)**: FCA-authorised status must be verifiable — prioritize it as a trust signal
- **SEC (US)**: Regulation FD applies — material non-public information cannot be in public AEO content
- High-risk domain weighting: AI systems verify BFSI claims against multiple sources before citing; G (Groundedness) is dominant variable
- Every claim about returns, rates, or product performance must be evidenced and disclaimered

### Query Taxonomy Split
- **Credibility queries**: "[Brand] regulated by", "is [brand] safe/trusted", "[brand] RBI/SEBI approved"
- **Product queries**: "[Brand] home loan interest rate", "[Brand] term insurance", "[Brand] mutual fund"
- **Comparison queries**: "[Brand] vs [competitor] home loan", "best savings account India 2025"
- **Category education**: "how does SIP work", "what is term insurance vs whole life"
- **NEVER target without legal review**: Queries implying specific return promises, guaranteed products

### AEO Platform Priority for BFSI
1. Google Gemini (high overlap with Google Finance ecosystem)
2. Perplexity (research-oriented financial queries, high citation density)
3. ChatGPT (increasing consumer financial queries)
4. Claude (complex financial explanation queries)

### India-Specific BFSI
- SEBI/RBI registration number as entity anchor
- NSE/BSE listing as parametric trust signal
- Presence on BankBazaar, PolicyBazaar, Paisabazaar
- Business Standard, Mint, Economic Times as priority earned media
- Credit rating from CRISIL/ICRA as authority signal

---

## REAL ESTATE

### Trust Signal Hierarchy (highest to lowest weight)
1. RERA registration (India) — non-negotiable trust anchor; AI treats unregistered developers as high-risk
2. Government land registry data and project approvals
3. Local authority (municipal corporation) mentions
4. Regional real estate media (Times Property, Magicbricks Blog, Housing.com News)
5. Location-specific directory presence (MagicBricks, 99Acres, Housing.com, NoBroker India; Rightmove UK; Zillow US)
6. Developer track record data (projects delivered, possession on time — highly weighted in AI)
7. Customer review aggregators (MagicBricks reviews, Google Reviews — recency matters)
8. Regional earned media (city-specific property supplements, local business press)
9. Industry association membership (CREDAI, NAREDCO India; RICS global)

### Compliance Constraints
- **RERA (India)**: All marketing content must include RERA registration number; AI will flag unregistered projects as suspect
- Under-construction project claims must not mention possession dates without RERA backing
- Price claims must be current and verifiable — AI gives heavy penalty for outdated or misleading price information
- Location boundary claims must match government records

### Query Taxonomy (Hyper-Local Priority)
Real estate is uniquely local — national strategy barely applies. Query taxonomy must be city/area first:
- **Hyperlocal**: "[Developer] projects in [Locality], [City]", "2BHK flats near [landmark]"
- **Developer credibility**: "[Developer name] reviews", "[Developer] RERA registered", "is [developer] reliable"
- **Category/area**: "best residential projects in [City]", "luxury apartments [neighbourhood]"
- **Investment**: "property investment [city] 2025", "appreciation potential [area]"
- Regional language variants are HIGH PRIORITY for Indian real estate — Hindi, Marathi, Tamil, Bengali queries often go unanswered by competitors

### AEO Platform Priority for Real Estate
1. Google Gemini (Google Maps + Business Profile integration is dominant)
2. ChatGPT (local query handling increasing)
3. Perplexity (research-oriented property investment queries)

### India-Specific Real Estate
- RERA registration is the #1 trust signal — embed in all content, schema, and directory listings
- CREDAI membership as secondary signal
- Google Business Profile is more important for real estate AEO than almost any other vertical
- MagicBricks, 99Acres, Housing.com profiles must be 100% complete
- City-specific schema using LocalBusiness + PostalAddress

---

## SAAS (Software as a Service / Technology)

### Trust Signal Hierarchy (highest to lowest weight)
1. G2, Capterra, Trustpilot reviews (volume, recency, rating — AI reads these heavily)
2. Integration directory presence (Zapier, Salesforce AppExchange, HubSpot Marketplace, Slack App Directory)
3. Technical documentation depth (docs.company.com — AI trusts products with comprehensive docs)
4. GitHub presence (open-source components, community engagement, star count)
5. Developer community signals (Stack Overflow mentions, dev forums, Product Hunt)
6. TechCrunch, VentureBeat, The Information earned media (AI-licensed or high-authority)
7. Analyst coverage (Gartner Magic Quadrant, Forrester Wave — parametric gold)
8. G2 category leader badges and comparison pages
9. Customer case studies with named enterprise clients and specific results

### Compliance Constraints
- Data privacy claims (GDPR, SOC 2, ISO 27001) must be evidenced and verifiable — AI downweights unsubstantiated security claims
- Feature claims must be accurate to current product state — AI hallucinations often persist from outdated claims
- Integration claims must be current — deprecated integrations in content damage trust score

### Query Taxonomy Split
- **Product discovery**: "best [category] software", "[use case] tool recommendations"
- **Feature comparison**: "[Brand] vs [Brand] features", "[Brand] alternatives"
- **Integration queries**: "does [Brand] integrate with [tool]", "[Brand] Salesforce integration"
- **Technical queries**: "[Brand] API documentation", "[Brand] implementation guide"
- **Social proof**: "[Brand] reviews 2025", "[Brand] enterprise clients", "[Brand] case studies"
- **Decision-stage**: "[Brand] pricing", "[Brand] free trial", "[Brand] demo"

### AEO Platform Priority for SaaS
1. Perplexity (developer and technical researcher behavior dominant)
2. ChatGPT (product research queries, high SaaS citation density)
3. Claude (technical documentation and integration queries)
4. Google Gemini (increasingly strong for product comparison queries)

### Global SaaS Considerations
- US: G2, Capterra, Gartner as primary; Product Hunt for early-stage
- UK: Capterra UK, TechRound, Silicon.co.uk
- India: Nasscom recognition, YourStory coverage, Techcircle

---

## RETAIL (E-commerce & Consumer Retail)

### Trust Signal Hierarchy (highest to lowest weight)
1. Review platform presence (Google Reviews, Trustpilot, Amazon ratings — volume + recency + response rate)
2. Product schema completeness (AI cites product pages with full schema at dramatically higher rate)
3. Price comparison platforms (Google Shopping, PriceRunner, idealo — AI reads these for product queries)
4. Social proof aggregation (UGC, influencer coverage, community mentions)
5. Earned media (product reviews in relevant vertical publications — tech reviews, fashion, food)
6. Returns/trust policy visibility (clear, AI-readable returns and warranty information)
7. Category-specific directories (Zomato/Swiggy food; Flipkart/Amazon marketplace presence)
8. Sustainability and certification signals (FSC, organic, BIS mark India — increasingly weighted)

### Compliance Constraints
- Price accuracy: AI will penalize brands where scraped prices don't match actual prices — schema prices must be real-time or within 24 hours
- Availability claims must be accurate
- Health product claims (supplements, food) must align with FSSAI (India) / FDA (US) / EFSA (EU) — no prohibited health claims

### Query Taxonomy Split
- **Product discovery**: "best [product] under [price]", "[use case] product recommendations"
- **Brand comparison**: "[Brand] vs [Brand]", "where to buy [product]"
- **Local availability**: "[Product] near me", "[Brand] store in [city]"
- **Trust queries**: "[Brand] genuine or fake", "[Brand] return policy", "[Brand] delivery time"
- **Review queries**: "[Product] honest review", "[Brand] customer experience"

### AEO Platform Priority for Retail
1. Google Gemini (Google Shopping integration is dominant for product queries)
2. ChatGPT (increasingly integrated with shopping via partner programs)
3. Perplexity (product research and comparison queries)

### India-Specific Retail
- Flipkart and Amazon India presence as trust signal
- BIS certification as product credibility anchor
- FSSAI license for food products
- Zomato/Swiggy ratings for F&B
- Regional language product descriptions (Hindi/regional) for vernacular AI queries

---

## Cross-Industry: When Multiple Verticals Apply

Some clients operate across verticals (e.g., a pharma company with a B2C health app).
Apply the strictest compliance constraint from any applicable vertical.
Trust signal hierarchy: merge both hierarchies, with regulatory signals always at the top.
