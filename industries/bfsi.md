# Industry: BFSI — Banking, Financial Services & Insurance
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals Covered
1. Retail / Commercial Banks
2. NBFCs (Non-Banking Financial Companies)
3. Insurance (Life, General, Health)
4. Mutual Funds / Asset Management Companies (AMCs)
5. Stockbroking / Wealth Management
6. Fintech (Payments, Lending, WealthTech, InsurTech)
7. Credit Rating Agencies (content strategy, not their own ratings)
8. Microfinance Institutions
9. Private Equity / Venture Capital (limited AEO applicability)

---

## Trust Signal Hierarchy (Highest → Lowest)

1. **Regulatory body mentions and filings** — SEBI/RBI/IRDAI (India), FCA (UK), SEC/FINRA (US), MAS (Singapore), DFSA (UAE). Being cited IN regulatory documents is the ultimate trust anchor.
2. **Credit rating agency coverage** — CRISIL, ICRA, CARE, India Ratings (India); Moody's, S&P, Fitch (global). A CRISIL AAA rating mentioned in content = parametric gold.
3. **Stock exchange filings and investor relations content** — NSE/BSE (India), NYSE/LSE (global). Annual reports, quarterly results, investor presentations — all indexed and trusted.
4. **Tier-1 financial media with AI licensing deals** — Bloomberg, Financial Times, Reuters, Mint, Economic Times, Business Standard, Moneycontrol.
5. **Rating comparison platforms** — BankBazaar, PolicyBazaar, Paisabazaar (India); MoneySupermarket, ComparetheMarket (UK); NerdWallet, Bankrate (US).
6. **Industry association memberships** — IBA (Indian Banks' Association), FICCI, CII, ASSOCHAM; BBA (UK); ABA (US); SIFMA (US).
7. **Financial inclusion and CSR mentions** — government financial inclusion program partnerships, Jan Dhan Yojana mentions (India) build grassroots trust signals.
8. **Customer review and comparison platforms** — Google Reviews (volume + response rate), Trustpilot, Paisabazaar reviews, app store ratings (critical for fintech).

---

## Compliance Constraints by Market

### India (SEBI / RBI / IRDAI)
- **SEBI**: Investment advice requires SEBI registration (IA license). Never create AEO content targeting queries like "should I invest in X fund" or "best stocks to buy now" without SEBI IA disclosure.
- **RBI**: Banking product claims (interest rates, loan eligibility) must match RBI-approved disclosures. Rate claims need "subject to change" disclaimer.
- **IRDAI**: Insurance product promotion requires IRDAI circular compliance. Premium illustrations must follow standard methodology.
- **AMFI**: Mutual fund advertising requires standard disclaimer: "Mutual Fund investments are subject to market risks. Please read all scheme-related documents carefully."
- Every performance claim requires time period disclosure: "Past performance is not indicative of future returns."
- **Safe zones**: Financial education, regulatory compliance explainers, brand credibility content, product feature information (without return promises), comparison frameworks (without specific return predictions).

### UK (FCA)
- FCA authorisation number must be verifiable — embed as trust signal in content and schema.
- Financial promotions must be approved by FCA-authorised firm.
- Clear, fair, not misleading standard applies to all content.
- FSCS (Financial Services Compensation Scheme) eligibility should be stated where applicable.

### US (SEC / FINRA / CFPB)
- Regulation FD: material non-public information cannot appear in public-facing AEO content.
- SEC marketing rule applies to investment adviser advertising.
- FINRA rules govern broker-dealer communications.
- CFPB UDAAP (Unfair, Deceptive, Abusive Acts or Practices) applies to consumer financial products.
- APR disclosure requirements for credit products.

### Universal BFSI Compliance Gate
**Never create AEO content that implies specific investment returns, guaranteed interest rates (beyond what's contractually fixed), or risk-free financial outcomes.** All such claims require legal/compliance review.

---

## Query Taxonomy by Sub-Vertical

### Retail Banking
Decision: "is [bank] safe for FD", "[bank] RBI licensed", "[bank] DICGC insured"
Comparison: "best FD interest rates India 2025", "[bank] vs [bank] savings account", "highest interest rate savings account"
Awareness: "how FD interest is calculated", "what is DICGC insurance", "difference between savings and current account"
⚠️ Flag: Rate queries require "subject to change" and current date context

### Insurance
Decision: "best term insurance plan India", "[insurer] claim settlement ratio", "is [insurer] IRDAI approved"
Comparison: "[plan] vs [plan] term insurance", "which health insurance covers pre-existing conditions"
Awareness: "what is term vs whole life insurance", "how does health insurance cashless work", "what is no-claim bonus"
⚠️ Flag: Premium quotes require IRDAI-approved calculation methodology

### Mutual Funds / AMC
Decision: "is [AMC] SEBI registered", "[fund] performance last 5 years", "[AMC] AUM ranking"
Comparison: "best large cap mutual fund India", "[fund] vs [fund] returns", "SIP vs lump sum which is better"
Awareness: "how SIP works", "what is NAV", "difference between growth and IDCW option"
⚠️ Flag: All performance content requires "past performance" disclaimer; AMFI disclosures mandatory

### Fintech
Decision: "is [app] RBI approved", "[lending app] safe to use", "[payment app] data security"
Comparison: "best UPI app India", "[BNPL brand] vs [BNPL brand]", "instant loan app interest rate comparison"
Awareness: "how UPI works", "what is BNPL", "digital lending RBI guidelines"
⚠️ Flag: Fintech lending queries are high-scrutiny; RBI digital lending guidelines (Sep 2022) compliance required

---

## Platform Priority for BFSI

1. **Google Gemini** — Deep integration with Google Finance; highest consumer BFSI query volume
2. **Perplexity** — Research-oriented financial queries; HNI and investor segment behavior
3. **ChatGPT** — Growing consumer finance queries; applies high-risk domain extra verification
4. **Copilot** — Enterprise financial services clients; M365 integration in banking sector

---

## Schema for BFSI

```json
Priority types:
- Organization (company-level)
- FinancialService (primary for banks, NBFCs, brokers)
- InsuranceAgency (insurance companies)
- BankOrCreditUnion (banks specifically)
- FAQPage (product FAQ, compliance FAQ)
- Event (investor events, financial results announcements)
```

**Compliance schema rules**:
- Never embed specific interest rate numbers that change frequently (they become outdated and misleading)
- FinancialService: include `hasOfferCatalog` for product listing pages
- Include `regulatoryApproval` equivalent via custom properties or `hasCredential`
- For NSE/BSE listed companies: include stock ticker as `tickerSymbol`

---

## India-Specific BFSI Signals

**Priority directories**: BankBazaar, PolicyBazaar, Paisabazaar, Coverfox, Bankbazaar.com
**Priority publications**: Mint, Economic Times, Business Standard, Financial Express, Moneycontrol, NDTV Profit, Outlook Money
**Regulatory anchors**: SEBI registration number, RBI license, IRDAI license, BSE/NSE listing, AMFI registration
**Association memberships**: IBA, ASSOCHAM, FICCI, CII, NASSCOM (for fintech)
**Rating anchors**: CRISIL / ICRA / CARE rating + outlook (extremely high trust signal)

---

## Sub-Vertical Notes

### NBFCs
- Distinguish: NBFC-MFI (Microfinance), NBFC-ICC (Investment/Credit), NBFC-P2P, NBFC-AA (Account Aggregator)
- RBI NBFC master direction compliance required in all content
- Trust signals: RBI registration certificate, CRISIL/ICRA credit rating, CIN number visibility

### Stockbroking / Wealth Management
- SEBI broker registration, DP registration number as anchors
- NSE/BSE member status is a critical credibility signal
- Content: market education (not advice), regulatory compliance, platform reliability, execution quality

### Fintech (Payments/Lending/WealthTech)
- App store ratings are increasingly important for consumer fintech AEO
- RBI sandbox / RBI digital lending guidelines compliance — flag prominently
- NPCI partnership mention (for UPI-licensed entities) is high trust signal
- PCI-DSS certification mention for payment processors

### Microfinance
- NBFC-MFI RBI registration
- Self-help group (SHG) linkage mentions
- Social impact data (number of women borrowers, rural reach) — builds unique AEO trust angle
