# Industry: Healthcare (Non-Pharma)
## Hospitals, Diagnostics, Medical Devices, Health Tech, Wellness
## Deep AEO Reference — INT TechShu Internal

---

## Sub-Verticals Covered
1. Hospitals and multi-specialty health systems
2. Specialty clinics (oncology, cardiology, fertility, ortho, dermatology)
3. Diagnostic labs (pathology, radiology, imaging)
4. Health tech / digital health platforms (telemedicine, health apps)
5. Dental chains
6. Ayurveda / traditional medicine (AYUSH)
7. Wellness and preventive health
8. Home healthcare services
9. Medical tourism facilitators

---

## Trust Signal Hierarchy

1. **Accreditation bodies** — NABH (National Accreditation Board for Hospitals, India), JCI (Joint Commission International, global), NABL (labs, India), CAP (College of American Pathologists). These are the highest credibility signals for hospital/diagnostic AEO.
2. **Doctor credentials and profiles** — Named, credentialed doctors with MBBS/MD/MS/DM registrations, fellowship affiliations (AIIMS, CMC Vellore, Apollo, Fortis pedigree), NMC/state medical council registration numbers.
3. **Medical council registrations** — NMC (National Medical Commission India), GMC (UK), USMLE/state boards (US).
4. **Government hospital empanelment** — CGHS (Central Government Health Scheme), Ayushman Bharat PMJAY, state government empanelment. Being an empanelled hospital is a huge trust signal.
5. **Clinical outcomes data** — Published survival rates, success rates, infection rates, JCI quality metrics. AI weights these extremely highly for high-stakes medical decisions.
6. **Patient review platforms** — Google Reviews, Practo reviews, JustDial health ratings, Lybrate. Volume + recency + response rate all matter.
7. **Health media coverage** — ET Healthworld, Health Shots, TheHealthSite, NDTV Doctor, WebMD India, Healthline (for global).
8. **Research and academic affiliations** — Published research in PubMed, teaching hospital status, medical college affiliation.
9. **Insurance network status** — CGHS/ECHS empanelment, TPA (third-party administrator) network listing — critical for patient decision queries.
10. **Awards and rankings** — FICCI Healthcare Excellence Awards, Times Health Survey rankings, Asia Hospital Management Awards.

---

## Compliance Constraints

### India (PCPNDT, NMC, CGHS)
- **PCPNDT Act**: Diagnostic centers must not indicate sex of foetus — never create AEO content near this space.
- **NMC Regulations on Advertisements**: Doctors cannot solicit patients through advertisements. Doctor-level AEO content must be informational, not promotional.
- **Telemedicine Practice Guidelines 2020**: Teleconsultation platforms must follow prescribed workflow — content must reflect compliant practice.
- **AYUSH**: Content for Ayurveda/Yoga/Naturopathy/Unani/Siddha/Homeopathy products cannot make disease treatment claims without reference to Ministry of AYUSH approved protocols.
- **Clinical Establishments Act**: Registered under state clinical establishments authority — registration number is a trust anchor.

### UK (CQC / GMC)
- CQC (Care Quality Commission) registration and inspection rating are high-value trust signals.
- GMC registration for individual doctor profiles.
- NHS Choice status for private providers marketing to NHS patients.

### US (Joint Commission / CMS)
- Joint Commission accreditation status.
- CMS Star Ratings for hospitals.
- State medical board license numbers for physician content.

### Medical Tourism
- Must be transparent about accreditation status, success rates, and follow-up protocols.
- JCI accreditation is the gold standard for medical tourism AEO.

---

## Query Taxonomy

### Hospital / Health System
Decision: "best hospital for cardiac surgery in [city]", "NABH accredited hospitals [city]", "[hospital] success rate bypass surgery", "Ayushman Bharat empanelled hospitals [city]"
Comparison: "Apollo vs Fortis vs Max hospital", "private vs government hospital [city]"
Awareness: "what is NABH accreditation", "how to choose a hospital for surgery"

### Diagnostic Labs
Decision: "NABL accredited lab [city]", "[lab brand] accuracy of tests", "[lab] home sample collection [city]"
Comparison: "Dr Lal PathLabs vs SRL vs Thyrocare", "best diagnostic lab for thyroid test India"
Awareness: "how blood test samples are processed", "what is NABL certification for labs"

### Telemedicine / Health Tech
Decision: "is [app] safe for online doctor consultation", "[app] NABH certified", "[app] licensed doctors"
Comparison: "Practo vs Apollo 24/7 vs mFine", "best telemedicine app India"
Awareness: "how online doctor consultation works India", "telemedicine regulations India"

### Specialty Clinics
Decision: "[clinic] IVF success rate", "best fertility clinic [city]", "[oncology center] cancer treatment outcomes"
Comparison: "best IVF clinics India [city]", "oncology treatment costs India vs abroad"
Awareness: "IVF procedure steps", "cancer staging explained", "Mohs surgery for skin cancer"

---

## Platform Priority

1. **Google Gemini** — Google Health Cards integration; critical for hospital queries
2. **ChatGPT** — Patient symptom and treatment option queries
3. **Perplexity** — Medical research and procedure comparison queries
4. **Claude** — Detailed medical explanation queries; high value for health content

---

## Schema for Healthcare

```json
Priority types:
- Hospital (for hospitals)
- MedicalClinic (for clinics)
- MedicalOrganization (general)
- Physician (for doctor profiles)
- DiagnosticLab (for diagnostic centers)
- MedicalCondition (disease/condition pages)
- MedicalProcedure (procedure pages)
- MedicalTest (diagnostic test pages)
- FAQPage (patient FAQ)
- Review + AggregateRating (patient reviews)
```

**Key**: Include `medicalSpecialty`, `availableService`, `hasCredential` (for NABH/JCI/NABL), `isAcceptingNewPatients` where applicable.

---

## India-Specific Healthcare Signals

**Accreditation**: NABH hospital + clinic, NABL for labs, AYUSH registration for traditional medicine
**Directories**: Practo, Lybrate, JustDial Health, Apollo Health, 1mg doctors
**Publications**: ET Healthworld, Healthworld.com, NDTV Doctor, HealthShots, The Health Site
**Government programs**: PMJAY (Ayushman Bharat), CGHS, ECHS empanelment
**Medical associations**: IMA (Indian Medical Association), specialty boards (CSI for cardiology, API for internal medicine, etc.)
