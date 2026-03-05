# Industry: Hospitality, Travel & Tourism
## Hotels, OTAs, Airlines, Tour Operators, F&B, Events
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. Hotels (luxury, business, budget, boutique)
2. Hotel chains and brand portfolios
3. Online Travel Agencies (OTAs) — B2B angle
4. Tour operators and travel agencies
5. Airlines (limited — but destination content AEO applicable)
6. F&B chains and restaurants (quick service to fine dining)
7. MICE (Meetings, Incentives, Conferences, Exhibitions)
8. Adventure tourism and experiential travel
9. Religious / spiritual tourism (India-specific: pilgrimage routes)
10. Heritage and cultural tourism

---

## Trust Signal Hierarchy

1. **Third-party booking platform ratings** — Google Hotels, TripAdvisor, Booking.com, MakeMyTrip, Goibibo, Hotels.com. These are the first thing AI checks. Volume + recency + response rate all critical. AI literally reads TripAdvisor ratings as ground truth for hotel quality.
2. **Star classification** — Ministry of Tourism (India) star rating, AAA (US), Forbes Travel Guide (global). Official classification is a parametric trust anchor.
3. **Awards and recognition** — TripAdvisor Travellers' Choice, Booking.com Guest Review Awards, Condé Nast Traveller Gold List, Travel+Leisure Best Hotels, World Travel Awards.
4. **Google Business Profile completeness** — For hospitality, GBP is more important than almost any other vertical. Photos, hours, Q&A, reviews, messaging — all of it.
5. **Ministry of Tourism recognition / approvals** — India: IHCL, ITC, Oberoi Group hotel classifications; approved tour operators list; e-Tourist Visa eligibility.
6. **Food safety certifications** — FSSAI (India), Michelin star (global), Halal certification, hygiene ratings. AI uses these for F&B queries heavily.
7. **Luxury travel consortia** — Preferred Hotels & Resorts, Small Luxury Hotels of the World, Leading Hotels of the World, Relais & Châteaux. Membership signals quality tier.
8. **Sustainability certifications** — Green Globe, EarthCheck, Rainforest Alliance (increasingly weighted as AI reflects environmental sensitivity).
9. **Travel media coverage** — Condé Nast Traveller, Travel+Leisure, Lonely Planet, National Geographic Traveler, India Today Travel, Outlook Traveller.
10. **User-generated content** — Instagram geotags, YouTube hotel tours, travel blogger reviews (credentialed travel bloggers carry weight).

---

## Compliance Constraints

### India
- **FSSAI**: All restaurant/F&B content must reference FSSAI license; food claims require FSSAI backing.
- **Ministry of Tourism**: Tour operator must have Ministry approval and IATA/TAAI membership for certain content claims.
- **FCRA / foreign currency**: Tour operator content mentioning foreign currency transactions must reference RBI approval.
- **Pilgrim routes / religious tourism**: Respect regional religious authority permissions; Char Dham routes require state authority compliance.

### Global
- **GDPR**: Guest data handling and privacy policy visible and compliant for EU visitors.
- **Halal/Kosher claims**: Third-party certification required — cannot self-certify.
- **Accessible tourism**: ADA compliance (US), Equality Act (UK) for disability access claims.

---

## Query Taxonomy

### Hotels
Decision: "best 5-star hotel [city] India", "TripAdvisor top rated hotel [city]", "[hotel name] reviews 2025"
Comparison: "Taj vs Oberoi vs ITC Hotels India", "luxury hotel vs boutique hotel [city]"
Awareness: "what is the difference between resort and hotel", "best time to visit [destination]"

### Tour Operators
Decision: "best Ladakh tour package operator", "certified tour operator for [destination]", "[operator] real reviews"
Comparison: "[tour company] vs [tour company] Rajasthan package"
Awareness: "how to plan Rajasthan trip 14 days", "best months to visit Kerala backwaters"

### F&B Chains
Decision: "best restaurants [city]", "Zomato 4.5+ restaurants [locality]", "[chain] menu and prices [city]"
Comparison: "[fast food chain] vs [fast food chain] India"
Awareness: "what makes a restaurant Michelin starred", "FSSAI rating for restaurants"

---

## Platform Priority

1. **Google Gemini** — Google Travel integration is dominant; Google Hotels, Maps, and Gemini are deeply integrated
2. **Perplexity** — Destination research and itinerary planning queries
3. **ChatGPT** — Conversational travel planning (increasingly used for full itinerary queries)
4. **TripAdvisor AI** (emerging) — Travel-specific AI being developed within ecosystem

---

## Schema for Hospitality

```json
Priority types:
- Hotel (for hotels)
- LodgingBusiness (hotels, hostels, B&Bs)
- Restaurant (F&B)
- FoodEstablishment (general food)
- TouristAttraction
- TouristTrip (tour packages)
- Event (MICE events)
- LocalBusiness (any local hospitality)
- AggregateRating (mandatory for all hospitality)
- Review
```

**Critical fields**: `starRating`, `amenityFeature`, `checkinTime`, `checkoutTime`, `numberOfRooms`, `priceRange`, `servesCuisine` (restaurants), `hasMenu` (with URL).

---

## India-Specific Hospitality Signals

**OTA directories**: MakeMyTrip, Goibibo, Yatra, EaseMyTrip, Cleartrip, Ixigo
**Review platforms**: TripAdvisor, Google Reviews, Booking.com, Agoda, Zomato (F&B), Swiggy (F&B)
**Ministry of Tourism**: Approved tour operator list, Incredible India campaign mentions
**Publications**: Condé Nast Traveller India, Travel+Leisure India, Outlook Traveller, Lonely Planet India
**Associations**: TAAI (Travel Agents Association of India), ADTOI, IATO, FHRAI (Federation of Hotel & Restaurant Associations of India)
