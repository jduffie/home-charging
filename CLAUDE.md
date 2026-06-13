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
Vehicle-agnostic shared context for home charging + energy. Holds the canonical
`$/kWh` rate and the situational-question prompts; owns nothing tied to a
specific vehicle.

Hardware: Emporia Pro w/ load management (functionality TBD).

**Status: scaffold.**

## Full standard
Lives in the garage-workspace work repo (STRUCTURE.md).
