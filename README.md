# home-charging

Vehicle-agnostic shared context for the **whole home-charging lifecycle** — plan,
install, configure, operate, monitor, optimize — not just buying a charger. Also
holds the canonical `$/kWh` rate that vehicle Expense dashboards reference.

Hardware: Emporia Pro w/ load management (functionality TBD).

Dependency direction: vehicles depend on this repo. Never the reverse.

**Status: scaffold.**

## I want to charge at home. The lifecycle:

| Stage | The question you have | Where it's answered |
|-------|-----------------------|---------------------|
| 1. Plan & install | Getting a charger in — which one, and wired safely | PROMPT → [prompts/charger-sizing.md](prompts/charger-sizing.md) |
| 2. Cost basis | What charging actually costs you | local → [rates/](rates/) · unsure? → [prompts/rate-estimate.md](prompts/rate-estimate.md) |
| 3. Configure hardware | Setting up the charger once it's in | local, TBD → [charger/](charger/) · also [electrical/](electrical/) for circuit/wiring/panel |
| 4. Operate | Charging at the cheapest time of day | PROMPT → [prompts/when-to-charge.md](prompts/when-to-charge.md) |
| 5. Monitor | Keeping an eye on usage and cost | roadmap → [docs/roadmap.md](docs/roadmap.md) |
| 6. Optimize | Being on the right rate plan | PROMPT → [prompts/when-to-charge.md](prompts/when-to-charge.md) · TOU cost math: roadmap |

Situational stages ship a copy-paste **prompt** (depends on *your* home); local
stages hold the concrete facts for this install; the rest is **interest-gauged**
on the [roadmap](docs/roadmap.md) — nothing there gets built until it's voted.

## How to use a prompt

1. Open the prompt file linked above and copy the fenced block.
2. Paste it into any assistant (Claude, ChatGPT, …).
3. It interviews you a few questions at a time — answer what you know, and it asks
   for the rest before giving you an answer.

On mobile and just want the raw text? Swap `github.com/.../blob/` for
`raw.githubusercontent.com/...` in the link.

> ⚠️ Informational only — **not** professional advice. Electrical work is
> hazardous; verify everything with a licensed electrician and your local AHJ.
> See **[DISCLAIMER.md](DISCLAIMER.md)**.
