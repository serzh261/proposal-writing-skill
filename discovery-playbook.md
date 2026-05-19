# Discovery Playbook — Patterns and Search Strategies

Detailed playbook supporting `modes/discovery.md`. Use this when running the seven discovery checks and you need specific search strategies, tool sequences, or example queries.

## Tool Sequencing

**Default: web_fetch first.** Fast, cheap, retrieves rendered content for most static pages.

**Escalate to Claude in Chrome when:**
- web_fetch returns thin content (page is JS-rendered with React/Vue/Angular)
- You need to interact with a search interface (procurement portal filter, USASpending search builder)
- You need to take a screenshot for visual analysis (existing dashboard, page layout)
- The site has authentication that javascript handles client-side

**For RFP PDFs uploaded by [Principal]:** read directly from the upload path, don't try to fetch the PDF from the buyer's website unless [Principal] needs the source URL captured.

## Search patterns by check

### 1. Buyer website pass

Start with the buyer's homepage. Look for:
- "About" / "Mission" page
- "Strategic Plan" / "Annual Report" — usually under About or News
- News / Press Releases — what's the buying unit doing this year?
- Org chart or "Leadership" page
- Department / unit pages for the specific buying unit

**Search queries (Google):**
- `site:[buyer-domain] strategic plan`
- `site:[buyer-domain] [buying unit name]`
- `site:[buyer-domain] dashboard OR analytics OR data`

### 2. Technology stack discovery

The [Regional Council] and [State University] wins both depended on getting this right. Spend extra time.

**Direct site searches:**
- `site:[buyer-domain] "Power BI"`
- `site:[buyer-domain] "Tableau"`
- `site:[buyer-domain] "Microsoft Fabric"`
- `site:[buyer-domain] "Azure"`
- `site:[buyer-domain] "AWS"`
- `site:[buyer-domain] "Snowflake"`
- `site:[buyer-domain] "ArcGIS"`

**Job postings (huge signal):**
- LinkedIn: `[buyer name] Power BI` (active job postings tell you stack)
- The buyer's careers page directly
- Indeed / Glassdoor for the buyer

**Public dashboards / data products:**
- Visit any public-facing dashboard the buyer hosts
- View page source or right-click on visuals to identify the tool (Power BI's `app.powerbi.com` URLs, Tableau's `tableau.com/views/` URLs, etc.)
- Take screenshots for stack identification

**IT vendor pages:**
- Many state/local agencies list approved vendors
- Check `[buyer]/IT` or `[buyer]/procurement` for software contracts

**Implications for proposal:**
- Buyer uses Microsoft → [Firm]'s Microsoft-native stack becomes a fit signal worth foregrounding
- Buyer uses Tableau → either position around it ("we can ingest from Tableau and produce parallel Power BI environments") or de-prioritize the stack-fit angle
- Buyer uses Snowflake/Databricks/non-Microsoft cloud → name how [Firm] interoperates, but don't claim deep native expertise [Firm] doesn't have
- No clear stack → propose Microsoft direction and explain why; frame it as "we'll align to your direction during Phase 1"

### 3. Predecessor product / incumbent hunt

**For state/local agencies:**
- Check procurement portal for past awards in similar NAICS or scope
- Search archived RFPs (many state portals keep these public)
- Look for "current vendor" references in the RFP itself

**For federal:**
- USASpending.gov — search by recipient name, NAICS, or agency
- FPDS-NG (Federal Procurement Data System) — more detailed contract data
- Beta.SAM.gov for active contracts

**For higher-ed:**
- Search the institution's site for the predecessor product's name (e.g., a legacy reporting product the institution has used for years)
- IT services pages often list supported products
- Past board presentations or strategic plan documents may name predecessor products

**For regional councils:**
- The council's site usually lists current vendors/partners
- Annual reports name technology partners

