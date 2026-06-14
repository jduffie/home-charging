# When to charge — copy-paste prompt

Use to work out *when* to charge to minimize cost under a time-of-use (TOU) or
tiered rate — and whether a different utility plan would save you money. This is
the operating side of home charging, separate from sizing the charger
([charger-sizing.md](charger-sizing.md)) and from picking the single blended
number for cost math ([rate-estimate.md](rate-estimate.md)). Paste the prompt
below into Claude, ChatGPT, or any assistant and let it interview you.

These are starting points. Confirm current rate plans and enrollment rules with
your utility before switching.

```
You are helping me decide when to charge my EV at home to minimize cost, and
whether I'm on the right utility rate plan. Don't make me fill in a form —
interview me. Ask for the details below a few at a time, wait for my answers, and
ask follow-ups before recommending a schedule.

Gather:
- my utility and current plan name
- my rate structure (flat, TOU, tiered); if TOU/tiered, the per-kWh prices and the
  hours/thresholds for each window (off-peak, peak, shoulder)
- other EV-specific or whole-home plans my utility offers that I could switch to
- my charging need (kWh per day, or daily miles + car efficiency)
- the window the car is plugged in on a typical night
- any hard deadline (target % or miles ready by a departure time)
- whether the charger or the car supports scheduled / delayed-start charging
- the charge rate the charger actually delivers (amps / kW)
- whether I have solar or a home battery, and rough offset
- my goal priority (lowest cost, fastest done, least grid use, battery longevity)

Once you have what you need, tell me:
1. The cheapest charging schedule that still meets my deadline, given my windows
   and charge rate (be specific about start/stop times).
2. Whether my available window is long enough to deliver my daily kWh at my charge
   rate entirely within the cheapest hours — and what to do if it isn't.
3. Whether switching to a different rate plan (EV/off-peak/TOU vs my current one)
   would meaningfully lower my cost given how I actually charge, and rough $/month.
4. Where to set scheduled/delayed-start charging (charger vs car) and any gotcha
   (e.g. preconditioning, both scheduling at once, losing a session).
5. How this changes the single blended $/kWh I should put in my cost math.
6. A short checklist and the open questions you still need answered.

Be specific with numbers and times. Flag anything I should confirm with my utility
(plan availability, enrollment rules, true-up) rather than guessing.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- Feeds back into [../rates/README.md](../rates/README.md): a TOU schedule can move
  your blended `$/kWh`, which is the number cost math uses. The rate stays a single
  flat constant for now — see the TOU item in [../docs/roadmap.md](../docs/roadmap.md).
