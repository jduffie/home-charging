# rates — $/kWh cost basis (source of truth)

This is the **single source of truth** for the home electricity rate used in cost
math. Edit it here, once.

```
RATE_USD_PER_KWH = 0.14   # EDIT ME — your blended home rate
```

- **How to find your number:** read it off a recent utility bill — total `$` ÷
  total `kWh`.
- **Referenced by vehicles:** vehicle Expense dashboards (`ford-lightning`,
  `vw-id4`) reference THIS value; they do not define their own. Change the
  constant above and downstream cost math follows.
- **Flat blended rate:** a single number — no time-of-use (TOU) or tiered split
  yet. That's a roadmap item — see [../docs/roadmap.md](../docs/roadmap.md).

Not sure of your rate? → [prompts/rate-estimate.md](../prompts/rate-estimate.md)
