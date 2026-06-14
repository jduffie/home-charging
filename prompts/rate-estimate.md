# Rate estimate — copy-paste prompt

Use to estimate your blended `$/kWh` for EV cost math when you don't have a clean
number. Paste the prompt below into Claude, ChatGPT, or any assistant and let it
interview you, then work out a single number you can drop into `rates/`.

```
You are helping me work out a single blended $/kWh for home EV charging cost math.
Don't make me fill in a form — interview me. Ask for the details below a few at a
time, wait for my answers, and ask follow-ups before giving a number.

Gather:
- my utility and rate plan name, if I know them
- a recent bill: total $ amount for total kWh used over the billing period
- my rate structure (flat, time-of-use, tiered, demand charges) and the per-kWh
  prices + any thresholds/hours that apply
- whether I have solar or a home battery, and rough offset
- whether my utility offers a separate EV / off-peak charging plan, and if I'm on it

Once you have what you need, tell me:
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
