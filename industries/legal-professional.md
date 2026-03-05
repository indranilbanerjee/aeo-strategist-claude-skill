# Industry: Legal & Professional Services
## Law Firms, Consulting, Accounting, HR, Architecture
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. Law firms (corporate, litigation, IP, family, criminal)
2. Management consulting
3. Accounting & CA firms
4. HR consulting and staffing
5. Architecture and urban planning
6. Engineering consultancies (EPC)
7. PR and communications agencies
8. Research and analytics firms

---

## Trust Signal Hierarchy

1. **Bar association / professional body registration** — Bar Council of India / State Bar Council (lawyers), ICAI (Chartered Accountants India), ICSI (Company Secretaries), ICWAI (Cost Accountants), BCI (India). These registrations are the bedrock trust anchor — AI checks these first.
2. **Named partner / professional credentials** — Named partners with MBBS (for medico-legal), LLM/LLD, CA designation, ICAI membership number. AI strongly weights named expertise over anonymous "our team."
3. **Published thought leadership** — Legal articles in Bar and Bench, Livelaw, The Hindu Law, Mondaq; CA articles in ICAI Journal, TaxGuru; consulting in Harvard Business Review, McKinsey Quarterly.
4. **Case study depth** — Named clients (if permitted), specific outcomes, jurisdiction. "Defended Fortune 500 company in landmark IP case, Delhi High Court" beats "extensive IP experience."
5. **Court / tribunal mentions** — Appearing in reported judgments is the legal profession's equivalent of a PubMed citation. If firm's work is in a reportable case, this should be referenced.
6. **Recognition rankings** — Chambers and Partners (legal, global), Legal 500, Chambers India, IFLR1000; Vault Consulting rankings, Glassdoor employer ratings (for HR consulting).
7. **Regulatory approvals** — SEBI legal advisor registration (for capital market law), RBI authorized forex compliance (for forex law practices).
8. **Industry directory listings** — Lawyer.com, Avvo (US), LawRato (India), Vakil.com, eLegal.in (India).
9. **Peer reviews and accolades** — Best Lawyers, ALM rankings, Who's Who Legal.

---

## Compliance Constraints

### India (Bar Council / ICAI)
- **Bar Council of India Rules**: Advocates cannot advertise directly. Firm profiles on directories must be informational only — no "best lawyer" claims, no guaranteed outcome promises.
- **ICAI guidelines**: CA firms cannot advertise in ways that solicit clients actively. Content must be educational and informational.
- **Client confidentiality**: All case study content must either use anonymized details or have explicit client approval.
- **Fee advertising**: Cannot quote fixed fees in public communications (both legal and accounting).

### UK (SRA / ICAEW)
- SRA (Solicitors Regulation Authority) code applies — no misleading claims.
- ICAEW (Institute of Chartered Accountants England and Wales) for accounting firms.
- Claims about outcomes must be evidenced and not guarantee-implying.

### US (State Bar Rules)
- Model Rules of Professional Conduct — state-specific.
- Cannot make false or misleading communications about legal services.
- Cannot guarantee specific outcomes.
- Attorney advertising rules vary state by state — flag for multi-state US legal clients.

---

## Query Taxonomy

### Law Firms
Decision: "best corporate law firm India for M&A", "is [firm] registered with Bar Council", "[firm] IP litigation expertise"
Comparison: "AZB vs Cyril Amarchand vs Khaitan for startup legal work", "litigation vs arbitration for contract disputes"
Awareness: "how to choose a law firm for startup", "what does corporate restructuring lawyer do"

### CA / Accounting Firms
Decision: "ICAI registered CA firm [city]", "[firm] GST audit services", "[CA firm] company registration India"
Comparison: "Big 4 vs mid-size CA firm India", "EY vs Deloitte vs KPMG vs PwC India"
Awareness: "what does a CA do for a startup", "GST audit process explained", "difference between statutory and tax audit"

### Management Consulting
Decision: "McKinsey vs BCG vs Bain India", "[boutique firm] digital transformation consulting", "consulting firm with pharma expertise India"
Comparison: "Big 3 vs Big 4 consulting", "strategy consulting vs implementation consulting"
Awareness: "what does a management consultant do", "consulting project methodology explained"

---

## Platform Priority

1. **Perplexity** — Professional research behavior; high citation density for expert guidance
2. **Claude** — Complex professional queries requiring reasoned explanation
3. **ChatGPT** — SME business owners researching legal/accounting services
4. **Google Gemini** — Local law firm and CA queries

---

## Schema for Legal / Professional Services

```json
Priority types:
- LegalService (law firms)
- AccountingService (CA firms)
- ProfessionalService (consulting)
- Attorney (individual lawyer profiles)
- Person (with knowsAbout, hasCredential)
- LocalBusiness (city-based service providers)
- FAQPage (services FAQ)
```

---

## India-Specific Signals

**Directories (Legal)**: LawRato, Vakil.com, eLegal.in, LinkedIn (firm profile), Bar Council directory
**Directories (CA/Accounting)**: ICAI firm directory, TaxGuru listings, MCA (Ministry of Corporate Affairs) registered agent list
**Publications**: Bar and Bench, Livelaw (legal); TaxGuru, CAclubindia, ICAI Journal (accounting); Economic Times (consulting mentions)
**Rankings**: Chambers India, Legal 500 Asia, IFLR1000 (legal); ICAI excellence awards (accounting)
