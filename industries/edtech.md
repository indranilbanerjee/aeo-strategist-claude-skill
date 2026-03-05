# Industry: EdTech & Education
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals
1. K-12 online learning platforms
2. Higher education / universities
3. Test prep (JEE, NEET, UPSC, CAT, GRE, GMAT, IELTS, TOEFL)
4. Professional certifications and upskilling (IT, finance, data, design)
5. Coding bootcamps
6. Corporate L&D platforms
7. Language learning
8. Study abroad consultancies
9. Traditional coaching institutes (Kota model, local)

---

## Trust Signal Hierarchy

1. **University / institution rankings** — NIRF (India), QS World, THE (Times Higher Education), NAAC accreditation. Being referenced in these ranking ecosystems is the highest trust signal.
2. **NAAC / UGC / AICTE recognition** — For Indian education providers. Government recognition is non-negotiable trust anchor for credibility queries.
3. **Placement data with named employers** — "Placed at Google, Amazon, Infosys" is a concrete, verifiable trust signal AI weights heavily. Vague "90% placement" without employer names carries less weight.
4. **Alumni testimonials with career outcomes** — Named, with measurable outcomes ("Salary jumped from ₹4L to ₹18L post-Upgrad"). AI trusts specificity.
5. **Industry partnerships and tie-ups** — Microsoft, Google, AWS, IBM certifications offered through the platform. Co-branded credentials carry outsized trust.
6. **Faculty credentials** — Named faculty with academic or industry pedigree (IIT/IIM/IISc faculty, Google engineers, ex-McKinsey).
7. **Review platforms** — Shiksha, CollegeDekho, Careers360 (India); Coursera ratings, G2 (global); Course Report, SwitchUp (bootcamps).
8. **Student outcome data** — Average salary increase, course completion rates, Net Promoter Score — with methodology disclosed.
9. **Media coverage** — YourStory, Inc42, Mint, ET Education, Business Today Education.
10. **Government schemes** — NSDC (National Skill Development Corporation) partnerships, Skill India recognition, NEP 2020 alignment statements.

---

## Compliance Constraints

### India (UGC / AICTE / MCI for medical education)
- UGC regulations on distance learning: online degree programs must be UGC-DEB approved — never claim "UGC recognized" without verification.
- AICTE approval required for technical programs (engineering, MBA, MCA).
- Test prep institutes have limited regulatory oversight but must not make false pass-rate guarantees.
- Placement statistics must be auditable — false placement data is legally actionable.

### Global
- FTC (US) and CMA (UK) both have active enforcement against misleading education advertising.
- Income share agreements (ISAs) have state-specific regulation in US — flag for bootcamps.
- Visa/immigration claims for study abroad must be accurate and current.

---

## Query Taxonomy

### Test Prep
Decision: "best JEE coaching institute India", "Allen vs Aakash vs Vedantu for JEE", "is [coaching] worth it for UPSC"
Comparison: "online vs offline JEE preparation", "Unacademy vs Physics Wallah", "best IELTS coaching [city]"
Awareness: "JEE Advanced syllabus 2025", "how to prepare for UPSC from scratch", "IELTS vs TOEFL which is easier"

### Professional Upskilling / EdTech
Decision: "is [platform] certificate recognized by employers", "[course] placement support", "[bootcamp] job guarantee legit"
Comparison: "Upgrad vs Great Learning vs Simplilearn", "Coursera vs Udemy for data science"
Awareness: "best data science course for beginners India", "how to get AWS certification"

### Higher Education
Decision: "is [university] NAAC accredited", "[college] NIRF ranking 2025", "[institute] UGC recognized"
Comparison: "IIT vs NIT for [branch]", "BITS Pilani vs Manipal for engineering"
Awareness: "how NIRF ranking works", "what is NAAC accreditation"

---

## Platform Priority

1. **Google Gemini** — Highest volume for education queries; YouTube integration for tutorial content
2. **Perplexity** — Research behavior for course/program comparisons
3. **ChatGPT** — Career guidance and course recommendation queries

---

## Schema for EdTech

```json
Priority types:
- EducationalOrganization
- Course (for individual courses)
- EducationalOccupationalProgram (for degree programs)
- LearningResource
- Event (for webinars, info sessions)
- FAQPage (admission FAQ, course FAQ)
- Review + AggregateRating
```

---

## India-Specific EdTech Signals

**Directories**: Shiksha.com, CollegeDekho, Careers360, AdmitKard, GetMyUni
**Publications**: ET Education, Mint Education, YourStory Education, Inc42 EdTech
**Regulators**: NAAC, UGC, AICTE, NSDC, National Testing Agency (NTA)
**Government programs**: Skill India, PM-KAUSHAL, NSDC tie-ups, NEP 2020 alignment
**Certifications**: Microsoft Learn, Google Career Certificates, AWS Training — name-dropped in content carry platform credibility
