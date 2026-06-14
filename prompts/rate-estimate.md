# Rate estimate — copy-paste prompt

Use to estimate your blended `$/kWh` for EV cost math when you don't have a clean
number. Paste the prompt below into Claude, ChatGPT, or any assistant. It offers
three input paths — upload a bill, a utility-database lookup, or an interview — and
works out a single number you can drop into `rates/`.

```
You are helping me work out a single blended $/kWh for home EV charging cost math.
Don't make me fill in a form. First ask which of these inputs I can give you, then
use the best one available:

A. A recent utility bill — I upload it (PDF/photo). Read the total $ billed and the
   total kWh used over the period, plus the rate plan name and any TOU/tier
   structure printed on it. Most accurate — prefer it if I have one.
B. My utility + location — look the tariff up in a rate database (only if you can
   browse/call APIs). The free canonical source is the NREL/OpenEI Utility Rate
   Database (URDB): ~3,700 US utilities, full flat/tiered/TOU structures. Get a free
   key and verify the current endpoint at openei.org/services (the developer.nrel.gov
   domain is migrating in 2026). NREL "Utility Rates v3" is simpler but ~2012 data —
   ballpark only. Paid providers (e.g. Arcadia, RateAcuity, WattBuy, UtilityAPI)
   exist for guaranteed-current tariffs.
C. Interview me — if I have neither, ask the details below a few at a time and wait
   for my answers.

Whichever path, gather or confirm:
- my utility and rate plan name
- total $ for total kWh over a recent billing period (the core ratio)
- rate structure (flat, TOU, tiered, demand charges) + per-kWh prices, thresholds, hours
- whether I have solar or a home battery, and rough offset
- whether a separate EV / off-peak plan exists and whether I'm on it

Once you have what you need, tell me:
1. A single blended $/kWh to use as my home rate constant, and how you got it.
2. Whether a TOU/EV plan would meaningfully change it if I charge mostly overnight,
   and roughly by how much.
3. Caveats — what makes one flat number rough (TOU spread, tier crossing, demand
   charges, seasonal swings, solar).
4. What else you'd need to tighten the estimate.

Give a specific number. Flag where a flat blended rate hides real variation.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- Three input paths, best-first: **upload a bill** (most accurate) → **database
  lookup** (NREL/OpenEI URDB is the free, TOU-capable source; needs an assistant
  that can call APIs) → **interview**. The assistant picks based on what you have.
- The output goes into [../rates/README.md](../rates/README.md) as
  `RATE_USD_PER_KWH`.
