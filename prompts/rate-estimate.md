# Rate estimate — copy-paste prompt

Use to estimate your blended `$/kWh` for EV cost math when you don't have a clean
number. Paste the prompt below into Claude, ChatGPT, or any assistant, fill in the
`<brackets>`, and let it work out a single number you can drop into `rates/`.

```
You are helping me work out a single blended $/kWh for home EV charging cost math.
Ask me for anything missing, then give one number plus caveats.

My situation:
- Utility / plan: <utility name and rate plan name, if known>
- Recent bill: total <$ amount> for <total kWh used> over the billing period
- Rate structure: <flat? time-of-use (TOU)? tiered? demand charges?> — list the
  per-kWh prices and any thresholds/hours if you have them
- Solar: <none / net-metered solar / battery> (and rough offset if known)
- EV-specific rate: <is there a separate EV / off-peak charging plan available, and
  am I on it?>

Please tell me:
1. A single blended $/kWh I should use as my home rate constant, and how you got it.
2. Whether a TOU/EV plan would meaningfully change that number if I charge mostly
   overnight, and roughly by how much.
3. Caveats — anything that makes one flat number a rough approximation for me
   (TOU spread, tier crossing, demand charges, seasonal swings, solar).
4. What else you'd need from me to tighten the estimate.

Give a specific number. Flag where a flat blended rate hides real variation.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- The output goes into [../rates/README.md](../rates/README.md) as
  `RATE_USD_PER_KWH`.
