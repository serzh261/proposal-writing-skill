# Template — Triage Verdict

Output structure for triage mode (`modes/triage.md`). Fill every section, even briefly.

---

## TRIAGE VERDICT

**Opportunity:** [Title]
**Solicitation #:** [Number]
**Buyer:** [Agency / organization]
**Award type:** [RFP / RFQ / RFI / BAA / CSO / Sole-source / Set-aside type]
**Estimated value:** [If stated; otherwise "Not stated" and your inferred range]
**Due date:** [Proposal due, in CT or local time]
**Q&A deadline:** [If applicable]
**Period of performance:** [Start date - end date if stated]

**Verdict:** **GO / NO-GO / MAYBE**

---

### Hard Eligibility Check

| Test | Result | Notes |
|---|---|---|
| For-profit allowed? | PASS / FAIL | [Cite RFP section] |
| NAICS match (541611/541512/541690 or adjacent)? | PASS / FAIL | [NAICS in RFP, size standard] |
| Agency-type restriction? | PASS / FAIL | [LEA/SAA only, nonprofit only, Title IV-E, etc.] |
| Clearance required? | PASS / FAIL | [Facility, personnel] |
| Past performance threshold? | PASS / FAIL | [Number of federal primes required, etc.] |
| Geographic restriction? | PASS / FAIL | [In-state, regional restrictions] |

[If any FAIL → verdict is NO-GO. Stop and go to blocklist entry section.]

---

### Five-Condition Hiring-to-Bid Framework

| Condition | Test | Result |
|---|---|---|
| 1. Eligibility open to for-profits | (covered above) | PASS / FAIL |
| 2. Core capability is scope center of gravity | [Yes if data/analytics/BI is the deliverable; No if domain bolt-on] | PASS / FAIL / MAYBE |
| 3. Adjacent past performance exists | [Which CCARs apply?] | PASS / FAIL / MAYBE |
| 4. Hire cost recoverable in award | [Hire cost estimate vs. EV] | PASS / FAIL / MAYBE |
| 5. Timeline fits hire process | [Days to submit vs. sourcing reality] | PASS / FAIL / MAYBE |

---

### Win Probability Assessment

| Factor | Read | Direction |
|---|---|---|
| Incumbent | [Identified? Who? Vulnerability?] | + / - / 0 |
| Set-aside | [Open / SB / 8(a) / WOSB / HUBZone] | + / - / 0 |
| Buyer relationship | [Warm / Cold / Existing relationship] | + / - / 0 |
| Working sample feasibility | [Yes / No / Constrained by timeline] | + / - / 0 |
| Competition density | [Sole-source / Limited / Open] | + / - / 0 |

**Win probability bucket:** **Low (5-15%) / Medium (15-35%) / High (35%+)**

---

### EV Math

- Estimated award value: $[X]
- Win probability: [Y]%
- Expected award value: $[X × Y]
- Estimated proposal hours: [N]
- [Principal]'s opportunity cost: $[REDACTED]/hr × [N hours] = $[Z]
- Out-of-pocket (sub proposal effort, graphics, etc.): $[A]
- Total proposal cost: $[Z + A]
- **Net EV: $[(X × Y) - (Z + A)]**

---

### Key Reasons to Pursue

- [Bullet 1]
- [Bullet 2]
- [Bullet 3]

### Key Reasons to Pass

- [Bullet 1]
- [Bullet 2]
- [Bullet 3]

---

### If GO — First Moves

1. **Submit Q&A by [date]:** [Specific questions to ask]
2. **Discovery:** [Next mode — `modes/discovery.md`. Time estimate.]
3. **Capabilities to source:** [Any gap analysis flagged hires]
4. **Working sample candidate:** [What to build, time estimate]

### If NO-GO — Blocklist Entry

```python
# [Title] — [Reason category]
# Surfaced: [date], Triage verdict: NO-GO, Reason: [reason]
"[ID/ALN]": "[concise reason]",
```

**Please confirm before treating this as final blocklist entry.**

### If MAYBE — Intel Needed

- [What specific information would flip this to GO or NO-GO]
- [How to get it — Q&A submission, contracting officer call, sources sought response]
- [By when]

---

**Estimated triage time spent:** [X minutes]
