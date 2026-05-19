# Proposal Writing Skill for Claude

A Claude skill that encodes a full government-proposal lifecycle — from go/no-go triage through final color-team review — as a reusable agentic workflow.

This is a **sanitized template** of a skill I built for my own data consulting practice. Real client names, contact information, pricing, and unverified past-performance figures have been replaced with `[placeholders]` you can fill in for your own firm.

---

## What this is

A modular Claude skill with six operational modes, a knowledge base of agency patterns and reference material, and templates for the most common proposal artifacts. Built to install as a single skill in Claude.ai (or run as a directory in Claude Code) and trigger automatically when you ask anything about a government bid.

## Why I built it

Solo consulting on government contracts is unforgiving. Every wasted proposal is real opportunity cost — 40 to 160+ hours of unbillable work on a bid you shouldn't have pursued. Generic AI assistance produces generic proposals that lose. I needed something that knew my voice, my past performance, my agency relationships, and the math of when *not* to bid.

The skill exists to do three things that generic prompting can't:

1. **Stop no-go bids early.** Hard eligibility checks, a five-condition framework, and explicit expected-value math before any drafting starts.
2. **Encode firm-specific voice and patterns.** Banned-phrase lists, agency contact patterns, past-performance citations (CCARs) — the institutional knowledge that disappears when you start a new chat.
3. **Walk the full lifecycle.** Triage → discovery → gap analysis → compliance matrix → drafting → Red Team → Gold Team. Each step has explicit inputs, outputs, and decision points.

## How it's structured

```
proposal-writing/
├── SKILL.md                          # Entry point and routing
├── modes/                            # Six operational modes
│   ├── triage.md                     # Go/no-go evaluation
│   ├── discovery.md                  # Buyer research
│   ├── gap-analysis.md               # Capability mapping
│   ├── compliance-matrix.md          # Section L/M/C mapping
│   ├── drafting.md                   # Section drafting
│   └── reviews.md                    # Red + Gold team reviews
├── references/                       # Knowledge base
│   ├── voice-and-tone.md             # Voice rules and banned phrases
│   ├── win-themes-discriminators.md  # Shipley-aligned win theme construction
│   ├── ccar-bank.md                  # Past performance citation bank (sanitized)
│   ├── hiring-to-bid-framework.md    # Five conditions for capability gaps
│   ├── discovery-playbook.md         # Buyer research workflow
│   ├── gap-analysis-and-sourcing.md  # Subcontractor sourcing playbooks
│   ├── color-team-checklists.md      # Red + Gold review checklists
│   ├── blocklist-format.md           # Pipeline integration spec
│   ├── federal-rfp-scaffolding.md    # FAR-aligned federal proposal structure
│   └── agency-patterns/              # Per-buyer-type patterns
│       ├── regional-councils.md
│       ├── state-higher-ed-and-agencies.md
│       ├── federal-civilian.md
│       └── sba-8a-pathway.md
└── templates/                        # Output templates
    ├── triage-verdict.md
    ├── compliance-matrix.md
    ├── ccar-template.md
    ├── proposal-skeleton.md
    └── sourcing-outreach.md
```

## Design decisions worth explaining

A few choices that took real thought:

**Triage is a hard gate, not a suggestion.** The skill won't route into drafting mode until a "go" verdict has been issued. Hard eligibility failures (for-profit excluded, clearance required, agency-type restriction) are automatic no-gos regardless of capability fit. This protects against the "I want to bid anyway" failure mode that wrecks small-shop economics.

**No automatic blocklist writes.** Triage produces a ready-to-paste Python blocklist entry when it issues a no-go, but requires manual confirmation before treating it as final. I wanted the audit trail to live with the human, not the agent.

**Pink team review skipped.** The standard Shipley color-team progression is Pink → Red → Gold. I dropped Pink because a solo practitioner doesn't have enough proposal in hand at the Pink stage to make the review worthwhile. Red and Gold are the high-leverage reviews.

**CCARs are tiered by verification status.** Past performance entries are flagged with `[VERIFY:]` tags when numbers came from memory rather than verified records. The skill surfaces those flags rather than hiding them. Unverified claims don't ship in real proposals.

**Discriminator tiers are honest.** The skill separates real discriminators (working samples built per bid, specific federal program past performance) from things consultants like to call discriminators but aren't (Microsoft-native tech stack, direct principal access, fast turnaround). These are strengths, not discriminators — and the skill says so.

**Hiring-to-bid framework is the gap-analysis spine.** When a capability is missing, the framework runs five conditions: (1) eligibility open to for-profits, (2) core capability is the scope's center of gravity, (3) adjacent past performance exists, (4) hire cost recoverable within award value, (5) timeline allows quality proposal. All five must pass for "hire to bid" to be positive expected value.

## How to use it

1. Clone or download this repo
2. Zip the `proposal-writing/` folder
3. Upload to Claude.ai under **Settings → Capabilities → Skills**
4. Replace placeholders throughout with your firm's specifics (search for `[Firm]`, `[Principal]`, etc.)
5. Customize the CCAR bank with your actual past performance
6. Customize agency-patterns files for your target buyers

Once installed, the skill auto-triggers on phrases like *"should I bid on this,"* *"work this bid,"* *"review my proposal,"* etc. No explicit invocation needed.

## What this demonstrates (for anyone evaluating me)

I built this because I needed it. The skill captures things you only learn from doing the work:

- **Agentic workflow design** — routing logic between modes, explicit hand-offs, output templates that compose
- **Prompt engineering at scale** — voice constraints, banned-phrase enforcement, multi-file reference architectures
- **Domain encoding** — Shipley methodology, FAR alignment, agency-specific procurement patterns, set-aside pathways
- **Pipeline integration** — designed to compose with a separate Python opportunity-scoring pipeline (blocklist format spec lives in `references/blocklist-format.md`)
- **Honest evaluation logic** — the skill is built to issue no-gos and negative-EV verdicts, not to flatter the user into more bids

## Stack

- Skill format: Claude skills (Markdown with YAML frontmatter)
- Knowledge structure: Hierarchical reference files loaded on demand
- Integration target: Claude.ai web app, Claude Code, or any Claude deployment supporting skills
- Companion tooling (not included): Python opportunity-scoring pipeline with word-boundary regex matching, banned-keyword filtering, eligibility-code checking, and a manual blocklist layer

## License

MIT. See [LICENSE](./LICENSE). Fork it, adapt it, use it.

## Attributions

The federal RFP scaffolding section draws structural inspiration from CaseMark's open-source `rfp-response` skill (Apache 2.0). The Shipley-aligned win theme and discriminator construction follows publicly documented Shipley methodology. Everything else is original work.

---

*Built by someone who got tired of writing the same proposal section three times. If you fork it and it saves you a weekend, that's the whole point.*
