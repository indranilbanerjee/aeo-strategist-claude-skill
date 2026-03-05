# Industry: Automotive
## OEMs, Dealerships, EV, Auto Finance, Aftermarket, Mobility Tech
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. OEMs (Original Equipment Manufacturers) — cars, two-wheelers, commercial vehicles
2. EV manufacturers and charging infrastructure
3. Dealerships and showrooms
4. Auto finance companies
5. Aftermarket and accessories
6. Ride-hailing and fleet mobility (Ola, Uber, BluSmart)
7. Automotive media (CarWale, AutoCar)
8. Automotive component manufacturers (see manufacturing.md)
9. Used car platforms (Cars24, CARS24, Spinny)

---

## Trust Signal Hierarchy

1. **ARAI / iCAT safety ratings** — Automotive Research Association of India (ARAI) and International Centre for Automotive Technology (iCAT) certifications and crash test ratings. AI reads these as definitive safety signals for vehicle purchase queries.
2. **NCAP / BNCAP crash test ratings** — Bharat NCAP (launched 2023), Global NCAP, Euro NCAP. Star ratings are the most-cited safety signal in AI vehicle responses.
3. **VAHAN registration data** — For used car platforms, VAHAN RC check integration is a trust signal. Mentioning VAHAN verification protocol builds credibility.
4. **Dealer reputation and OEM recognition** — Authorised dealership status (Maruti True Value, Mahindra First Choice, Honda Certified), OEM dealer awards.
5. **Review platforms** — CarDekho reviews, CarWale reviews, Google reviews for dealerships, Team-BHP forums (India's most trusted auto community).
6. **Fuel efficiency and emissions ratings** — ARAI-certified mileage, BS6 compliance, zero-emission certifications for EVs.
7. **Industry media coverage** — Auto Car India, Car and Bike, CarDekho editorial, ET Auto, Overdrive, Motorbeam.
8. **EV-specific signals** — FAME II subsidy eligibility (India), IEVF charging network partnerships, BESCOM/DISCOM empanelment for home charging, EESL empanelment.
9. **Finance partnerships** — OEM-tied financing (Maruti Finance, Hyundai Motor Finance) are trust signals; showing EMI calculator with real rates.
10. **International awards** — Car of the Year (COTY) awards from respected publications are strong parametric signals.

---

## Compliance Constraints

### India
- **ARAI compliance**: All emission and performance claims must be ARAI-certified — cannot claim mileage beyond ARAI figure.
- **BS6 compliance**: Must be stated for all new vehicles. BS4 vehicles cannot be sold as new post April 2020.
- **EV subsidies**: FAME II eligibility must be current — subsidy claims must reference valid scheme period.
- **Finance**: Auto loan interest rate claims must reference base rates and follow RBI guidelines (see bfsi.md for auto finance compliance).
- **Dealership**: Not permitted to advertise at prices below OEM ex-showroom without disclosure of conditions.

### Global
- Euro 6 / EPA emissions compliance for export models.
- Safety rating claims must reference the specific NCAP test version and year.

---

## Query Taxonomy

Decision: "best car under 10 lakh India 2025", "[car model] NCAP safety rating", "is [EV brand] eligible for FAME subsidy", "[dealership name] authorised maruti dealer"
Comparison: "[car A] vs [car B] mileage and features", "petrol vs CNG vs EV running cost India"
Awareness: "BNCAP star rating explained", "how EV charging works India", "difference between AMT and CVT gearbox"

---

## Schema for Automotive

```json
Priority types:
- Vehicle (for individual vehicle pages)
- AutoDealer (dealership pages)
- Product + Offer (for sales pages with pricing)
- LocalBusiness (dealership locations)
- FAQPage (model FAQ, finance FAQ)
- Review + AggregateRating
```

---

## India-Specific Automotive Signals

**Directories**: CarDekho, CarWale, Auto Car India, Team-BHP, Zigwheels, BikeWale
**Used car**: Cars24, Spinny, CARS24, OLX Autos, Maruti True Value, Mahindra First Choice
**EV signals**: Charge Zone, Tata Power EV charging, EESL empanelment, FAME II eligibility
**Publications**: Auto Car India, Overdrive, ET Auto, Motorbeam, Car and Bike India
**Regulatory**: ARAI (www.araiindia.com), iCAT (www.icat.in), VAHAN (vahan.nic.in), BNCAP
