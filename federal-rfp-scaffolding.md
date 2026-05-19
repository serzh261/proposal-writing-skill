# Federal RFP Scaffolding (FAR-Aligned Multi-Volume Structure)

This reference adapts the CaseMark `rfp-response` skill (Apache 2.0 License, https://agentskills.legal/skills/rfp-response) for [Firm]'s federal civilian proposals. The structural scaffolding (Section L/M/C, multi-volume organization, FAR-aligned cost elements) is broadly applicable; [Firm]'s voice rules, win themes, and CCARs replace any generic content guidance.

Use this reference when responding to a federal civilian RFP. For state/regional/higher-ed proposals, use `templates/proposal-skeleton.md` instead.

## Pre-Proposal Phase

Before drafting begins, complete:

### 1. Compliance Matrix

Map every Section L (instructions) requirement to a proposal section. See `modes/compliance-matrix.md`.

### 2. Solicitation Analysis

Extract:
- **Section L** — Instructions to Offerors (format, content, submission)
- **Section M** — Evaluation Factors for Award (weights, sub-factors)
- **Section C** — Statement of Work / Performance Work Statement (tasks, deliverables)
- All amendments (number each and track changes)
- Q&A submissions and responses

### 3. Q&A Strategy

If a Q&A period exists, submit clarifying questions before the cutoff. Strong questions:
- Surface ambiguity in scope (where a competitor might overpromise)
- Establish baseline assumptions (CONUS travel, government-furnished property)
- Demonstrate engagement (CO/program office notice serious bidders)

Don't submit obvious "show your work" questions that signal inexperience.

## Multi-Volume Proposal Structure

Federal civilian solicitations typically request a multi-volume proposal. Standard volumes for a small-to-mid federal civilian bid:

### Volume 1 — Cover Letter / Transmittal Letter (≤2 pages)

- Addressed to named Contracting Officer
- Reference solicitation number, title, and amendments
- Validity period of offer (typically 60-120 days)
- Authorized signatory with binding authority
- POC for clarifications
- Brief (1-2 paragraph) summary of [Firm]'s interest and fit
- No marketing language

### Volume 2 — Technical Proposal

#### A. Executive Summary (≤3 pages)

- Restate the requirement interpretively (shows understanding)
- Connect SOW to agency mission (mirror their strategic plan language)
- Name discriminators that apply (working sample, [Federal Intermediary] past performance, 8(a) status if applicable)
- Brief technical approach overview
- Brief past performance summary (lead with most relevant)
- Brief team summary (named key personnel)

Voice rules apply — no "in today's digital age," no "delve," no "comprehensive."

#### B. Technical Approach

Structure mirrors the SOW (Section C) exactly. For each major task:

- **Task statement** — restate from SOW in [Firm]'s words to demonstrate comprehension
- **Methodology** — concrete approach, not framework names
- **Tools and standards** — specific tools (Power BI, Azure Data Factory, etc.), standards (NIST 800-53, FISMA, Section 508, WCAG 2.1 AA where applicable), and regulations cited as relevant
- **Quality assurance / quality control** — how [Firm] ensures deliverable quality
- **Risk identification and mitigation** — 1-3 risks per task with concrete mitigation plans
- **Innovation** — where [Firm]'s approach differs from standard practice (subtle — overdone reads as inexperience)
- **Diagrams** — process flow, architecture, or data flow diagrams with action captions

Action caption pattern: Every diagram has a caption that delivers the diagram's point on its own. Evaluators scan; captions that just label the figure get skipped.

#### C. Management Plan

- **Organization chart** — [Principal] as Principal/Project Manager, [GIS Subcontractor] as GIS subcontractor (if applicable), any other named team members
- **Key personnel resumes** — name, role, education, certifications, relevant experience, % time commitment. Resumes go in appendix; here, summarize.
- **Schedule** — Gantt or table format. Phases, milestones, deliverables, dates. Realistic, not aggressive.
- **Contract administration** — billing cadence, invoice format, communication protocols
- **Staffing approach** — base team + named subs + Additional Capacity description
- **Succession planning** — what happens if key personnel become unavailable

#### D. Past Performance

3-5 CCARs from `references/ccar-bank.md`. For each:

- Project title, client, contract number (if federal), period of performance
- Contract value
- 2-3 sentence narrative in CCAR format
- CPARS rating (if federal and rating issued)
- Reference contact (verified willing)
- **Relevance to [Agency]:** callout linking this project to specific Section M evaluation factor

Lead with most relevant, not most impressive. For [Firm] today, [Federal Intermediary] leads for federal-grant-related work; $[REDACTED]M pipeline leads for enterprise BI delivery; [Federal Grantee] supports for smaller-scale federal grantee work.

### Volume 3 — Cost / Price Proposal

#### A. Cost Summary

Total proposed price with breakdown by:
- Direct labor
- Fringe
- Overhead
- G&A
- Materials
- Subcontracts
- Travel
- Other Direct Costs (ODCs)
- Fee / Profit

#### B. Direct Labor Breakdown

Table by Labor Category (LCAT):
- LCAT name (e.g., "Senior Data Analyst," "GIS Analyst")
- Hours per task / total
- Unloaded hourly rate
- Loaded hourly rate (with fringe + overhead + G&A)
- Total cost per LCAT

#### C. Fringe / Overhead / G&A Rates

For small firms without DCAA-approved rate agreements:
- Provide rate calculations with basis (historical data, market benchmarks)
- Cite federal cost principles (FAR Part 31)
- Be prepared for cost realism review

Typical small-firm structure:
- Fringe: 25-30% of direct labor
- Overhead: 25-40% of direct labor + fringe
- G&A: 10-20% of all costs (or as a percentage of total cost input)

#### D. Subcontracts

For [GIS Subcontractor] (GIS) or other subcontractors:
- Sub name, role, scope
- Hours × rate
- Basis of estimate
- Pass-through fee (if any)

#### E. Travel

If CONUS travel anticipated:
- Trip purpose, destination, duration
- Per diem (current GSA rates)
- Airfare estimate
- Total travel cost

#### F. Other Direct Costs

- Software licenses (Power BI Pro, Microsoft 365, etc.)
- Materials, supplies
- Anything not direct labor

#### G. Fee / Profit

- 5-10% on cost-type
- Higher on FFP (Fixed Price)
- Risk-adjusted

#### H. Basis of Estimate

Narrative explaining how cost estimate was developed:
- Labor hour estimates derived from comparable past performance
- Labor rates supported by current salary surveys, prior contract awards, or historical data
- Indirect rate basis (if not DCAA-approved, show calculation)
- Travel estimates per GSA tables
- Subcontract pricing supported by sub quotes

### Volume 4 — Representations and Certifications (Reps & Certs)

Standard certifications required for federal civilian:

- **SAM.gov entity registration current**
- **Small business size status** per NAICS
- **Tax compliance**
- **Executive compensation disclosure** (if applicable per FAR 52.204-10)
- **Organizational Conflict of Interest (OCI) disclosure**
- **Lobbying certification**
- **Debarment / suspension representation**
- **Affirmative action / equal opportunity compliance**
- **Section 508 accessibility compliance** (where applicable)
- **Cybersecurity / NIST 800-171 compliance** (where applicable)
- **Buy American / Trade Agreements compliance** (where applicable)
- **8(a) status** (if certified)

Each cert signed and dated by authorized signatory.

### Volume 5 — Past Performance (separate volume for larger bids)

For larger federal bids, past performance may be requested as a separate volume rather than as a section of the technical proposal. In that case:

- Each project gets its own page
- Standard CPARS information (if federal contract)
- Reference contact (verified)
- Quantified outcomes
- "Relevance" callout

## Federal-Specific Voice Considerations

Federal proposals can read slightly more formal than state/regional proposals, but [Firm]'s core voice rules still apply:

- Active voice
- Concrete actions over vague commitments
- Banned phrases still banned
- Contractions still acceptable (most federal proposals use them)
- Sentence-length variation

What changes for federal:
- More acronym definitions on first use (FAR, NIST, CPARS, etc.)
- More citation of regulations, standards, frameworks
- More risk language (federal evaluators reward identified risks with mitigations)
- More formal structure (numbered sections, subsections)

## Common Federal Proposal Mistakes [Firm] Should Avoid

1. **Over-promising scope.** Federal evaluators discount aggressive claims. Realistic is better than ambitious.

2. **Ignoring Section M weights.** If Past Performance is weighted 40% and Technical Approach is weighted 30%, the proposal should reflect that emphasis.

3. **Treating Section L as guidelines.** Page limits, font, margin, file naming — all enforced. Misses = disqualification.

4. **Generic past performance.** "We have analytics experience" is generic. "[Firm] operated $[REDACTED]M federal program analytics for [Federal Intermediary]" is specific.

5. **Marketing language.** "Cutting-edge," "innovative," "comprehensive" — banned in [Firm] voice generally, and especially in federal proposals where they signal generic vendor.

6. **Inconsistent voice across volumes.** Cost narrative often gets contracted out and ends up reading different from technical proposal. Edit for voice consistency.

7. **Submitting at the last minute.** Federal submission portals have rejected submissions for being one minute late. Submit with hours of buffer.

8. **Missing reps & certs.** Easy to overlook. Every federal proposal needs them; missing them = disqualification.

## Attribution

Structural scaffolding (Section L/M/C mapping, multi-volume organization, FAR-aligned cost elements) adapted from CaseMark `rfp-response` skill, available at https://agentskills.legal/skills/rfp-response under Apache 2.0 License. [Firm]-specific content (voice rules, win themes, CCARs, agency patterns) is original.
