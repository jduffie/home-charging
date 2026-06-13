# home-charging

Vehicle-agnostic shared context for home charging + energy. Holds the canonical
`$/kWh` rate that vehicle Expense dashboards reference.

Hardware: Emporia Pro w/ load management (functionality TBD).

Dependency direction: vehicles depend on this repo. Never the reverse.

**Status: scaffold.**

## I want to charge at home. How do I…?

- **size / install a charger?** → it's situational, depends on your home → PROMPT → [prompts/charger-sizing.md](prompts/charger-sizing.md)
- **what `$/kWh` rate should I use for cost math?** → local, the canonical editable constant → [rates/](rates/)
- **set up the Emporia Pro (integration, load management)?** → local, TBD → [charger/](charger/)
- **figure out circuit / wiring / panel + load?** → local, TBD → [electrical/](electrical/)
