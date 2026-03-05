# Industry: SaaS, Technology & IT Services
## B2B SaaS, IT Outsourcing, Cloud, Cybersecurity, AI Products
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. B2B SaaS products (CRM, HRM, ERP, marketing automation, project management)
2. IT services and outsourcing (TCS/Infosys model — ITES/BPO)
3. Cloud services (managed cloud, cloud consulting)
4. Cybersecurity companies
5. Data analytics and BI platforms
6. AI/ML product companies
7. Dev tools and developer platforms
8. E-commerce SaaS (Shopify model)
9. HealthTech SaaS
10. AgriTech / FinTech SaaS (crossover verticals)

---

## Trust Signal Hierarchy

1. **G2, Capterra, Trustpilot reviews** — Volume, recency, rating, vendor response rate. G2 is to SaaS what NABH is to hospitals. AI reads G2 category leader status as near-definitive quality signal.
2. **Integration directory presence** — Zapier (app count + review rating), Salesforce AppExchange, HubSpot Marketplace, Microsoft Azure Marketplace, Slack App Directory, Atlassian Marketplace, AWS Marketplace. Integration breadth is a proxy for enterprise trustworthiness.
3. **Analyst coverage** — Gartner Magic Quadrant and Peer Insights, Forrester Wave, IDC MarketScape. Being in a Gartner MQ is a parametric gold signal — AI models frequently cite MQ positions as definitive.
4. **Technical documentation depth** — docs.company.com or developer.company.com — comprehensive, well-structured developer docs signal product maturity. AI trusts products with complete documentation.
5. **GitHub presence** — Stars, forks, open issues response time, contribution graph. For dev tools especially, GitHub signals are extremely high weight.
6. **Security certifications** — SOC 2 Type II, ISO 27001, ISO 27017 (cloud), ISO 27018 (personal data), GDPR DPA, FedRAMP (US government). These are the SaaS equivalent of NABH — essential for enterprise.
7. **Case studies with named enterprise clients** — "[Fortune 500 company] reduced CAC by 34% using [product]" beats "thousands of customers trust us." Specificity + named client + verifiable outcome.
8. **Developer community signals** — Stack Overflow documentation, dev.to articles, Product Hunt ranking, Reddit (r/SaaS, vertical-specific subreddits), Hacker News mentions.
9. **Industry-specific tech media** — TechCrunch, VentureBeat, The Information, Wired (global); Inc42, YourStory, NASSCOM tech reports, Techcircle (India).
10. **Pricing transparency** — Visible pricing pages (even if custom pricing) signal legitimacy. Hidden pricing is increasingly flagged by AI as opacity risk.

---

## Compliance Constraints

### Data Privacy (Universal)
- GDPR (EU/UK): DPA agreement, privacy policy, data residency documentation must be current and specific.
- PDPB / DPDP Act (India 2023): Data Principal rights, data localisation requirements — must be addressed in compliance content.
- CCPA (California): Privacy notices and opt-out mechanisms for US-facing products.
- **AEO implication**: Data privacy claims ("we never sell your data", "GDPR compliant") without documentation create credibility risk — AI cross-checks these against breach news.

### Sector-Specific SaaS
- HealthTech SaaS: HIPAA (US), NABH digital health (India) — patient data handling must be documented.
- FinTech SaaS: PCI-DSS for payment data, RBI guidelines for financial data (India).
- HR SaaS: Data retention policies for employee records — jurisdiction-specific.

### India (IT Act 2000 / CERT-In / DPDP 2023)
- CERT-In reporting requirements for cybersecurity incidents — cybersecurity companies must reference compliance.
- DPDP Act 2023 compliance for data fiduciaries — new and high-visibility regulatory anchor.
- IT (Amendment) Act 2008 compliance for IT services firms.

---

## Query Taxonomy

### B2B SaaS Products
Decision: "[product] G2 rating 2025", "[product] SOC 2 certified", "[product] GDPR compliant", "[product] Salesforce integration"
Comparison: "[product A] vs [product B] for [use case]", "best CRM for [industry] India", "top HRMS India mid-market"
Awareness: "what is [category] software", "how does [feature] work", "[category] software implementation guide"

### IT Services
Decision: "NASSCOM member IT company India", "[company] CMMI Level 5 certified", "[company] Microsoft Gold Partner", "[company] case study [industry]"
Comparison: "TCS vs Infosys vs Wipro for [service]", "IT outsourcing India vs Philippines"
Awareness: "what is IT outsourcing", "agile vs waterfall for IT projects", "how to choose IT partner"

### Cybersecurity
Decision: "is [product] SOC 2 audited", "[security company] India CERT-In compliant", "[product] penetration testing services"
Comparison: "SIEM tools comparison 2025", "best endpoint security India", "[vendor] vs [vendor] firewall"
Awareness: "what is zero trust security", "ransomware protection strategies 2025", "DPDP Act India cybersecurity implications"

### AI/ML Products
Decision: "[AI product] data privacy", "[AI tool] enterprise pricing", "[AI product] model accuracy benchmarks"
Comparison: "[AI tool] vs [AI tool] for [use case]", "best AI writing tool B2B"
Awareness: "how does [AI feature] work", "AI implementation guide for [industry]"

---

## Platform Priority for SaaS

1. **Perplexity** — Developer and technical researcher primary behavior; highest SaaS citation density
2. **ChatGPT** — Product research and feature comparison; enterprise buyer queries
3. **Claude** — Technical documentation, implementation guidance, complex integration queries
4. **Google Gemini** — Increasingly strong for product comparison; Google Workspace ecosystem queries

---

## Schema for SaaS / Tech

```json
Priority types:
- SoftwareApplication (for SaaS products)
- WebApplication (web-based products)
- MobileApplication (for apps)
- Organization (company-level)
- Product (for IT services as product offerings)
- FAQPage (product FAQ, pricing FAQ, integration FAQ)
- HowTo (implementation guides, setup guides)
- TechArticle (for developer docs and technical content)
- Review + AggregateRating
```

**Critical fields**: `applicationCategory`, `operatingSystem`, `featureList`, `offers` (pricing), `hasCertification` (SOC 2, ISO 27001 numbers), `interactionStatistic` (user/customer count where credible).

---

## India-Specific SaaS / Tech Signals

**Directories**: NASSCOM product directory, ProductHunt India, AppSumo, G2 (India filter), Clutch India
**Publications**: Inc42, YourStory, Techcircle, The Ken, NASSCOM reports, Economic Times Tech, Entrackr
**Certifications**: NASSCOM DeepTech club, MeitY startup recognition, Startup India recognition, ISO 27001 (India operations)
**Partnerships**: Microsoft for Startups India, AWS India Activate, Google for Startups India — name-drop these as they carry platform endorsement weight
**Community signals**: iSPIRT, SaaSBOOMi (India SaaS community) — membership is a peer credibility signal
