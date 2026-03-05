# TEMPLATE: Adding a New Industry to AEO Strategist
## Copy this file, rename to [industry-name].md, fill all sections

---

## Industry: [INDUSTRY NAME]
## Sub-Verticals Covered
1. [sub-vertical 1]
2. [sub-vertical 2]
(List all relevant sub-verticals — minimum 5)

---

## Trust Signal Hierarchy (Highest → Lowest)
List 8–12 trust signals specific to this industry, ranked by AEO weight.
For each: the signal type, why AI weights it, and where to verify/build it.

1. **[Signal name]** — [Why AI trusts this] [Where to build it]
...

---

## Compliance Constraints

### India ([Relevant regulatory body])
- [Constraint + implication for content]
- [Safe zones]

### US / Global ([If applicable])
- [Constraint]

### Gate Requirement
[State if medico-legal / compliance review is required before content goes live]

---

## Query Taxonomy

### [Sub-vertical or use case 1]
Decision: "[example query]", "[example query]"
Comparison: "[example query]"
Awareness: "[example query]"
⚠️ Flag: [Compliance flag if applicable]

[Repeat for each major sub-vertical]

---

## Platform Priority for [Industry]
1. **[Platform]** — [Reason specific to this industry]
2. ...

---

## Schema for [Industry]
```json
Priority types:
- [Schema type 1] — [when to use]
- [Schema type 2] — [when to use]
```
Key fields: [list critical schema fields]

---

## [Country/Market]-Specific Signals

**Directories**: [List]
**Publications**: [List — AI-licensed or high-DA specific to this vertical]
**Regulatory anchors**: [List — registration numbers, certifications]
**Associations**: [List — memberships that signal credibility]
**Certifications**: [List]

---

## Notes / Special Considerations
[Anything unique about how AEO works in this industry]

---
AFTER COMPLETING:
1. Add this industry to SKILL.md description field (line 8–9)
2. Add to the client context intake options (line 30)
3. Test with at least one /audit and one /brief prompt
4. Add 2 eval cases to evals/evals.json
