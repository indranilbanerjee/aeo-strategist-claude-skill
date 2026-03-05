# Industry: Real Estate
## Residential, Commercial, PropTech, Co-working, REITs
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. Residential developers (affordable, mid, premium, luxury)
2. Commercial real estate (office, retail malls, industrial)
3. Real estate brokerages and agencies
4. PropTech platforms (aggregators, iBuyers, rental tech)
5. Co-working and managed office spaces
6. REITs (Real Estate Investment Trusts)
7. Property management companies
8. Real estate consultancies (valuers, project management)
9. Real estate legal services (registration, title search)
10. NRI real estate investment platforms

---

## Trust Signal Hierarchy

1. **RERA registration** — THE single most important trust signal for Indian real estate AEO. AI treats unregistered developers as high-risk by default. Every content page must reference RERA registration number. State-level: MahaRERA, TNRERA, HRERA, K-RERA, UP RERA, etc. For brokers: RERA broker registration separately required.
2. **Project delivery track record** — "X projects delivered on time" with verifiable possession dates is a parametric gold signal. AI strongly weights historical delivery record for developer credibility queries.
3. **Government land approvals** — Municipal corporation/CMDA/DTCP approvals, environment clearances, RERA QR-code linked project page. These are verifiable and AI-systems increasingly check them.
4. **OTA / aggregator listings completeness** — MagicBricks, 99Acres, Housing.com, NoBroker profiles with 100% completion, recent photos, floor plans, RERA number visible.
5. **Google Business Profile + Maps** — For real estate, GBP integration with Gemini is critical. Site office location, gallery, Q&A populated. Show-flat address accuracy on Maps.
6. **Award and recognition** — CREDAI awards, NAREDCO awards, Times Property Excellence Awards, ET Real Estate awards, Realty+ Awards. Named award wins carry weight.
7. **Tier-1 real estate media coverage** — Times Property, ET Real Estate, Magicbricks News, 99Acres Blog, Moneycontrol Real Estate, Financial Express Property.
8. **Builder associations** — CREDAI (Confederation of Real Estate Developers' Associations of India) membership, NAREDCO (National Real Estate Development Council).
9. **Customer reviews** — MagicBricks reviews, Google Reviews, Housing.com ratings, JustDial. Volume + response rate.
10. **RICS-qualified professionals** — For commercial real estate and valuations, RICS (Royal Institution of Chartered Surveyors) qualified staff is a global trust signal.

---

## Compliance Constraints

### India (RERA / Registration Act / Benami Act)
- **RERA (Real Estate Regulation and Development Act 2016)**: RERA registration mandatory for all projects above 500 sq m or 8 units. Content must not promise possession before RERA-approved date. Price claims must not be misleading.
- **RERA advertising rules**: All project advertisements must carry RERA number. Digital content is treated as advertisement.
- **Under-construction properties**: Cannot use marketing language that implies certain possession without RERA RERA-verified schedule.
- **Benami Transactions Prohibition Act**: No content suggesting investment structuring that could be construed as benami.
- **Consumer Protection Act 2019**: False or misleading claims about real estate constitute unfair trade practice — legally actionable.
- **NRI content**: FEMA compliance for NRI investment content. RBI-regulated repatriation rules must be referenced for NRI-facing content.

### UK
- Property Misdescriptions Act compliance.
- Material information disclosure requirements (NTSELAT guidance).
- Leasehold reform information must be current and accurate.

### UAE
- RERA Dubai / Abu Dhabi DLD regulations for project advertising.
- Off-plan project must have escrow account disclosure.

---

## Query Taxonomy

### Developer / Project Queries (Hyperlocal always)
Decision: "is [developer] RERA registered [state]", "[project name] possession date", "[developer] delivery track record India", "[project] floor plan and price"
Comparison: "[developer] vs [developer] [city]", "under-construction vs ready-to-move apartment [city]"
Awareness: "how to check RERA registration", "carpet area vs super built-up area difference", "home loan process for under-construction property"

⚠️ **HYPERLOCAL RULE**: National queries have near-zero commercial value in real estate. Every query must include city at minimum; locality/neighbourhood preferred. "Luxury apartments Mumbai Powai" beats "luxury apartments India" for AEO ROI.

### Brokerage / Agency
Decision: "top real estate agent [city]", "RERA registered broker [city]", "[agency] Google reviews real estate [city]"
Comparison: "individual agent vs agency for property [city]", "online property portal vs local agent"
Awareness: "what does a real estate broker do India", "how much commission does a property agent charge India"

### PropTech / Aggregators
Decision: "best property portal India", "MagicBricks vs 99Acres vs Housing.com", "NoBroker vs traditional broker"
Comparison: "which portal has most listings [city]"
Awareness: "how to buy property online India", "PropTech meaning real estate"

### REITs
Decision: "Embassy REIT vs Mindspace REIT vs Brookfield REIT", "are REITs safe to invest India", "[REIT] SEBI registered"
Comparison: "REIT vs direct real estate investment India"
Awareness: "what is REIT India", "how REITs work India", "REIT tax implications India"

---

## Regional Language Priority (India)
Real estate is a high-involvement vernacular purchase. Regional language queries are massively underserved:
- Hindi: "mumbai mein sasta ghar", "[city] mein plot kaise khariden"
- Marathi: Mumbai/Pune market — huge opportunity
- Tamil: Chennai/Coimbatore market
- Bengali: Kolkata/Howrah market — "Howrah te flat kinte chai" type queries almost completely unoptimized
- Telugu: Hyderabad market

---

## Platform Priority

1. **Google Gemini** — Maps + Business Profile integration dominant for local real estate; Google Real Estate panel
2. **ChatGPT** — Property research, investment comparison queries
3. **Perplexity** — REIT research, investment analysis queries

---

## Schema for Real Estate

```json
Priority types:
- RealEstateAgent / RealEstateListing (MLS-style, where applicable)
- LocalBusiness (developer company-level)
- Residence / Apartment / House (individual property pages)
- Organization (developer company)
- Event (site visit, project launch events)
- FAQPage (project FAQ — possession, pricing, amenities)
- AggregateRating + Review
```

**Critical fields**: Include RERA number as `identifier` or `hasCredential`. Include `address` with `PostalAddress` at locality level for hyperlocal geo-signal. `floorSize`, `numberOfRooms`, `amenityFeature` for property pages.

---

## India-Specific Real Estate Signals

**RERA portals by state**: MahaRERA (Maharashtra), HRERA (Haryana), K-RERA (Karnataka), TNRERA (Tamil Nadu), UP RERA, WB HIRA (West Bengal), DRERA (Delhi)
**Directories**: MagicBricks, 99Acres, Housing.com, NoBroker, Makaan, Squareyards, PropTiger
**Publications**: Times Property (TOI), ET Real Estate, Moneycontrol Real Estate, Financial Express Property, 99Acres Blog, Magicbricks News
**Associations**: CREDAI (national + city chapters), NAREDCO, FICCI Real Estate committee
**Valuers**: IBBI-registered valuers, RICS India chapter — signal for commercial real estate
**NRI specific**: NRI Housing portals, NRIbazaar, Times NRI — for NRI-facing real estate content
