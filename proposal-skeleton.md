# Template — Proposal Skeleton

Default 11-section structure for state, regional, and higher-ed proposals. This is the proven structure from [Regional Council] and [State University] bids. Adapt to RFP-specific requirements when they differ. For federal civilian proposals, use `references/federal-rfp-scaffolding.md` instead.

---

## §1 — Cover Page

- Firm name ([Firm Name] LLC)
- Solicitation number and title
- Submitted to: [Buyer name, address]
- Submitted: [Date]
- Submitted by: [Principal Name], Principal
- Contact: [email, phone]
- [Firm] NAICS codes: 541611, 541512, 541690
- UEI / SAM.gov registration status (when applicable)

---

## §2 — Executive Summary

**Length:** 1 page (2 max)
**Written:** LAST, placed first
**Voice:** Confident, conversational, specific. Banned phrases excluded.

Opening pattern ([Firm] voice):
> "We've read the RFP carefully and we're not proposing a generic analytics engagement..."

Required elements:
- Opening that references the buyer's problem (not [Firm]'s capabilities)
- Naming of the discriminators that apply (working sample, [Federal Intermediary] past performance, Microsoft fit, [Metro] presence as appropriate)
- One paragraph on [Firm]'s specific fit
- One sentence on fee and timeline
- One line authorizing next conversation

---

## §3 — Firm Overview

**Length:** 0.5 page

- Legal name: [Firm Name] LLC
- Structure: For-profit LLC
- Founded: June 2025
- Location: [City, ST] ([Metro Area]politan area)
- NAICS codes: 541611 (Administrative Management Consulting), 541512 (Computer Systems Design Services), 541690 (Other Scientific and Technical Consulting Services)
- SAM.gov: [registration status — current or pending]
- 8(a) status: [If certified — disclose. If pending, do not disclose application status in proposal.]
- Core capabilities: Power BI dashboards, SQL/Python data pipelines, federal grant compliance reporting, GIS via named subcontractor
- Why we're bidding this work: [One sentence linking firm fit to RFP scope]

---

## §4 — Relevant Experience

**Length:** 1.5-2 pages

3-5 past performance entries from `references/ccar-bank.md`. Lead with most relevant (not most impressive).

For each entry:
- **Project title** (Client, dates)
- 2-3 sentence narrative in CCAR format
- **Relevance to [Buyer]:** callout connecting to specific evaluation criterion in the RFP
- Quantified outcome where defensible

Standard sequence for [Firm]:
1. **[Federal Intermediary] $[REDACTED]M Multi-Jurisdictional Federal Initiative** (lead for federal-adjacent and multi-jurisdictional bids)
2. **[Federal Grantee] Federal Grantee Dashboard** (supports federal-adjacent positioning)
3. **$[REDACTED]M Enterprise Sales Analytics Pipeline** (BI delivery at scale, Microsoft-native fit)

Adjust order and selection based on bid type per guidance in `references/ccar-bank.md`.

---

## §5 — Technical Skills Summary

**Length:** 0.5-1 page

Three-column table:

| Analytics & BI | Data & Integration | GIS & Visualization |
|---|---|---|
| Power BI Pro/Embedded | SQL Server, T-SQL, SSIS, SSRS | ArcGIS Online ([GIS Subcontractor], named) |
| DAX, Power Query, M | Azure Data Factory | ArcGIS Pro ([GIS Subcontractor], named) |
| Microsoft Fabric | Python (Pandas, automation) | [GIS Certification] |
| Dashboard design and theming | SharePoint integration | ESRI Dashboard Builder |
| Federal grant compliance reporting | API integration | Azure Maps |
| Multi-source data integration | ETL pipeline architecture | Power BI map visualizations |

Customize column headers to match RFP categories where they differ. Don't list tools [Firm] doesn't have.

---

## §6 — Proposed Scope of Work, Methodology & Approach

**Length:** Largest section, typically 3-5 pages

Structure: Mirror RFP's task structure exactly. If RFP has Task 1, Task 2, Task 3, your subsections are §6.1, §6.2, §6.3 with matching task names.

For each task:

### §6.[N] — [Task name from RFP]

