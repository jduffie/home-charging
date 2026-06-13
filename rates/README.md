# rates — $/kWh cost basis (source of truth)

This is the **single source of truth** for the home electricity rate used in cost
math. Vehicle Expense pages (`ford-lightning`, `vw-id4`) reference this value;
they do not define their own. Edit it here, once.

```
RATE_USD_PER_KWH = 0.14   # EDIT ME — your blended home electricity rate
```

- **Edit in one place:** change the constant above; downstream Expense dashboards
  pull from this value.
- **Flat blended rate:** a single number, no time-of-use (TOU) or tiered split
  yet. That's a roadmap item — see [../docs/roadmap.md](../docs/roadmap.md).
