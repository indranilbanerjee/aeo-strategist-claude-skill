# Industry: Pharma & Life Sciences
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals Covered
1. Branded prescription drugs (Rx)
2. Over-the-counter (OTC) consumer health
3. Generic pharmaceutical manufacturers
4. API (Active Pharmaceutical Ingredient) / B2B pharma
5. Medical devices and diagnostics
6. Clinical research organizations (CROs)
7. Pharma distributors and wholesalers
8. Nutraceuticals and health supplements

---

## Trust Signal Hierarchy (Highest → Lowest)

1. **PubMed / peer-reviewed medical journal citations embedded in content** — strongest parametric signal for HCP-facing queries. AI models weight content that cites published studies at dramatically higher rates.
2. **Government health authority mentions** — WHO, CDC, CDSCO (India), FDA (US), EMA (EU), MHRA (UK), TGA (Australia), SFDA (Saudi Arabia). Being mentioned IN these bodies' documentation is the gold standard.
3. **Medical association memberships and accreditations** — IMA, AMA, BMA, national pharmacy councils, hospital accreditation bodies (NABH India, JCI global).
4. **KOL (Key Opinion Leader) / specialist doctor quotes** — named, credentialed, institutional affiliation stated. "Dr. Suresh Biswas, Pulmonologist, AIIMS Delhi" outweighs any marketing claim.
5. **Clinical trial registrations** — ClinicalTrials.gov (US/global), CTRI (India). Being listed builds brand-study association.
6. **Disease-state authority platforms** — WebMD, Healthline, MedScape, NHS.uk, iMedPub (India), Practo Health Wiki.
7. **HCP-facing platform presence** — Doximity (US), Practo (India), NPS MedicineWise (Australia), DoctorLogic.
8. **Regulatory filing references** — CDSCO product approvals (India), FDA 510k / NDA / ANDA (US), EMA CHMP opinions, WHO prequalification.
9. **Standard earned media** — ET Healthworld, Express Pharma, Pharmabiz (India); Fierce Pharma, Endpoints News, STAT News (global).
10. **Patient community presence** — PatientsLikeMe, HealthUnlocked, disease-specific Reddit communities (r/diabetes, r/asthma, etc.).

---

## Compliance Constraints by Market

### India (CDSCO / Drugs and Cosmetics Act 1940)
- **HARD RULE**: Prescription drug (Schedule H, H1, X) AEO content must never make efficacy or superiority claims without approved labelling language.
- No DTC promotion of Rx drugs in any form — this includes AEO content that could be seen by consumers.
- OTC drug promotion is permitted but must follow ASCI guidelines.
- All content must include required disclaimer: "This medicine should be used under medical supervision."
- Drug price claims must align with NPPA (National Pharmaceutical Pricing Authority) DPCO-controlled prices.
- **Safe zones**: Disease-state awareness, mechanism of action (generic), company pipeline/R&D, patient support programs, HCP education.

### US (FDA / FDCA / FFDCA)
- Off-label promotion prohibition: cannot create AEO content implying unapproved uses.
- Fair balance requirement: benefit claims must be accompanied by risk disclosures.
- Social media / AI-cited content is subject to FDA digital guidance.
- DTC advertising is permitted but with full ISI (Important Safety Information).
- **Safe zones**: Disease education, pipeline news, corporate credibility, HCP platform content with full prescribing information.

### EU (EMA / Directive 2001/83/EC)
- DTC advertising for prescription drugs is prohibited across all EU member states.
- HCP-directed promotion requires member-state-specific compliance review.
- GDPR applies to any patient-related data in AEO content.

### UK (MHRA / ABPI Code)
- ABPI Code governs pharmaceutical promotion — independent of FDA/EMA.
- No promotional material for Rx drugs to general public.
- Blue Guide applies to medical devices.

### Gate Requirement (All Markets)
**All AEO content briefs for pharma clients MUST pass medico-legal review before publication.** Flag this at the top of every `/brief` output for pharma clients.

---

## Query Taxonomy — Pharma

