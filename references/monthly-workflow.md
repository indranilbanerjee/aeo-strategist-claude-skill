# Monthly Retainer Workflow — AEO Client Management
## INT TechShu Internal | Operational rhythm for the team

---

## Overview
AEO retainer delivery is a repeating monthly cycle. This document defines exactly what happens each month, who owns it, and what gets delivered. Use this as the operational SOP — not a strategy document.

---

## Monthly Cycle: Week-by-Week

### WEEK 1 — MEASURE (Days 1–7)

**Day 1–2: AI SOV snapshot run**
- Assign to: Junior AEO analyst
- What: Run all 20 tracked queries × all relevant platforms × 3 tests each (use tracking-protocols.md Layer 1)
- Output: Filled SOV snapshot sheet with screenshots
- Flag to senior if: Brand disappears from a query it was appearing in / New competitor appears / AI response contains inaccuracy about brand

**Day 2–3: GA4 AI channel review**
- Pull: AI Referral traffic from custom channel group (tracking-protocols.md Layer 2)
- Note: Sessions, engagement rate, goal completions vs last month
- Note: Which pages are receiving AI referral traffic

**Day 3: Brand search volume check**
- Google Search Console: branded query impressions trend (last 30 days vs prior 30 days)
- Note any anomalies

**Day 4–5: Citation audit**
- For queries where brand appears: what sources are being cited alongside it?
- Build or update cited assets list
- New citations this month = wins. Missing citations from pages you optimised last month = signals to investigate.

**Day 5–7: Month's measurement summary**
- Compile: SOV score, SOV delta vs last month, GA4 AI traffic, brand search trend, new citations, competitor movement
- This becomes Section 2 of the monthly report

---

### WEEK 2 — PRODUCE (Days 8–14)

**Day 8–9: Content production**
- Produce 1–3 AEO-optimised content pieces (based on `/brief` outputs from last month's strategy)
- Follow eval-criteria.md quality gates for briefs
- For regulated industry clients: submit for medico-legal review now (gives 1 week for review before publish)

**Day 10: Schema audit**
- Check if any schema deployed last month is live and returning rich results in Google Rich Results Test
- Flag any schema errors in Search Console → Enhancements

**Day 11: Directory updates**
- Revisit incomplete directories flagged in last month's P1/P2 list
- Update any directory listings with new content, photos, or review responses
- Note: Respond to ALL new reviews in directory platforms — response rate is a trust signal

**Day 12–14: Technical fixes (if queued)**
- Deploy any pending schema, robots.txt, llms.txt, or content restructuring changes
- Document exactly what was changed + date (for attribution purposes in next month's report)

---

### WEEK 3 — EARN (Days 15–21)

**Day 15–17: PR outreach**
- Send 2–3 targeted pitches to publications from `/pr-brief` output
- Target: AI-licensed publications and high-DA sector media
- Follow up on previous pitches
- Goal: 1+ piece of coverage per month in qualifying publication

**Day 18–19: Community and Reddit activity** (where applicable for vertical)
- Participate in 2–3 relevant discussions
- NOT spam — answer actual questions, reference brand only when genuinely relevant
- For India clients: relevant subreddits + Quora + LinkedIn communities

**Day 20–21: Link earning / citation building**
- Identify unlinked brand mentions (tools: Ahrefs Alerts, Google Alerts for brand name)
- Outreach to convert to linked mentions (these become AI source citations)

---

### WEEK 4 — REPORT + PLAN (Days 22–30)

**Day 22–24: Write monthly report**
- Use `/report` mode output template
- Sections: Executive summary, SOV trend, citation rate, sentiment check, attribution, next month priorities
- Keep it non-technical at summary level — CMO/client sees this

**Day 25: Internal review**
- Senior AEO team member reviews report before client delivery
- Check: Are attribution claims valid? Are recommendations actionable? Is compliance section complete for regulated clients?

**Day 26–28: Client delivery and feedback**
- Deliver report
- Present in meeting or async per client preference
- Capture client feedback + new business context (product launches, campaigns, news that affects AEO angle)

**Day 29–30: Next month planning**
- Update priority list based on month's findings
- Run `/strategy` refresher if major change in competitive landscape
- Queue content briefs for next month (`/brief` for 2–3 new topics)
- Update tracked query list if new queries emerge from keyword/competitive research

---

## Monthly Deliverables Summary

| Deliverable | Mode Used | Audience | Due |
|-------------|-----------|----------|-----|
| SOV snapshot report | Manual (tracking-protocols.md) | Internal team | Day 7 |
| 1–3 AEO content pieces | /brief + /rewrite | Content team | Day 14 |
| Schema / technical update log | /schema | Dev team | Day 14 |
| Earned media coverage summary | /pr-brief tracking | Internal | Day 21 |
| Monthly AEO client report | /report | Client (CMO/marketing) | Day 26 |
| Next month content queue | /brief | Internal planning | Day 30 |

---

## Escalation Triggers

Flag to client immediately (don't wait for monthly report) if:

1. **AI response contains damaging inaccuracy** — wrong facts about brand, negative framing without basis
2. **Brand disappears completely from 3+ tracked queries** — sudden parametric shift may indicate a negative press event or algorithm change
3. **Compliance issue discovered** — AI is citing client content in a way that creates regulatory risk
4. **Competitor makes a major AEO-relevant move** — publishing proprietary research, major press placement, Wikipedia creation

---

## Quarterly Review (Every 3 Months)

In addition to monthly cycle, conduct quarterly:
- Full `/audit` refresh (compare to baseline)
- Competitive footprint update (`/competitor` re-run)
- Query library expansion (`/query-library` — add 10 new queries based on market changes)
- Strategy check: Are we still on the right track or does Layer A / Layer B strategy need adjustment?
- Roadmap update: Mark completed items, revise remaining weeks
