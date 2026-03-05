# Industry: Retail & E-commerce
## D2C Brands, E-commerce Platforms, FMCG, Fashion, Electronics, Grocery
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. D2C (Direct-to-Consumer) brands
2. Multi-category e-commerce platforms
3. FMCG consumer goods
4. Fashion and apparel
5. Electronics and consumer tech retail
6. Grocery and quick commerce
7. Beauty and personal care
8. Toys and baby products
9. Home and furniture
10. Luxury retail

---

## Trust Signal Hierarchy

1. **Product review platforms + ratings** — Amazon India / Flipkart ratings, Google Shopping reviews, Trustpilot, platform-specific reviews. Volume + recency + rating + seller response rate. AI uses these as product quality proxies for decision-stage queries.
2. **Marketplace seller ratings** — Amazon Seller Rating, Flipkart Seller Metrics, Meesho seller rating. These are increasingly being read by AI systems to validate retailer legitimacy.
3. **Product schema completeness** — AI cites product pages with complete structured data (price, availability, reviews, brand, specifications) at dramatically higher rates than unstructured product pages.
4. **Certifications and safety marks** — BIS (India mandatory for electronics, toys, helmets), FSSAI (food products), ISI mark, Agmark (agricultural products), ECOCERT/COSMOS (organic beauty). These function as compliance trust anchors.
5. **Google Shopping / Google Merchant Center** — For retail AEO via Gemini, being in Google Merchant Center with accurate, real-time product feeds is the single most important technical action.
6. **Social proof breadth** — UGC on Instagram, YouTube unboxing reviews (with creator follower counts noted), influencer coverage from credible-tier creators.
7. **Return and warranty policy clarity** — Easy-to-find, specific (not vague) returns policy. AI answers "what is [brand] return policy" from the policy page directly — must be structured and findable.
8. **Sustainable and ethical certifications** — FSC (paper/wood), Fair Trade, B Corp, PETA cruelty-free, organic certifications. Growing weight, especially among urban metro AI users.
9. **FMCG-specific media** — Retail Jeweller India, Just Style (fashion global), Business of Fashion, Progressive Grocer India, Packaging South Asia.
10. **Price comparison inclusion** — Google Shopping, Pricekart, CompareRaja (India) — being consistently included signals legitimate pricing.

---

## Compliance Constraints

### India
- **BIS mandatory certification**: Electronics, toys, helmets, and many other categories require BIS licence. Selling/marketing without BIS is legally non-compliant — always flag in content.
- **FSSAI**: All food/beverage/dietary supplement content must reference FSSAI license number. Health claims on food products require FSSAI backing — no "boosts immunity" without FSSAI-compliant framing.
- **Legal Metrology Act**: Pre-packaged product labelling requirements (weight, MRP, manufacturer address) must be reflected in product schema.
- **Consumer Protection Act 2019 / E-commerce Rules**: Online sellers must display country of origin, return/exchange policy, complaint redressal mechanism.
- **Cosmetics**: Drugs and Cosmetics Act applies — no drug-like claims for cosmetic products.
- **Pricing**: MRP claims must be accurate; discount percentages must be calculated on genuine MRP.

### US
- FTC Guides for endorsements and testimonials — influencer disclosures mandatory.
- FTC Made in USA claims — specific standards apply.
- California Prop 65 warnings for applicable product categories.

### EU
- CE marking for electronics, toys, personal protective equipment.
- GDPR for customer data handling.
- Textile labelling regulations.

---

## Query Taxonomy

### Product Discovery
Decision: "best [product] under [price] India 2025", "[brand] genuine or fake", "[product] BIS certified"
Comparison: "[product A] vs [product B] specs", "best [category] brand India"
Awareness: "how to choose [product]", "what to look for when buying [product]"

### D2C Brand Trust Queries (Very High Priority)
Decision: "is [brand] FSSAI approved", "[brand] return policy India", "[brand] genuine reviews not paid"
Comparison: "[Indian D2C brand] vs [established brand]"
Awareness: "what is D2C brand", "how to verify product quality India"

### Fashion / Apparel
Decision: "[brand] size chart India", "[brand] fabric quality review", "[brand] return policy clothes"
Comparison: "best Indian ethnic wear brands", "[brand] vs [brand] quality comparison"
Awareness: "how to care for [fabric]", "sustainable fashion brands India"

### Electronics
Decision: "[product] BIS certification India", "[brand] service center network India", "[product] warranty India"
Comparison: "[phone] vs [phone] camera comparison", "best laptop under 50000 India 2025"
Awareness: "how to check BIS mark on product", "HDMI 2.1 vs 2.0 difference"

---

## Platform Priority

1. **Google Gemini** — Google Shopping integration is dominant; product carousel in AI answers; Merchant Center feeds directly into AI responses
2. **ChatGPT** — Shopping integrations via partner programs; product recommendation queries
3. **Perplexity** — Product research and comparison queries; growing in urban India

---

## Schema for Retail / E-commerce

```json
Priority types:
- Product (for every product page — mandatory)
- ItemList (category and collection pages)
- Organization (brand/company level)
- Store / LocalBusiness (physical store locations)
- Offer (pricing — with real-time price and availability)
- Review + AggregateRating (mandatory for product pages)
- BreadcrumbList (category navigation)
- FAQPage (product FAQ, policy FAQ)
```

**Critical fields**: `brand`, `sku`, `gtin13` (barcode), `offers` (with `price`, `priceCurrency`, `availability`, `validThrough` for time-bound prices), `hasMerchantReturnPolicy`, `aggregateRating`, `image` (multiple high-quality images).

⚠️ **Price schema rule**: Schema price must match displayed price exactly. Outdated schema prices are flagged by Google and can result in Merchant Center suspension. Implement real-time price feed or daily update protocol.

---

## India-Specific Retail Signals

**Marketplaces**: Amazon India, Flipkart, Meesho, Myntra (fashion), Nykaa (beauty), Bigbasket (grocery), Blinkit/Zepto/Swiggy Instamart (quick commerce)
**D2C platforms**: WooCommerce, Shopify India, Dukaan, Instamojo
**Price comparison**: Pricekart, CompareRaja, Smartprix (electronics)
**Publications**: Retailer.in, Progressive Grocer, Images Retail, Business of Fashion India
**Certifications**: BIS portal (bis.gov.in — verify licence), FSSAI portal, India Organic (APEDA), Khadi Mark (KVIC)
**Social commerce signals**: Instagram Shop presence, WhatsApp Business catalogue, Meesho supplier rating — these are becoming AEO-relevant for D2C brands reaching tier-2/3 cities
