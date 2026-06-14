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

## Third update (added later) — charger-sizing prompt: load-mgmt unlock + AHJ gate

**Informational — no `STRUCTURE.md` action required.** This is prompt *content*,
not a standard change; logged here so the workspace session has the full picture.

`prompts/charger-sizing.md` was strengthened so that when a main/sub-panel is the
binding constraint, the assistant surfaces an **EVEMS / load-management solution**
(circuit-sharing device, or a charger with built-in load management) as the path
to install *without* a feeder/panel upgrade — gated on whether the user's **AHJ /
adopted code edition** permits managed-load circuit sizing (else confirm with the
AHJ). Added an AHJ/code-edition item to the gather-checklist. Stayed vendor-neutral
(no "buy Emporia"). Commit on `main` in `repos/home-charging`.

If `STRUCTURE.md` ever grows prompt-authoring guidance/examples, this is a good
exemplar of a reusable convention — *surface the unlock and the regulatory gate,
vendor-neutrally* — but that's optional, not a required edit.

## Fourth update (added later) — `home-charging` fully de-personalized (no brand, no personal data)

**Requires a work-repo `CLAUDE.md` edit you must make — I can't from a
home-charging session.** The owner decided `home-charging` ships as a **neutral
fork-and-use skeleton**: `rates/`, `charger/`, `electrical/` are now neutral
templates a forker fills with *their own* facts — **no personal install data, and
no device brand, anywhere in the repo.** This **reverses** the earlier "total
Emporia de-brand *except* `charger/`" decision: `charger/` is now de-branded too
(the exception only made sense under the old "`charger/` = my real device" model,
which is gone).

What changed in `repos/home-charging` (committed on `main`):
- `charger/README.md` — dropped "Emporia Pro" from title + body; now a neutral
  "record your charger's specifics here" template.
- `rates/README.md` — `0.14` relabeled a **placeholder** (was "EDIT ME"); the
  "referenced by vehicles (`ford-lightning`, `vw-id4`)" bullet generalized to
  "referenced downstream / downstream cost dashboards" (consumer README names no
  specific vehicles).
- `electrical/README.md` — "this house / the install" → "your house / your install".
- `README.md` — stage-table `local →` cells → `yours →`; neutralized the
  "specific device for this install lives in `charger/`" line.
- `CLAUDE.md` (child) — bucket description now says the middle bucket is neutral
  templates with no personal data; kept the rate-dependency rule + vehicle names
  (maintainer/architecture doc, not consumer content).

**Please update the work-repo (`garage-workspace/CLAUDE.md`):** the "Asset
profiles" table row for `home-charging` lists hardware **"Emporia Pro w/ load
management"** — that device is no longer documented anywhere in the repo. Change
it to a neutral descriptor (e.g. "smart charger w/ load management; vendor-neutral
template — no device brand"). Also reconcile the earlier "Optional" note below if
you act on it.

## Optional, your call

The workspace `CLAUDE.md` "Asset profiles" charger row currently reads
`functionality TBD; vehicle-agnostic` — you may want to swap "functionality TBD"
for "full-lifecycle hub (scaffold)" to match. Flagging, not prescribing.