**Opening paragraph:** Restate the task in [Firm]'s words. Connect to buyer's outcome (not to [Firm]'s process).

**Approach:** Concrete actions, named tools, real methods. Not "we will leverage industry best practices" but "we'll embed with [Buyer] staff from day one, attend planning sessions, and turn raw operational data into usable documentation fast."

**Deliverables:**
- [Deliverable 1] — [Format, e.g., "Power BI report (.pbix) + documentation"]
- [Deliverable 2]
- [Deliverable 3]

**Tools and methods:**
- [Specific tools used]
- [Specific data sources]
- [Specific standards/frameworks where relevant]

**Phase or timing note (optional):** [If task has specific timing within overall engagement]

---

## §7 — Project Staffing & Qualifications

**Length:** 1-1.5 pages

### §7.1 — Lead Consultant

| Item | Detail |
|---|---|
| Name | [Principal Name] |
| Role | Principal Consultant / Project Manager |
| % Time on engagement | [60-80%] |
| Qualifications | [Brief — full resume in Appendix A] |
| Responsibilities | [Specific to this engagement] |

### §7.2 — GIS Subcontractor (when GIS in scope)

| Item | Detail |
|---|---|
| Name | [GIS Subcontractor] |
| Role | GIS Lead |
| % Time on engagement | [20-40%] |
| Qualifications | [GIS Certification], [N] completed government GIS projects, [X]% success rate |
| Responsibilities | [Specific to this engagement] |
| Engagement basis | Named subcontractor under formal subcontract agreement |

### §7.3 — Additional Capacity (paragraph form)

> "Beyond the core team, [Firm] maintains an active network of vetted contractors for specialized capacity — graphics support, additional GIS analysts, federal grant writers, and domain SMEs. For this engagement, no additional team members are anticipated, but we have on-call capacity to scale if scope expands."

Adjust the paragraph based on actual capacity expectations for the bid.

**Full resumes in Appendix A.**

---

## §8 — Project Timeline

**Length:** 0.5 page

Phase table:

| Phase | Name | Weeks | Activities | Deliverables |
|---|---|---|---|---|
| 1 | Stakeholder Alignment & Discovery | Weeks 1-3 | [Activities] | [Deliverables] |
| 2 | Data Integration & Architecture | Weeks 2-8 | [Activities] | [Deliverables] |
| 3 | Dashboard & Documentation Build | Weeks 5-14 | [Activities] | [Deliverables] |
| 4 | Refinement, Training, Handoff | Weeks 12-20 | [Activities] | [Deliverables] |

Phases overlap intentionally. Final deliverable date should match RFP-required completion.

---

## §9 — Itemized Cost Proposal

**Length:** 0.5-1 page

Table format:

| Task / Deliverable | Hours | Rate | Who | Cost | % of Total |
|---|---|---|---|---|---|
| Phase 1 — Stakeholder Alignment | [N] | $[X]/hr | [Principal] | $[Y] | [Z]% |
| Phase 2 — Data Integration | [N] | $[X]/hr | [Principal] | $[Y] | [Z]% |
| Phase 3 — Dashboard Build | [N] | $[X]/hr | [Principal] | $[Y] | [Z]% |
| Phase 3 — GIS Components | [N] | $[REDACTED]/hr | [GIS Subcontractor] | $[Y] | [Z]% |
| Phase 4 — Refinement & Handoff | [N] | $[X]/hr | [Principal] | $[Y] | [Z]% |
| **Total** | | | | **$[Total]** | 100% |

**Rate note** (brief, no AI-sounding justification):
> "This proposal is presented as a fixed-fee engagement. All hours and rates above reflect the blended cost basis. No additional fees for travel within the [Metro Area] region, communication, or scope items as described above."

---

## §10 — Work Product Samples

**Length:** 0.5 page

If a working sample has been built for this bid:
- Reference it (Appendix B or C, by name)
- Caption explaining what it demonstrates
- Offer same-day delivery of additional samples on request

If no working sample for this bid:
- Reference past work generally
- Offer same-day samples on request
- Consider whether to build a sample before submission (Tier 1 discriminator opportunity)

---

## §11 — References

**Length:** 0.5 page

Three references, real and verified within 30 days of submission. Table format:

| Name | Title | Organization | Phone | Email |
|---|---|---|---|---|
| [Real name] | [Title] | [Organization] | [Phone] | [Email] |
| [Real name] | [Title] | [Organization] | [Phone] | [Email] |
| [Real name] | [Title] | [Organization] | [Phone] | [Email] |

**No placeholders in submitted version.** If references are not yet verified, the proposal is not ready to submit.

---

## Appendices and Attachments

### Appendix A — Resumes
- [Principal Name] (full resume)
- [GIS Subcontractor] (if named in §7.2)

### Appendix B — Work Sample
- [If applicable — the dashboard PDF or screenshot]

### Attachment A — Affirmative Action Checklist
- [Completed or N/A statement for small firms]

### Attachment B — Debarment Certification
- [Signed and dated by [Principal]]

### Other required attachments per RFP
- [Insurance certs, reps & certs, etc.]

---

## How to use this skeleton

1. Open this template and the RFP side by side
2. Walk the RFP's "Required Proposal Contents" section
3. Map each RFP requirement to a section above (or note a deviation if RFP requires different structure)
4. Adjust section numbering and headers to match RFP requirements if different
5. Once mapped, draft section by section following voice rules and win themes
6. Update compliance matrix Status column as sections are drafted

If RFP structure differs from this skeleton significantly (e.g., federal multi-volume, unusual page-limited structure), defer to RFP structure and use this skeleton only as a content checklist.
