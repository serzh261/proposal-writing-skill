# Color Team Review Checklists

Detailed checklists supporting `modes/reviews.md`. [Firm] runs Red Team (content + win themes) and Gold Team (executive polish + submission readiness). Pink Team (compliance) overlaps too much with the compliance matrix for a solo shop and is skipped.

## Red Team Review Checklist

**Timing:** Draft is 60-70% complete. Significant rewrites still possible. Run 5-7 days before submission for most state/regional bids; 10-14 days for federal.

**Time investment:** 60-90 minutes for state/regional bid; 2-3 hours for federal civilian.

### 1. Compliance Walk

Walk the compliance matrix end-to-end. For each row:

- [ ] Is the requirement addressed in the proposal?
- [ ] Is it addressed in the right section (matches what the RFP asks)?
- [ ] If MANDATORY, is it unambiguously addressed?
- [ ] Are all required attachments listed in the table of contents?

Flag every miss. Compliance misses get fixed before anything else.

### 2. Win Theme Audit

For each major section (Executive Summary, Methodology, Past Performance, Staffing):

- [ ] Is there a clear, articulated win theme?
- [ ] Does the theme anchor to a specific Section M evaluation criterion (or equivalent)?
- [ ] Does the theme name a discriminator (Tier 1 or Tier 2) or strength?
- [ ] Is the theme supported by concrete proof (past performance, sample, named partner, quantified outcome)?
- [ ] Is the theme repeated across sections so evaluators hear it multiple times?

Sections without clear win themes should be rewritten. A section that just describes what [Firm] does, without tying it to what the buyer is evaluating, scores lower.

### 3. Discriminator Visibility

- [ ] Working sample (if applicable) — referenced in Executive Summary?
- [ ] Working sample (if applicable) — featured in Work Samples section with caption?
- [ ] [Federal Intermediary] $[REDACTED]M past performance (if federal-adjacent) — leads Past Performance section?
- [ ] [metro-local] presence (if regional bid) — visible in Firm Overview?
- [ ] 8(a) status (once certified) — disclosed in Firm Overview / Reps & Certs?

If a discriminator is buried in a later section, foreground it. Discriminators belong in the Executive Summary or first paragraph of the relevant section, not page 12.

### 4. Language Mirror Check

Pull the "Mirror Language" column from the compliance matrix (or the language list from the discovery brief). For each phrase:

- [ ] Is the exact RFP phrase present in the proposal where relevant?
- [ ] Or did the draft paraphrase ("operational dashboard" instead of "common operating picture")?
- [ ] Are agency-specific acronyms used correctly?
- [ ] Is the buyer's strategic-plan language reflected in the Executive Summary?

Replace every paraphrase with the agency's exact terminology.

### 5. CCAR Defensibility

For every past performance entry:

- [ ] Is every dollar amount defensible? Could you back it up if challenged?
- [ ] Are dates and timeframes accurate?
- [ ] Are reference contacts verified willing to serve as references?
- [ ] Is every `[VERIFY:]` flag from the CCAR bank resolved?
- [ ] If quantified outcomes are claimed (%, $, count), are they real?

Any uncertain detail must be either confirmed by [Principal] or removed from the proposal. CCARs that fabricate specifics get firms disqualified or worse — false certifications can trigger debarment.

### 6. Voice and AI-Tell Check

Run the proposal text through the voice rules in `references/voice-and-tone.md`:

- [ ] Search for each banned phrase. None should appear:
  - delve, leverage, unlock, comprehensive, game-changer
  - "in today's digital age"
  - "X isn't just about Y" / "X is not just Y"
  - utilize (when "use" works), facilitate (when "help" works)
  - foster, holistic, synergy, cutting-edge, state-of-the-art, world-class, best-in-class
  - strive to, endeavor to, empower
- [ ] Contractions present throughout (we'll, it's, we're, won't)?
- [ ] Sentence-length variation? (No paragraph of all 15-word sentences)
- [ ] Active voice dominant?
- [ ] Concrete actions instead of vague commitments ("we'll embed with [Regional Council] staff from day one" instead of "we will ensure consistent engagement")?

Flag every instance with the sentence and a suggested rewrite.

### 7. Lead-With-Buyer Check

For each section's opening paragraph:

- [ ] Does the first sentence reference the buyer's world, not [Firm]?
- [ ] Is the buyer's problem named before [Firm]'s solution?
- [ ] Could this opening paragraph be on any consulting firm's proposal, or is it specific to this buyer?

Generic openings are the most common Red Team finding. Rewrite to lead with the buyer.

### 8. Pricing Sanity Check

- [ ] Does the fixed fee anchor against comparable awards from discovery?
- [ ] Is the cost breakdown clear (task / hours / rate / who / cost / %)?
- [ ] Is subcontractor cost separated as a line item?
- [ ] Is the rate note brief (not AI-sounding pricing justification)?
- [ ] Does the cost align with the buyer's typical budget for this scope?