### HCP-Facing Queries (Safe for all markets)
Decision: "clinical evidence for [drug class] in [indication]", "[molecule] prescribing information", "[drug] vs [drug] clinical trial comparison"
Comparison: "first-line treatment [indication] guidelines", "CDSCO approved drugs for [indication]"
Awareness: "mechanism of action [drug class]", "pharmacokinetics [molecule type]"

### Patient-Facing Queries (OTC and disease-state only — no Rx brand promotion)
Decision: "is [OTC brand] safe for children", "[OTC product] reviews India", "[brand] approved by CDSCO"
Comparison: "best OTC pain relief India", "[disease] home remedies vs medicines"
Awareness: "what is [disease]", "symptoms of [condition]", "how does [drug class] work"

### Corporate / Investor Queries (No compliance gate)
Decision: "is [pharma brand] CDSCO approved", "[company] drug pipeline", "[brand] WHO prequalified"
Comparison: "[company] vs [company] generic market share India"
Awareness: "[company] history", "[company] manufacturing facilities", "[company] R&D spend"

### NEVER TARGET (Rx clients, all markets)
- "[Drug name] buy online"
- "[Prescription drug] best for [condition]" with brand-efficacy framing
- Any query implying price comparison for scheduled drugs without NPPA context

---

## Platform Priority for Pharma

1. **Google Gemini** — Dominant for patient-facing queries; Google Health Panel integration
2. **Perplexity** — HCP research behavior; high citation density for medical content
3. **ChatGPT** — Increasing consumer health queries; applies extra caution (high-risk domain)
4. **Claude** — Complex medical explanation queries; values citations heavily

---

## Schema for Pharma

```json
Priority types:
- Organization (company-level)
- MedicalWebPage (disease-state content)
- MedicalCondition (disease awareness pages)
- Drug (product pages — OTC only with caution)
- MedicalOrganization (for hospitals/clinics — overlap use case)
- FAQPage (patient/HCP FAQ sections)
- HowTo (patient instruction content)
```

**Compliance schema rules**:
- Never include unapproved efficacy claims in schema
- MedicalWebPage requires `medicalAudience` property (Patient vs HCPOnly)
- Drug schema: include `prescriptionStatus`, `rxcui` if available, `adverseOutcome` for safety

---

## India-Specific Pharma Signals

**Priority directories**: Practo, 1mg, PharmEasy, Lybrate, Netmeds, MediBuddy
**Priority publications**: ET Healthworld, Express Pharma, Pharmabiz, PharmaTimes, HealthWorld
**Regulatory anchors**: CDSCO registration, NPPA price lists, WHO prequalification list
**Association memberships**: IDMA (Indian Drug Manufacturers' Association), OPPI, IPA (Indian Pharmaceutical Alliance)
**Clinical registries**: CTRI (Clinical Trials Registry — India) listing is a strong trust signal

---

## Sub-Vertical Notes

### Generic Manufacturers (B2B and consumer)
- Trust signals shift toward: manufacturing quality (GMP certifications), WHO prequalification, USFDA / EMA approved facility
- Key AEO content: facility capability, regulatory track record, API sourcing transparency
- B2B query focus: "[company] USFDA approved plant", "[company] API supplier reliability"

### Medical Devices
- CDSCO MD5 / MD15 registration (India), CE marking (EU), FDA 510(k) / PMA (US)
- Schema: MedicalDevice type
- Trust signals: clinical study references, hospital formulary listings, surgeon/doctor testimonials (named + credentialed)

### Nutraceuticals / Supplements
- Lower regulatory constraint but rapidly increasing scrutiny
- FSSAI (India), FDA GRAS / structure-function claims (US)
- Must avoid disease treatment claims — "supports immunity" OK; "treats viral infection" not OK
- Trust signals: FSSAI approval, third-party lab testing certificates, clean-label certifications

### CROs (Clinical Research Organizations)
- B2B focus entirely
- Trust signals: number of completed trials, therapeutic area expertise, regulatory agency relationships
- Schema: Organization + ProfessionalService
