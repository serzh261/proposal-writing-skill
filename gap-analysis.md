# Mode: Gap Analysis

Use this mode when [Principal] has decided to bid (or is leaning toward bidding) and needs to know what capabilities are required vs. what's on bench. [GIS Subcontractor] was the proof of concept: [Regional Council] required GIS, [Firm] didn't have deep ESRI, we found [GIS Sub] on Upwork and named him in the proposal. The pattern works. Encode it.

## What gap analysis produces

A structured map:

1. Every capability the RFP requires
2. Which capabilities [Firm] has covered ([Principal], Ben)
3. Which capabilities are missing
4. For each gap: hire / team-as-sub / no-go recommendation
5. For each hire recommendation: a concrete sourcing playbook

## Process

### Step 1 — Extract every capability the RFP requires

Read the RFP's statement of work and required qualifications sections. Pull out every skill, certification, tool, or domain expertise mentioned. Be granular — "data analytics" is too vague. Examples of capability-level granularity:

- Power BI dashboard development
- Azure Data Factory pipeline build
- ETL from SQL Server to Snowflake
- ArcGIS Pro spatial analysis
- Section 508 accessibility compliance
- Federal grant compliance reporting (NOFA, FFR, federal cost principles)
- Bilingual content (Spanish, etc.)
- Specific federal framework knowledge (FISMA, NIST 800-53, FedRAMP)
- Clinical SME (specific specialty)
- Customs/trade SME
- Workforce development domain expertise
- Statistical methods (specific: regression, ML, predictive modeling)
- Survey design and administration
- Stakeholder facilitation across X jurisdictions

Output a flat list, capability by capability.

### Step 2 — Map against the bench

[Firm]'s bench (don't maintain this as a persistent file — re-derive each bid):

**[Principal Name], Principal:**
- Power BI (Pro, Embedded, theming)
- DAX, Power Query, M
- SQL Server, T-SQL, SSIS, SSRS
- Python (Pandas, automation)
- Azure Data Factory, Azure Maps
- SharePoint integration
- Microsoft 365 / Teams
- Federal grant compliance reporting ([Federal Intermediary], AHP)
- Multi-jurisdictional federal program analytics
- Enterprise sales analytics
- Microsoft Fabric (current direction)

**[GIS Subcontractor], Subcontractor (GIS lead):**
- ArcGIS Online, ArcGIS Pro
- [GIS Certification]
- ESRI Dashboard Builder
- GIS data normalization
- Government and infrastructure GIS ([N] projects, [X]% success rate)
- Power BI familiarity

**Tools/methods [Firm] does NOT have on bench (default to gap unless added by [Principal]):**
- Tableau (not Microsoft-native)
- Snowflake, Databricks (capable, not credentialed)
- AWS, GCP (Microsoft-native firm)
- Clinical domain SMEs
- Trade/customs SMEs
- Survey design specialists
- Bilingual content delivery
- Federal facility clearance
- FedRAMP-authorized hosting (would require partner)
- Section 508 accessibility audit credentials
- Statistical methods beyond descriptive (regression, ML — [Principal] can do basic, not credentialed)
- Grant writing (specific to NOFA/NIH/NSF formats)

For each capability in the RFP, mark: **COVERED ([Principal])** / **COVERED (Ben)** / **GAP**.

### Step 3 — For each gap, apply the hiring-to-bid framework

Load `references/hiring-to-bid-framework.md`. Check all five conditions for the bid as a whole, then specifically ask for each gap:

- **Is this gap fillable by a single hire, or does it require institutional capability we can't bolt on?**
  - Hire-fillable: GIS expert (Ben proved it), grant writer, statistical SME, customs SME
  - Not hire-fillable: facility clearance, FedRAMP authorization, "10 years federal prime past performance," organizational maturity beyond [Firm]'s scale
- **Is the hire cost recoverable in the award?**
  - Subcontractor at $58-300/hr × 20-100 hours = $1,200-$30,000
  - Award value × P(win) needs to comfortably exceed this
