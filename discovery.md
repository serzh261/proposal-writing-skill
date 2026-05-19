# Mode: Discovery

Discovery is the hard gate before any drafting. The [State University] bid worked because we found out they used Microsoft Fabric, they had a predecessor product ([legacy reporting product]), and [Internal Analytics Office] was driving the project. Generic proposals lose.

Use this mode when [Principal] says "research this buyer," when he's starting a proposal, or when triage has issued a GO and the next step is to understand who's buying.

## What discovery produces

A short discovery brief (1-2 pages of notes) covering:

1. **Buyer profile** — what they do, mission language they use, recent strategic plans
2. **Decision-makers** — contracting officer, program owner, evaluation committee if identifiable
3. **Technology stack** — what BI/cloud/analytics tools they actually use
4. **Predecessor product / incumbent** — what exists today, who built it, what's wrong with it
5. **Political/strategic context** — why this RFP, why now
6. **Comparable awards** — what they paid last time, who won
7. **Geography/community** (for regional councils) — member jurisdictions, local dynamics
8. **Mirrored language** — exact phrases from their website, strategic plan, RFP to use in the proposal

That brief feeds directly into win-theme selection, sample-artifact design, and language mirroring in the draft.

## Tool sequence

Start with **web_fetch** (faster, cheaper). Escalate to **Claude in Chrome** only when:

- A page is JS-rendered and web_fetch returns thin content
- You need to interact with a search interface (procurement portal search, USASpending filter)
- You need to take a screenshot of an existing dashboard, page layout, or visual artifact

The [Regional Council] and [State University] discovery work used Chrome heavily for buyer-website navigation. Don't be afraid to use it — just lead with web_fetch and escalate.

## The seven discovery checks

Run these in order. Each one builds on the previous.

### 1. Read the RFP source documents end-to-end first

Before searching anything externally, extract from the solicitation:

- All evaluation criteria (Section M for federal, equivalent section for state/regional/higher-ed)
- Required proposal contents and section structure (Section L for federal)
- Statement of work (Section C for federal) — every task, every deliverable
- Required attachments (debarment certifications, affirmative action checklists, reps & certs)
- Deadlines (Q&A, proposal due, evaluation period, award date, period of performance start)
- Submission format (PDF, portal upload, email, page limits, font requirements)
- Specific terminology the agency uses (mirror this verbatim later)

Extract their *exact wording* on what they want. The proposal will quote it back.

### 2. Buyer website pass

Visit the buyer's main site. Look for:

- Mission statement, strategic plan, annual report — the language they use about themselves
- Org chart and the specific unit that owns this RFP
- News/press releases — what's the unit currently doing that connects to this RFP?
- Existing dashboards, data products, or publications that overlap with the scope
- Vendor/partner pages — who do they already work with? Who's the incumbent likely to be?
- Careers page — IT and analytics job postings reveal the stack. A job posting for "Power BI developer" tells you everything.

The [Regional Council] site told us they used Microsoft tools and had an existing operational framework. The [State University] site told us about the buyer's legacy products, internal analytics office,, and the buyer's stated tech direction.

### 3. Technology stack discovery

Look hardest here — this is the part most competitors skip.

- Search the buyer's domain for "Power BI," "Tableau," "Qlik," "Azure," "AWS," "Snowflake," "ArcGIS"
- Check IT job postings (LinkedIn, the buyer's careers page) for required tools
- Look at any public dashboards they publish — screenshot them, identify the tool by visual signature
- Check procurement archives for past software contracts (state/local agencies often publish these)
- For higher-ed: check the IT website for "supported software" or "data governance" pages

If they use Microsoft → [Firm]'s Microsoft-native stack becomes a fit signal worth mirroring in the proposal.
If they use Tableau → don't pretend otherwise. Position around it ("we can ingest from Tableau and produce parallel Power BI environments") or down-weight the stack fit.

### 4. Predecessor product / incumbent hunt

Almost every RFP is replacing or extending something. Find it:

- Search "[buyer name] dashboard" / "[buyer name] reporting"
- Check the buyer's site for existing public-facing data products
- For federal: search USASpending.gov for prior contracts in this NAICS at this agency
- For state/local: check the agency's procurement archive
- For higher-ed: check the institution's research/data services pages

If there's an incumbent, ask: what would the evaluator's frustration with the incumbent look like? Then the proposal positions against that specific weakness, not against generic competitors.

If there's a predecessor product (like [State University]'s [legacy reporting product]), reference it explicitly in the proposal. It signals you did the homework and demonstrates depth other bidders won't have.

