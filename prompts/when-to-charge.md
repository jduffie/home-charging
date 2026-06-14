# When to charge — copy-paste prompt

Use to work out *when* to charge to minimize cost under a time-of-use (TOU) or
tiered rate — and whether a different utility plan would save you money. This is
the operating side of home charging, separate from sizing the charger
([charger-sizing.md](charger-sizing.md)) and from picking the single blended
number for cost math ([rate-estimate.md](rate-estimate.md)). Paste the prompt
below into Claude, ChatGPT, or any assistant. It uses whatever you can give it —
bills, your utility's rate sheets, an interval-usage export — and interviews you
for the rest.

These are starting points. Confirm current rate plans and enrollment rules with
your utility before switching.

```
You are helping me decide when to charge my EV at home to minimize cost, and
whether I'm on the right utility rate plan. Don't make me fill in a form. First ask
which inputs I can give you, use whatever reduces the questions, then interview me
for the rest — a few at a time, waiting for my answers before recommending anything.

A. Photos / documents — read what you can from these before asking:
- recent bill(s) — ideally ~12 months to capture seasonal usage; at minimum one
  (total $, total kWh, and any TOU/tier breakdown printed on it)
- my utility's rate / tariff sheets for my current plan and any plans I'd compare
- my interval-usage export if my utility offers one (e.g. a Green Button "Download
  My Data" CSV) — hourly whole-home usage is the best input for comparing plans

B. Lookups — only if you can browse or call APIs:
- my utility's residential tariffs, including EV / off-peak and whole-home TOU
  options, from the NREL/OpenEI URDB (verify the current endpoint at
  openei.org/services; the developer.nrel.gov domain is migrating in 2026)
- confirm my current plan's windows and prices if I'm unsure of them

C. Interview me for anything the above didn't cover:
- my utility and current plan name
- my rate structure (flat, TOU, tiered); if TOU/tiered, the per-kWh prices and the
  hours/thresholds for each window (off-peak, peak, shoulder)
- other EV-specific or whole-home plans my utility offers that I could switch to
- my charging need (kWh per day, or daily miles + car efficiency)
- the window the car is plugged in on a typical night
- any hard deadline (target % or miles ready by a departure time)
- whether the charger or the car supports scheduled / delayed-start charging
- the charge rate the charger actually delivers (amps / kW)
- my whole-home usage shape beyond the EV — when I use the most power and which big
  loads run in peak hours (A/C, electric heat, pool/spa) — since switching plans
  reprices every kWh, not just charging
- whether I have solar or a home battery, and rough offset
- my goal priority (lowest cost, fastest done, least grid use, battery longevity)

Once you have what you need, tell me:
1. The cheapest charging schedule that still meets my deadline, given my windows
   and charge rate (be specific about start/stop times).
2. Whether my available window is long enough to deliver my daily kWh at my charge
   rate entirely within the cheapest hours — and what to do if it isn't.
3. A plan-by-plan comparison: my estimated total bill (monthly and annual) under my
   current plan vs each candidate, modeling my WHOLE-HOME usage — not just the EV,
   since a plan change reprices every kWh. Call out: the net $ difference and which
   plan wins; whether EV/off-peak savings are cancelled by higher peak rates on the
   rest of my usage; enrollment friction (lock-in or minimum stay, ability to switch
   back, true-up, demand charges, minimum bills, separate-meter requirement); and how
   much the answer depends on me actually moving charging into off-peak hours.
4. Where to set scheduled/delayed-start charging (charger vs car) and any gotcha
   (e.g. preconditioning, both scheduling at once, losing a session).
5. How this changes the single blended $/kWh I should put in my cost math.
6. A short checklist and the open questions you still need answered.

Be specific with numbers and times. Flag anything I should confirm with my utility
(plan availability, enrollment rules, true-up) rather than guessing.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- Three input paths, best-first: **bills / tariff sheets / an interval-usage export**
  (a Green Button CSV is the gold standard for plan comparison) → **URDB tariff
  lookup** (needs an assistant that can browse) → **interview**.
- Plan-switch comparisons price your **whole-home** usage, not just charging — an
  EV/off-peak plan can cut charging cost but raise the cost of everything else.
- Feeds back into [../rates/README.md](../rates/README.md): a TOU schedule can move
  your blended `$/kWh`, which is the number cost math uses. The rate stays a single
  flat constant for now — see the TOU item in [../docs/roadmap.md](../docs/roadmap.md).
