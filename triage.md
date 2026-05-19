# Mode: Triage (Go / No-Go)

Use this mode when [Principal] pastes an opportunity, RFP, or solicitation and asks whether it's worth bidding. The output is a structured verdict he can act on in under five minutes.

## What triage costs

Roughly 5-15 minutes of model time per opportunity. Cheaper than spending 40-80 hours on a no-win bid. The goal is to either kill the opportunity early or hand off to full-lifecycle mode with a clear win logic.

## Process

### Step 1 — Read what's in front of you

Read the opportunity carefully before searching the web. Extract:

- Title, solicitation number, agency/buyer
- Award type (RFP, RFQ, RFI, BAA, CSO, sole-source, set-aside)
- Estimated value if stated
- Due date (proposal and any questions deadline)
- NAICS code and size standard
- Set-aside designation (small biz, 8(a), WOSB, HUBZone, full and open)
- Eligibility restrictions (LEA/SAA only, nonprofit only, Title IV-E partnership, clearance required, past performance threshold)
- Scope summary in two sentences
- Evaluation criteria (Section M) if visible

If the opportunity is just a one-line description from [Principal]'s pipeline, ask him to paste the actual posting before proceeding. Triage without the source document is guessing.

### Step 2 — Apply the hard eligibility check (binary)

Any single fail here = NO-GO, full stop, no need to continue.

- For-profit allowed? ([Firm] is for-profit LLC)
- NAICS in 541611, 541512, 541690 or adjacent? (or does the size standard fit?)
- Agency-type restrictions: does the RFP exclude commercial firms? (HHS BAAs often exclude for-profits; FEMA PRPA is LEA/SAA only; EPA water training excludes for-profits)
- Clearance required? ([Firm] has none — DoD/IC bids are no-go as prime)
- Past-performance threshold? (Some federal RFPs require 3+ prior federal primes — [Firm] has zero completed federal primes yet)
- Facility security clearance? (None)
- Geographic restriction? (Some state contracts require in-state registration)

If hard eligibility passes, continue.

### Step 3 — Apply the five-condition hiring-to-bid framework

Load `references/hiring-to-bid-framework.md`. Score each of the five conditions:

1. Eligibility open to for-profits (already checked above; binary)
2. [Firm]'s core capability is the scope's center of gravity
3. [Firm] has adjacent past performance to anchor the narrative
4. Hire cost is recoverable within the award
5. The clock fits

Each condition: PASS / FAIL / MAYBE. If any single condition fails, the default is no-go — but flag the condition so [Principal] sees what would have to change.

### Step 4 — Quick win-probability assessment

Estimate based on:

- **Incumbent presence.** Run a quick search: is there a current contractor on this work? If yes, what's their weakness? Note: ~40-60% of federal procurements have a preferred vendor before the RFP drops — be honest about this.
- **Set-aside designation.** Small business / 8(a) / WOSB set-asides shrink the competitive pool dramatically.
- **Buyer relationship.** Warm = existing [Regional Council] relationship, prior conversation. Cold = first contact with this agency.
- **Working sample feasibility.** Can [Firm] build a credible working dashboard or artifact in the timeline? If yes, that's a Tier 1 discriminator. If no, win probability drops.
- **Competition density.** Sole-source RFI vs. open competition vs. small-biz set-aside.

Bucket the result: **Low (5-15%)** / **Medium (15-35%)** / **High (35%+)**.

For first-time-buyer / no-incumbent-relationship / open-competition bids, the realistic ceiling is Medium. Don't inflate.

### Step 5 — Effort and EV math

Estimate proposal hours:

| Type | Hours |
|---|---|
| RFI response | 8-20 |
| State/regional RFP ([Regional Council]-sized) | 40-80 |
| Higher-ed RFP (UM-sized) | 40-80 |
| Federal civilian RFP | 80-200 |
| Federal CSO/BAA | 100-300+ |

Compute net EV:

```
Expected award value × P(win) − proposal cost = net EV

Proposal cost = ([Principal]'s effective hourly rate × proposal hours) + any out-of-pocket
                (subcontractor proposal effort, software, graphics, etc.)
```

Use [Principal]'s effective rate at ~$[REDACTED]/hr as the opportunity cost of his time (matches [Regional Council] pricing).

If net EV is negative, surface the number plainly. Don't argue. [Principal] may still want to bid for strategic reasons (federal past performance, agency relationship, etc.) and that's his call.

### Step 6 — Issue the verdict

Use `templates/triage-verdict.md` as the output structure.

**GO:** All hard eligibility passes, hiring-to-bid framework passes, win probability is Medium or higher, net EV positive OR [Principal] has a strategic reason to bid despite negative EV.

**NO-GO:** Hard eligibility fails, OR hiring-to-bid framework has 2+ fails, OR net EV is meaningfully negative with no strategic justification.

**MAYBE:** Need specific intel before deciding. List exactly what's missing (Q&A submission, clarification call, buyer research) and what would flip it to GO or NO-GO.

### Step 7 — If NO-GO, prepare a blocklist entry

Format per `references/blocklist-format.md`. Show it to [Principal] and ask him to confirm before treating it as final. Never assume he wants it logged.

### Step 8 — If GO, hand off

End the triage with a clear next step:

- "Want me to start full discovery on this? Will take ~30 minutes."
- Surface any questions to submit to the buyer before the Q&A deadline (these matter — Q&A signals engagement and gets you intel)
- Flag the most important capability gap to source first (if any)

## Anti-patterns to avoid

- **Don't soft-pedal a no-go to avoid disappointing [Principal].** He values honesty over comfort. A skill that lets him chase bad bids costs him real money.
- **Don't pretend you know the incumbent without searching.** If you don't know, search USASpending.gov, the agency procurement portal, or recent award announcements. If you can't find it, say so.
- **Don't skip the hard eligibility check because the rest looks good.** A great-fit RFP that excludes for-profits is still zero percent win probability.
- **Don't inflate win probability because [Principal] wants to bid.** If you're talking yourself into Medium when the honest answer is Low, you're not helping.
- **Don't issue MAYBE as a fence-sit.** MAYBE means "specific intel would change my answer" — name the intel. If you can't name it, the answer is GO or NO-GO.