- **Is the timeline survivable?**
  - <2 weeks to proposal due → only people [Principal] can engage same-day
  - 2-4 weeks → Upwork sourcing, LinkedIn outreach plausible
  - 4+ weeks → can build a real team

Output for each gap:

- **HIRE** — specific role, expected rate range, expected hours, sourcing approach
- **TEAM AS SUB** — prime contractor types to approach ([Firm] as subcontractor on someone else's bid)
- **NO-GO REASON** — gap is structural, not fillable

### Step 4 — Generate sourcing playbooks for the HIRE gaps

Load `references/gap-analysis-and-sourcing.md` for the playbook patterns. The playbooks cover:

- Upwork search and outreach (proven: this is how [GIS Sub] was found)
- LinkedIn search and outreach
- ESRI Partner Directory (for GIS-specific)
- Retired-federal SME networks (for federal domain expertise)
- University consulting offices (for specialized academic SMEs)
- Local trade association networks
- Prime contractor BD teams (for team-as-sub plays)

Generate a concrete one-pager per gap with:

- Where to search (specific URLs, search terms)
- What to look for in a candidate (certifications, past projects, rate range, availability)
- An outreach message template ([Principal] copy-pastes and sends)
- Timeline expectations (how long to expect from first contact to verbal yes)

### Step 5 — Roll up to a recommendation

Show [Principal] the full map: capabilities, coverage, gaps, fix per gap. Then issue a recommendation:

- **PROCEED** — gaps are fillable, total fill cost is reasonable, timeline works
- **PROCEED IF [X]** — gaps fillable conditional on a specific event (e.g., "if we can get a verbal commit from a GIS person by Wednesday")
- **PIVOT TO TEAMING** — too many gaps for prime bid; pursue as sub instead. Generate primes-to-approach list.
- **NO-GO** — structural gap (clearance, past performance threshold) can't be fixed for this bid

## Output format

```
GAP ANALYSIS — [Solicitation Number / Title]

CAPABILITIES REQUIRED (extracted from RFP):
1. [Capability] — [COVERED [Principal] / COVERED [GIS Sub] / GAP]
2. [Capability] — [...]
...

GAPS REQUIRING ACTION:
[For each gap]
- Capability: [name]
- Severity: [Critical / Important / Nice-to-have]
- Recommendation: [HIRE / TEAM AS SUB / NO-GO]
- If HIRE:
  - Role title: [e.g., "[GIS-certified] GIS analyst"]
  - Estimated hours: [X]
  - Rate range: [$Y-$Z/hr]
  - Total cost: [$N]
  - Sourcing approach: [Upwork / LinkedIn / partner directory / network]
  - Outreach template: [→ generated in sourcing-outreach.md]
  - Timeline: [days from contact to verbal commit]
- If TEAM AS SUB:
  - Prime types to approach: [list]
  - Outreach angle: [[Firm]'s value to the prime]
- If NO-GO:
  - Structural reason: [why no hire can fix this]

OVERALL RECOMMENDATION:
[ PROCEED / PROCEED IF X / PIVOT TO TEAMING / NO-GO ]

FIRST MOVES (if PROCEED):
1. [Action — by date]
2. [Action — by date]
3. [Action — by date]
```

## Anti-patterns to avoid

- **Don't treat every gap as a hire opportunity.** Some gaps (clearance, structural past performance, multi-year accumulated organizational maturity) cannot be hired in. Be honest.
- **Don't underestimate the time cost of sourcing.** A "quick hire on Upwork" still takes 2-5 days from search to verbal commit. Build that into the timeline.
- **Don't let hiring cost balloon past EV.** If the bid needs $40K of hires to win and the bid is $100K with 15% win probability, the math doesn't work.
- **Don't promise capabilities the hire hasn't agreed to yet.** Until you have a verbal commit and a one-page bio you can attach, the hire is hypothetical and the proposal can't name them.
- **Don't list "Ben" reflexively for every GIS gap.** Verify [GIS Sub]'s availability for this timeline before assuming. He has a day job and limited bandwidth.
