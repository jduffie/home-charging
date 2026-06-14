# Hand-off: reflect the home-charging lifecycle reframe in `STRUCTURE.md`

For the **garage-workspace** session. This repo (`home-charging`) was reframed
around the full home-charging lifecycle; the workspace standard should follow.
**Do not edit `repos/home-charging`** — its edits are done and committed.

## What happened (in `repos/home-charging`)

The owner decided `home-charging`'s purpose is the **full home-charging
lifecycle**, not just "buy a charger + hold the rate." The repo's README,
CLAUDE.md, prompts, rates pointer, and roadmap were updated to match:

- new prompt `prompts/when-to-charge.md` (stage 4/6 — operating side of TOU)
- new `docs/roadmap.md` item: *TOU / tiered rate model* (time-aware `$/kWh`)
- fixed the dangling TOU pointer in `rates/README.md`
- README reframed as a 6-stage lifecycle table; CLAUDE.md purpose rewritten

## The lifecycle (6 stages)

1. Plan & install · 2. Cost basis · 3. Configure hardware ·
4. Operate (*when* to charge) · 5. Monitor · 6. Optimize

## The sorting rule that's now load-bearing

Every stage lands in exactly one of three buckets:

- **situational** (depends on the owner's home) → a `prompts/` file, never prose
- **local/concrete** (this install's facts) → `rates/` · `charger/` · `electrical/`
- **not-yet-built** → an interest-gauged `docs/roadmap.md` item (vote-gated)

## Please update `STRUCTURE.md` to

1. In the **charger asset kind** description (the `home-charging` entry/row):
   change the framing from "holds the canonical rate + situational prompts" to
   "**owns the full home-charging lifecycle (plan → install → configure →
   operate → monitor → optimize); holds the canonical `$/kWh` rate**." Charger
   repos are lifecycle hubs, not just rate-holders.
2. If `STRUCTURE.md` documents the **prompt/local/roadmap bucketing** anywhere
   (the README-contract / prompts-format section), note that for charger repos
   the lifecycle **stage table** in the README is the organizing structure, and
   each stage maps to one bucket.
3. Leave the **single-canonical-rate rule** and **dependency direction**
   (vehicles → `home-charging`) unchanged — both held. TOU stayed a flat constant
   (operating lives in a prompt; TOU cost-math is a voted roadmap item, *not* a
   `rates/` change).

## Second update (added later) — prompts format changed to interview-style

The owner changed the prompt format: prompts no longer present `<bracketed>`
blanks for the user to pre-fill. Instead the prompt **instructs the assistant to
interview the user** — ask for the inputs a few at a time, wait for answers, then
recommend. The input list becomes the assistant's gather-checklist.

`STRUCTURE.md` line ~119 documents the old standard ("a fenced block containing
the prompt with `<bracketed>` variables the user fills in"). Please update it to
describe the interview-style format instead. The repo's own `CLAUDE.md` "Prompts
format" rule and all three prompt files have already been updated in
`repos/home-charging` (commit on `main`) — match `STRUCTURE.md` to them.

## Optional, your call

The workspace `CLAUDE.md` "Asset profiles" charger row currently reads
`functionality TBD; vehicle-agnostic` — you may want to swap "functionality TBD"
for "full-lifecycle hub (scaffold)" to match. Flagging, not prescribing.
