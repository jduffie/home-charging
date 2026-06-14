# CLAUDE.md — home-charging

## Rules (every session)
- **Dependency direction:** vehicles depend on THIS repo for the `$/kWh` rate.
  NEVER the reverse. Do not add vehicle-specific content here — no per-vehicle
  PIDs, dashboards, or model quirks. Those live in the vehicle hub repos.
- **Canonical rate:** the `$/kWh` cost basis lives in `rates/` as one editable
  constant. Edit it there, once. Vehicle Expense pages (`ford-lightning`,
  `vw-id4`) reference that value; they do not define their own.
- **Scope:** situational / advice questions (panel capacity, local code, budget,
  charger sizing) ship a copy-paste prompt under `prompts/`, NEVER prose. We do
  not write advice essays.
- **Prompts format:** one file per prompt. A one-line purpose, then a single
  fenced block with `<bracketed>` vars the user fills in, vendor-neutral. End the
  prompt by asking the assistant for open questions / what else it needs — these
  are starting points, not authoritative answers.
- **Roadmap is interest-gauged:** `docs/roadmap.md` drafts an issue with "👍 to
  vote." Don't build a roadmap item until it's voted.

## What this repo is
Vehicle-agnostic shared context for the **whole home-charging lifecycle**, not
just buying a charger. Six stages: (1) plan & install, (2) cost basis,
(3) configure hardware, (4) operate — *when* to charge, (5) monitor, (6) optimize.
Owns the canonical `$/kWh` rate and the situational-question prompts; owns nothing
tied to a specific vehicle.

Each stage lands in one of three buckets, per the rules above: **situational** →
a `prompts/` file; **local/concrete** → `rates/`, `charger/`, `electrical/`;
**not-yet-built** → an interest-gauged `docs/roadmap.md` item. Keep the README
stage table and this list in sync when stages move between buckets.

Hardware: Emporia Pro w/ load management (functionality TBD).

**Status: scaffold.**

## Full standard
Lives in the garage-workspace work repo (STRUCTURE.md).
