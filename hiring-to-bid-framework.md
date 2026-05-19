# Hiring-to-Bid Framework — Five Conditions

This framework determines whether a capability gap is worth filling via a hire/sub vs. signals a no-go. Originally derived from the chat where [Principal] pushed back on reflexive no-gos and Claude articulated when hiring makes sense.

**The rule: hire only if ALL FIVE conditions are TRUE. If even one fails, hiring becomes a money-losing exercise.**

## The Five Conditions

### Condition 1 — Eligibility is open to for-profits

This is binary and non-negotiable. No amount of hiring fixes the applicant-type bar.

**Examples of fails:**
- FEMA PRPA (LEA/SAA only)
- EPA Water Training and Technical Assistance (for-profit explicitly excluded)
- HRSA MHEMT (nonprofit/higher-ed only)
- ACYF Child Welfare Predictive Analytics (Title IV-E agency partnership required)

**Test:** Does the RFP, ALN, or program guidance restrict eligibility to non-commercial entities? If yes, no-go regardless of capability.

### Condition 2 — [Firm]'s core capability is the scope's center of gravity

The work must be fundamentally a data / analytics / dashboard / automation / reporting problem with domain context around it. The hires fill the domain context. If the scope is fundamentally clinical, legal, construction, or research with data bolted on, the hires *become* the proposal and reviewers will see it.

**Examples of fails:**
- NGA BIG-ST BAA (fundamentally GEOINT research, not analytics)
- HRSA MHEMT (fundamentally clinical training, not analytics)
- [State DNR] Force Main sewer bid (civil construction)

**Test:** Strip the RFP down to its core deliverable. Is the deliverable a data product? Or is it a clinical study, training curriculum, construction project, or research paper that uses data?

### Condition 3 — [Firm] has adjacent past performance to anchor the narrative

A reviewer needs something concrete to point to in your past-performance section. If every hire on the proposal has stronger past performance than [Firm] does in the actual scope area, [Firm] is the wrong prime.

**Strong anchors for adjacent past performance:**
- Federal grant compliance reporting ([Federal Intermediary], AHP)
- Multi-jurisdictional federal program analytics ([Federal Intermediary] $[REDACTED]M)
- Enterprise-scale BI delivery ($[REDACTED]M pipeline)
- Microsoft-native dashboards and ETL

**Examples of fails:**
- Any clinical/medical scope (no past performance)
- Any DoD/IC scope (no past performance, no clearance)
- Any pure GIS-research scope where [GIS Sub]'s commercial GIS doesn't anchor

**Test:** Can [Firm] credibly write a past-performance section that connects to the RFP's scope, where the connection isn't only through the hired SMEs? If past performance is empty for this scope, sub under someone with the past performance instead of priming.

### Condition 4 — Hire cost is recoverable within the award

Ballpark: $30K-$80K to assemble a credible hired team (SME consultants at $150-400/hr, proposal writer at $15-30K, letters of support coordination) before knowing whether the bid wins.

**Math:**
- On a $600K award with 10-15% win probability = $60K-$90K expected value. Hire cost of $30K-$80K is break-even territory or negative.
- On a $3M award with <5% win probability = $150K expected value. Hire cost of $80K is negative.
- On a $5M+ award where [Firm] is a genuine fit = winning bet.

**Test:** Compute expected value (award × P(win)) minus all-in proposal cost including hires. Is the number positive? Is it meaningfully positive given [Firm]'s bandwidth alternatives?

### Condition 5 — The clock fits

Quality hires need 2-3 weeks of back-and-forth to sign teaming agreements, review scope, write their sections, provide biographies, and give letters of support. Sub-25-day windows compress that to the point where you're hiring whoever answers the phone, not the best fit.

**Timeline benchmarks:**
- <14 days to submit: hire only what [Principal] can engage same-day (Ben for GIS, a writer if already on rolodex). No new SME hires.
- 14-25 days: Upwork sourcing for technical roles plausible. Letters of support hard.
- 25-45 days: full team build plausible if started immediately.
- 45+ days: comfortable to source SMEs, proposal writer, graphics support.

**Test:** Map every hire needed to a realistic source-to-commit-to-deliverable timeline. Do all hires complete their work by the proposal due date? With buffer?

## Application to Triage

For each opportunity at triage:

| Condition | Test | Result |
|---|---|---|
| 1 | For-profit eligible? | PASS / FAIL |
| 2 | Core competency is scope center of gravity? | PASS / FAIL / MAYBE |
| 3 | Adjacent past performance exists? | PASS / FAIL / MAYBE |
| 4 | Hire cost recoverable in award? | PASS / FAIL / MAYBE |
| 5 | Timeline fits hire process? | PASS / FAIL / MAYBE |

**ALL PASS → proceed (gap analysis next).**
**ANY HARD FAIL → no-go.**
**ANY MAYBE → either gather intel to flip to PASS/FAIL, or proceed cautiously with the risk surfaced.**

## When the framework points to teaming-as-sub instead

If Condition 1 passes but 2 or 3 fail, [Firm] might still get involved as a subcontractor on someone else's bid. The DHS CSO example: [Firm] as prime was a fail on Condition 3 (no federal past performance). [Firm] as sub to a prime like Booz Allen would still need to be evaluated, but the math changes — [Firm] isn't risking the proposal effort, just providing capability statement to the prime.

**Sub-as-team decision criteria:**
- Is there a credible prime to approach within 48 hours?
- Does [Firm] bring something specific the prime needs (data analytics, [metro-local] presence, niche capability)?
- Is the sub effort small enough to not pull focus from active prime bids?

Generate outreach via `templates/sourcing-outreach.md` if pursuing teaming.

## When the framework points to "wait for next cycle"

Some opportunities are clear no-gos *this cycle* but plausible *next cycle* if [Firm] invests in specific capability building. File these to a "future targets" list with the missing capability noted.

Examples:
- "Pursuable in 2 years if 8(a) certification lands"
- "Pursuable after first completed [Regional Council] delivery as past performance"
- "Pursuable after 1 year of federal sub work to build CPARS history"

## Anti-patterns the framework prevents

- **The "I want to apply anyway" failure mode.** [Principal] has pushed back on no-gos before. Sometimes rightly (this framework came from one of those pushbacks). Sometimes wrongly (DHS CSO where math was clearly negative). The framework provides honest numbers. [Principal] retains decision authority.
- **The capability-gap reflex.** Not every gap is automatic no-go. The framework distinguishes structural gaps (clearance, past performance threshold) from fillable gaps (specific technical skill, domain SME).
- **The sunk-cost trap.** Effort already spent on partial research doesn't justify bidding a losing opportunity. If conditions fail, bail — the work already done is lost regardless.
- **The "we'll figure it out" optimism.** Quality hires take time. If the timeline doesn't fit, the bid doesn't fit.