### 5. Decision-maker research

Contracting officer and program owner names are usually in the RFP. LinkedIn them.

- Background (federal career, prior agency, private sector before government)
- Recent posts or articles — signal what they care about
- Mutual connections worth name-dropping (carefully) in cover letter

For evaluation committees, you usually can't identify members in advance. Don't try to.

For regional councils ([Regional Council]) and state/local agencies, the program owner is often public and findable. Use that.

### 6. Political and strategic context

Why is this RFP happening *now*? Strong signals:

- Recent board mandate, strategic plan milestone
- Federal funding cycle (grant deadlines, FY end)
- Audit finding or public commitment driving urgency
- Recent leadership change in the buying unit
- Adjacent procurements (an RFP for "data warehouse" right before an RFP for "dashboard" tells you about sequencing)

The [Regional Council] bid happened because they needed analytics capacity ahead of a coming planning cycle. The [State University] bid happened in the Microsoft Fabric transition context. Knowing the why lets you write the proposal as the answer.

### 7. Comparable awards

For state/local: their procurement portal usually shows past awards. Look at award value and winning vendor.

For federal: USASpending.gov, FPDS-NG (Federal Procurement Data System). Search by NAICS + agency for the past 2-3 years.

This anchors pricing. If similar work paid $60K-$90K last time, $78K-$95K is defensible. If similar work paid $400K, undercharging at $80K looks unserious.

## Output format

End discovery with a structured brief. Use this skeleton:

```
DISCOVERY BRIEF — [Solicitation Number / Title]
Date: [today]

BUYER
- Name, location, mission language
- Owning unit + program owner
- Strategic context (why now)

DECISION-MAKERS
- Contracting officer: [name, background]
- Program owner: [name, background, LinkedIn observations]

TECHNOLOGY STACK
- Confirmed tools: [list with source]
- Likely platform direction: [inference + reasoning]
- Implications for our positioning: [bullets]

PREDECESSOR / INCUMBENT
- Existing product: [name + description]
- Vendor (if known): [name + why they may be vulnerable]
- Evaluator likely frustrations: [bullets]

EVALUATION CRITERIA (from RFP)
- [Each criterion verbatim, with weight if given]

REQUIRED PROPOSAL SECTIONS
- [Per Section L or equivalent]

LANGUAGE TO MIRROR
- [List of exact phrases from RFP, buyer website, strategic docs to use verbatim in the proposal]

COMPARABLE AWARDS
- [Prior contract, vendor, value if findable]

WIN THEMES (candidates anchored to Section M)
- [3-5 candidate themes, each linked to a specific evaluation criterion]

DISCRIMINATORS THAT APPLY HERE
- [Which of [Firm]'s Tier 1/2 discriminators map to this bid — see references/win-themes-discriminators.md]

CAPABILITY GAPS TO ADDRESS
- [What scope elements [Firm] can't cover with current bench]
- [→ route to gap-analysis.md if non-trivial]

OPEN QUESTIONS FOR THE BUYER
- [Questions worth submitting in Q&A period — usually 2-3 max]

SAMPLE ARTIFACT OPPORTUNITY
- [Is a working sample dashboard/mockup feasible in this timeline? What would it show?]
```

Once the brief is complete, ask [Principal]: "Discovery done. Want to move to compliance matrix and start drafting, or want me to refine anything in this brief first?"

## Anti-patterns to avoid

- **Don't skip technology stack discovery.** This is the single highest-ROI piece. The [State University] bid was won partially because we knew about Microsoft Fabric before drafting.
- **Don't make claims about the buyer without citing the source.** "[Regional Council] uses Microsoft" needs to be tied to a specific page or job posting.
- **Don't try to identify evaluation committee members.** Procurement law prohibits direct contact during the bid period, and pretending you know specific evaluators is worse than not knowing.
- **Don't research forever.** 30-60 minutes for a mid-sized bid is appropriate. Half a day for a major federal bid. If you're going past that, something's wrong with the search strategy.
- **Don't draft until discovery is complete.** Hard gate. If [Principal] pushes, ask: "What we know so far is X, Y, Z. Want me to draft on what we have, or finish discovery first?" His call, but make him see what's missing.