### Red Team Output Format

Provide [Principal] a structured findings list:

```
RED TEAM FINDINGS — [Proposal Name]

CRITICAL (do-or-fail before submit):
- [Finding 1, section, rewrite suggestion]
- [Finding 2 ...]

IMPORTANT (will reduce evaluator score):
- [Finding 1 ...]

POLISH (improves but won't disqualify):
- [Finding 1 ...]

ESTIMATED REWRITE EFFORT: [hours]
```

---

## Gold Team Review Checklist

**Timing:** 24-48 hours before submission. Draft is final or nearly final.

**Time investment:** 30-60 minutes.

### 1. Format and Submission

- [ ] Page limits respected for every section (with page numbers verified)
- [ ] Font matches RFP requirement (Times Roman 12pt or whatever specified)
- [ ] Line spacing matches RFP requirement
- [ ] Margins match RFP requirement
- [ ] Headers and footers per RFP (if specified)
- [ ] Required cover page populated, no placeholders
- [ ] File format correct (PDF? Specific PDF/A version? Multi-file vs. single?)
- [ ] File naming per RFP (some federal RFPs specify exact filenames)
- [ ] Submission method confirmed (email vs. portal vs. courier)
- [ ] Submission address correct (CO email, alternate contact)
- [ ] Deadline confirmed in correct timezone

### 2. Compliance Matrix Final Pass

Walk the compliance matrix one more time. Any row still marked "in progress" or "not started":

- [ ] Resolved?
- [ ] Or formally removed from scope with rationale documented?

If anything is still unresolved within 24 hours of submission, it's a critical issue.

### 3. Cover Page and Executive Summary

These are the highest-impact pages. Read them aloud.

- [ ] Cover page: all fields populated, no placeholders, contact info verified correct
- [ ] Executive summary: opens with buyer problem, names discriminators, fee and timeline visible
- [ ] Executive summary fits within page limit
- [ ] Executive summary has no AI tells (banned phrases, monotone sentence structure)
- [ ] Executive summary is signed (if cover letter format) by authorized signatory

### 4. References Verification

- [ ] All three references verified willing within last 30 days
- [ ] Names, titles, phone numbers, emails correct
- [ ] No placeholders ("TBD", "to be added", "[reference 1]")
- [ ] References still in their roles (people leave jobs — verify currency)

### 5. Signatures and Certifications

- [ ] Debarment certification (Attachment B) signed and dated
- [ ] Affirmative action checklist (Attachment A) completed or N/A statement included
- [ ] Reps & Certs (federal) completed
- [ ] Insurance certificates (if required) attached
- [ ] Authorized signatory has actual binding authority
- [ ] All signatures are in ink or digitally signed (per RFP requirement)

### 6. Attachments Inventory

- [ ] All required attachments included
- [ ] All listed in table of contents (if used)
- [ ] Attachment names match references in proposal body
- [ ] Resumes (Appendix A) included for all named key personnel
- [ ] Work sample (Appendix B or C) included if referenced
- [ ] No extra attachments that aren't requested (some RFPs penalize extras)

### 7. Final Read Aloud

Read the following aloud, looking for anything that doesn't sound right:

- [ ] Executive summary, beginning to end
- [ ] Each methodology task's opening paragraph
- [ ] Each past performance entry
- [ ] Cost proposal table and rate note

Flag any sentence that doesn't sound like a human consultant talking, doesn't fit the [Firm] voice, or feels off.

### 8. Submission Logistics

- [ ] Email draft prepared (if email submission) with correct subject line and body
- [ ] Portal upload tested (if portal submission) — confirmed the upload works and the proposal renders
- [ ] Backup copy saved
- [ ] Submission scheduled for delivery with buffer time (don't submit at the last minute)
- [ ] Confirmation receipt expected (and method to capture it)

### Gold Team Output Format

Short structured checklist:

```
GOLD TEAM SUBMIT-READY CHECK — [Proposal Name] — [Submit Date]

✅ Format compliant (font, margin, spacing, page limit)
✅ All required sections present
✅ All attachments signed and included
✅ References verified within 30 days
✅ No placeholders remaining
✅ Submission method confirmed
✅ Deadline confirmed in correct timezone
✅ Cover page populated
✅ Executive summary tight and on-voice

⚠️ REMAINING ITEMS:
- [Any items still ⚠️ — must resolve before submit]

SUBMIT-READY: YES / NO
```

If SUBMIT-READY = NO, list exactly what must be resolved and by when.

---

## When [Principal] pushes back on a finding

Take corrections seriously. Don't argue past a [Principal] correction. But also: ask whether the disagreement is about *this finding* or about *the underlying rule*. If it's the rule (voice, win-theme structure, compliance approach), suggest a specific edit to the relevant reference file so the next bid doesn't surface the same friction.
