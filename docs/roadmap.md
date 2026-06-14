# Roadmap

Interest-gauged. Each item below is now an **open GitHub issue** — click through and
**react 👍 to vote.** Nothing here gets built until it's voted.

---

## TOU / tiered rate model

Make the canonical `$/kWh` time-aware instead of one flat blended constant:
represent peak / off-peak / shoulder prices and their hours, so cost math can
reflect *when* energy was used. Affects the `rates/` contract and the downstream
vehicle Expense dashboards that depend on a single number — so it's a deliberate,
voted change, not a snap edit. Until then: flat rate in `rates/`, and the
[when-to-charge](../prompts/when-to-charge.md) prompt covers the operating side.

[👍 Vote — issue #5](https://github.com/jduffie/home-charging/issues/5)

---

## Charging-session logging

Capture per-session data (date, kWh delivered, duration, cost at the canonical
`rates/` value) so charging history is queryable over time.

[👍 Vote — issue #1](https://github.com/jduffie/home-charging/issues/1)

---

## Load-management visibility

Surface what the Emporia Pro's load management is actually doing — when it
throttles, by how much, and why — instead of it being an invisible black box.

[👍 Vote — issue #2](https://github.com/jduffie/home-charging/issues/2)

---

## Energy / cost export

Export charging + energy data (CSV/JSON) for use in vehicle Expense dashboards
and external spreadsheets, using the canonical `$/kWh` rate.

[👍 Vote — issue #3](https://github.com/jduffie/home-charging/issues/3)

---

## Home Assistant integration

Pull the Emporia Pro / energy data into Home Assistant for automation,
dashboards, and alerts.

[👍 Vote — issue #4](https://github.com/jduffie/home-charging/issues/4)