**Search queries:**
- `[buyer name] vendor OR contractor OR consultant`
- `[buyer name] partners`
- `[buyer name] "implemented by" OR "built by" OR "developed by"`

Even when you can't identify a specific incumbent, identify the *type* of vendor likely to be the incumbent (e.g., "small [Metro] IT consultancy" vs. "large federal prime"). This shapes positioning.

### 4. Decision-maker research

**Contracting officer:**
- The RFP names the CO. Search LinkedIn for that name + the agency.
- Background: prior agencies, prior roles, length of tenure
- Recent posts: signal what they care about

**Program owner:**
- For state/regional, often named in the RFP scope section
- For federal, usually named as a technical POC
- LinkedIn for background

**Don't try to identify evaluation committee members.** Direct contact during the bid period is prohibited, and pretending to know specific evaluators is worse than not knowing.

### 5. Political and strategic context

**Search queries:**
- `[buyer name] strategic plan 2025 OR 2026`
- `[buyer name] board meeting [recent date]` (board minutes often reveal mandates driving RFPs)
- `[buyer name] press release [recent date]`
- `[buyer name] new director OR new leader` (leadership changes often trigger RFPs)
- For federal: agency budget submissions, OMB pass-back, agency strategic plans
- For higher-ed: BoR meeting minutes, accreditation reviews
- For state: legislative committee reports, audit findings

**Why now signals:**
- Strategic plan milestone arrived
- Federal funding deadline
- Audit finding requiring corrective action
- New leadership setting priorities
- Adjacent procurement just closed (sequencing tells you about the broader strategy)

### 6. Comparable awards

**For state/local:**
- The procurement portal usually shows past awards with vendor and value
- Some states have public bid tabulations

**For federal:**
- USASpending.gov: search by NAICS + agency + date range
- FPDS-NG for detailed contract structure
- Award announcements (press releases, federal grant databases)

**Use comparable awards to anchor pricing.** If similar work paid $60K-$90K, $78K-$95K is defensible. If similar work paid $400K, $80K looks unserious.

## RFP-specific research patterns

When the RFP itself is the primary source, extract these signals:

**Section L / "Required Proposal Contents":**
- Section structure they want — mirror this exactly
- Page limits — these are mandatory
- Format requirements (font, margin, line spacing)
- Submission method (PDF, portal, email, multi-file)

**Section M / "Evaluation Criteria":**
- Each factor and its weight if given
- Sub-factors
- Pass/fail criteria

**Section C / "Statement of Work":**
- Every task and deliverable
- Period of performance
- Place of performance
- Government-furnished property

**Throughout:**
- Specific terminology and acronyms the agency uses — mark for mirror
- Specific frameworks, standards, regulations cited — verify currency
- Specific tools or platforms named — fit to [Firm]'s stack

## Discovery brief template

After completing all checks, produce the brief in this format (from `modes/discovery.md`):

```
DISCOVERY BRIEF — [Solicitation Number]

BUYER
DECISION-MAKERS
TECHNOLOGY STACK
PREDECESSOR / INCUMBENT
EVALUATION CRITERIA
REQUIRED PROPOSAL SECTIONS
LANGUAGE TO MIRROR
COMPARABLE AWARDS
WIN THEMES (candidates)
DISCRIMINATORS THAT APPLY
CAPABILITY GAPS
OPEN QUESTIONS FOR BUYER
SAMPLE ARTIFACT OPPORTUNITY
```

Save this to the working directory. It feeds compliance matrix, gap analysis, and drafting.

## Time budgets

- RFI response: 20-30 minutes discovery
- State/regional bid ([Regional Council]-sized): 45-90 minutes discovery
- Higher-ed bid (UM-sized): 60-120 minutes discovery
- Federal civilian bid: 2-4 hours discovery
- Federal CSO/BAA: 4-8 hours discovery

If you're going meaningfully past these, something's wrong with the search strategy. Stop, summarize what you have, and ask [Principal] what's missing.
