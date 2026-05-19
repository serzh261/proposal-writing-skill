# Blocklist Format

When triage issues a NO-GO, format an entry for [Principal]'s `opportunity_matcher.py` blocklist. Ask [Principal] to confirm before treating the entry as final — never auto-log.

## Format

The blocklist in `opportunity_matcher.py` is structured by opportunity ID/ALN and reason. Format the entry as a Python-compatible line [Principal] can paste directly:

```python
# Blocked: [Opportunity Title] — [Brief reason]
# Surfaced: [date], Triage verdict: NO-GO, Reason: [one-line]
"[OPPORTUNITY_ID_OR_ALN]": "[concise no-go reason]",
```

## Example entries

```python
# FEMA Preparedness Reporting and Performance Analysis (PRPA) — LEA/SAA only
# Surfaced: 2026-04-15, Triage verdict: NO-GO, Reason: eligibility restricted to law enforcement / state administering agencies
"97.067": "FEMA PRPA — LEA/SAA only, for-profit ineligible",

# EPA Water Training and Technical Assistance — for-profit excluded
# Surfaced: 2026-04-12, Triage verdict: NO-GO, Reason: eligibility explicitly excludes for-profit entities
"66.461": "EPA Water TA — for-profit explicitly excluded",
```

## What to include in the reason

Keep the reason concise (one line, under 80 characters). Reason categories:

- **Eligibility:** `for-profit excluded`, `LEA/SAA only`, `nonprofit only`, `Title IV-E required`, `facility clearance required`
- **Past performance:** `requires 3+ federal primes`, `requires CPARS history`, `requires X years federal contracting`
- **Scope mismatch:** `not analytics — [domain]`, `requires PhD-level [field]`, `requires clinical SME team`
- **Set-aside:** `8(a) only — [Firm] not yet certified`, `WOSB only`, `HUBZone only`
- **Geographic:** `requires in-state firm`, `requires DC presence`
- **Capacity:** `requires X-person team`, `requires Y-year track record`
- **False positive:** `civil construction false positive`, `keyword match in unrelated context`

## What to capture in addition

For [Principal]'s pipeline learning, the blocklist entry should also include in the comment:

- The opportunity ID or ALN
- The opportunity title
- The date it surfaced
- The triage verdict
- The specific reason

This lets [Principal] review the blocklist later and:
1. Verify the no-go was correct
2. Update the matcher's keyword scoring to avoid resurfacing similar opportunities
3. Reconsider if [Firm]'s status changes (e.g., 8(a) certification lands, federal past performance accumulates)

## Confirmation flow

After issuing a NO-GO verdict in triage, show the formatted entry:

```
PROPOSED BLOCKLIST ENTRY (please confirm before logging):

# [Title] — [Reason category]
# Surfaced: [date], Triage verdict: NO-GO, Reason: [reason]
"[ID]": "[reason]",

Confirm to add (y/n)?
```

Wait for [Principal]'s explicit "yes" or equivalent. Then present the entry as final and ready-to-paste into the matcher.

If [Principal] says no — either because he disagrees with the no-go or wants to keep the opportunity in pipeline for future review — surface his reasoning and skip the blocklist add. Don't add silently.

## Edge cases

**Maybe-verdicts:** Don't generate a blocklist entry. MAYBE means "need intel before deciding" — keep the opportunity in pipeline until the intel arrives.

**GO verdicts:** Don't generate a blocklist entry. Obvious, but worth stating.

**Reconsidered no-gos:** If [Principal] wants to revisit a previously-blocklisted opportunity (e.g., once 8(a) certification lands), surface this as a separate "consider unblocking" workflow rather than removing from blocklist silently.

**ALN with multiple programs:** Some ALNs map to multiple programs. If only one program is ineligible, blocklist by opportunity ID instead of ALN to avoid blocking legitimate programs under the same ALN.

## Anti-patterns

- **Don't auto-log without confirmation.** [Principal]'s pushed back on no-gos before, and he should always retain final authority.
- **Don't write vague reasons.** "Not a fit" is useless for future learning. "For-profit excluded — see RFP §1.3" is actionable.
- **Don't blocklist false positives without documenting the keyword issue.** If the matcher surfaced a civil construction RFP by mistake, the blocklist entry should note "civil construction false positive" so [Principal] can also fix the matcher's keyword scoring.
- **Don't blocklist opportunities [Firm] might pursue as a sub.** If the no-go is "can't prime this," consider whether it's a teaming-as-sub candidate before blocklisting. Add a comment if so.
