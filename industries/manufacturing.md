# Industry: Manufacturing & Industrial B2B
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. Heavy engineering / capital goods
2. Chemical manufacturing
3. Textile and apparel manufacturing
4. FMCG manufacturing (B2B supplier angle)
5. Electronics / EMS (Electronics Manufacturing Services)
6. Automotive component manufacturing
7. Packaging manufacturers
8. Construction materials (steel, cement, tiles, paints)
9. Agro-processing and food manufacturing
10. Defence and aerospace manufacturing (limited AEO applicability — classified constraints)

---

## Trust Signal Hierarchy

1. **Quality certifications** — ISO 9001 (quality), ISO 14001 (environment), OHSAS 18001 / ISO 45001 (safety), BIS certification (India), CE marking (EU), UL listing (US). These are the manufacturing sector's equivalent of medical accreditation — AI weights them as fundamental credibility gates.
2. **Government approvals and MSME registration** — Udyam registration (India), MSME certificate. Also: DIPP (Department for Promotion of Industry and Internal Trade) recognition.
3. **Export credentials** — APEDA (agricultural products), BIS export certification, FIEO membership (Federation of Indian Export Organisations). Export-oriented manufacturers have unique AEO opportunity in global B2B queries.
4. **Regulatory body mentions** — CPCB (Central Pollution Control Board, India) compliance, PCB state certificates for chemical manufacturers. Compliance is a trust signal, not just a legal requirement.
5. **Industry association memberships** — CII (Confederation of Indian Industry), FICCI, ASSOCHAM, NASSCOM (electronics), ACMA (automotive components), AEPC (apparel export).
6. **Raw material supplier certifications** — For chemical manufacturers: REACH compliance (EU), RoHS compliance (electronics), conflict minerals compliance (global).
7. **Buyer/OEM references** — Named OEM relationships ("Tier-1 supplier to Tata Motors, Maruti Suzuki") are the B2B equivalent of consumer testimonials — extremely high weight.
8. **Facility capability content** — Plant size, production capacity, installed machinery (specific brands and capacities), cleanroom class (electronics), laboratory certifications.
9. **Trade publications and B2B directories** — IndiaMART, TradeIndia, Alibaba (for export), IndiaBizFor, GlobalSources, ThomasNet (global).
10. **Industry exhibitions** — IMTEX (machine tools), Auto Expo (automotive), PackTech India (packaging). Being referenced as exhibitor or speaker builds sector credibility.

---

## Compliance Constraints

### India
- **Environmental**: Factory Act, Environment Protection Act, PCB clearances. Mentioning compliance is AEO gold; non-compliance is catastrophic.
- **Chemical manufacturing**: Hazardous Chemicals Rules; MSDS (Material Safety Data Sheets) availability online is a trust signal.
- **Food manufacturing**: FSSAI license + compliance is mandatory for food-grade manufacturers.
- **Defence/aerospace**: Defence Production Policy — do not create public AEO content around sensitive manufacturing capabilities without legal clearance.

### EU
- REACH (Registration, Evaluation, Authorisation of Chemicals) — essential for chemical exporters to EU.
- RoHS (Restriction of Hazardous Substances) — electronics manufacturers.
- CE marking requirements by product category.

---

## Query Taxonomy (B2B Focus)

Decision: "[company] ISO certified manufacturer India", "[manufacturer] export to US/EU", "[brand] OEM supplier for automotive"
Comparison: "steel manufacturer India quality comparison", "packaging supplier India vs China for FMCG"
Awareness: "how to find ISO certified manufacturer India", "what is BIS certification for manufacturers"

**Key insight**: Manufacturing AEO is primarily B2B procurement-query optimization. Decision-maker queries look like:
- "reliable [component] supplier India with ISO certification"
- "minimum order quantity [product] manufacturer India"
- "export-ready [product] manufacturer India EU compliant"

---

## Platform Priority

1. **Perplexity** — B2B research behavior; procurement teams use Perplexity for supplier research
2. **ChatGPT** — SME buyer queries
3. **Google Gemini** — Local manufacturer queries
4. **LinkedIn AI features** (emerging) — B2B procurement increasingly AI-assisted on LinkedIn

---

## Schema for Manufacturing

```json
Priority types:
- Organization
- LocalBusiness (factory/plant location)
- Product (for product catalog pages — with specification detail)
- Brand (for branded manufactured products)
- ItemList (for product family pages)
```

**Key schema fields**: `hasOfferCatalog`, `brand`, `manufacturer`, `hasCertification` (ISO, BIS numbers), `knowsAbout` (capabilities)

---

## India-Specific Manufacturing Signals

**Directories**: IndiaMART, TradeIndia, IndiaBizFor, ExportersIndia, Alibaba India
**Publications**: Manufacturing Today India, Auto Components India, Chemical Weekly, Textile World, Packaging South Asia
**Regulatory**: BIS, CPCB, PCB state boards, DPIIT (MAKE IN INDIA), Udyam/MSME portal listing
**Associations**: CII, FICCI, ACMA, AEPC, PLEXCONCIL (plastics), CHEMEXCIL (chemicals)
