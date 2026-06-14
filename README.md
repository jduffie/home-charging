# home-charging

Vehicle-agnostic shared context for the **whole home-charging lifecycle** — plan,
install, configure, operate, monitor, optimize — not just buying a charger. Also
holds the canonical `$/kWh` rate that vehicle Expense dashboards reference.

Hardware: Emporia Pro w/ load management (functionality TBD).

Dependency direction: vehicles depend on this repo. Never the reverse.

**Status: scaffold.**

New here / just want to charge at home? → **[docs/start-here.md](docs/start-here.md)**

## I want to charge at home. The lifecycle:

| Stage | The question | Where it's answered |
|-------|--------------|---------------------|
| 1. Plan & install | Can I? what charger? how is it wired? | PROMPT → [prompts/charger-sizing.md](prompts/charger-sizing.md) |
| 2. Cost basis | what `$/kWh` for cost math? | local → [rates/](rates/) · unsure? → [prompts/rate-estimate.md](prompts/rate-estimate.md) |
| 3. Configure hardware | Emporia Pro setup, load management | local, TBD → [charger/](charger/) · also [electrical/](electrical/) for circuit/wiring/panel |
| 4. Operate | *when* do I charge? schedule to off-peak? | PROMPT → [prompts/when-to-charge.md](prompts/when-to-charge.md) |
| 5. Monitor | usage, cost, what load-mgmt did, history | roadmap → [docs/roadmap.md](docs/roadmap.md) |
| 6. Optimize | right TOU plan? shift load? | PROMPT → [prompts/when-to-charge.md](prompts/when-to-charge.md) · TOU cost math: roadmap |

Situational stages ship a copy-paste **prompt** (depends on *your* home); local
stages hold the concrete facts for this install; the rest is **interest-gauged**
on the [roadmap](docs/roadmap.md) — nothing there gets built until it's voted.
