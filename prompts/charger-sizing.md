# Charger sizing & install — copy-paste prompt

Use when deciding what home EV charger to buy and how to wire it. The answer
depends on your home, car, and habits, so this isn't something a repo can answer
directly — paste the prompt below into Claude, ChatGPT, or any assistant, fill in
the `<brackets>`, and let it reason about your specific situation.

These are starting points. Confirm anything load- or code-related with a licensed
electrician before you buy or wire.

```
You are helping me size and plan a home Level 2 EV charger install. Ask me for
anything missing, then give a concrete recommendation with reasoning.

My situation:
- Location: <city, state/country>  (note climate + likely utility/permit rules)
- Electrical service: <main panel amperage, e.g. 200A> with roughly
  <spare capacity / known large loads like HVAC, range, dryer, hot tub>
- Panel-to-charger distance: <approx feet, and indoor garage vs outdoor/driveway>
- Vehicle(s): <make/model/year>, onboard AC charger max <kW if known>,
  battery <kWh if known>
- Driving: ~<daily miles>, typically parked at home <hours/night> to charge,
  worst-case day <miles>
- Goals: <future-proofing? second EV later? solar? lowest cost? fastest charge?>
- Constraints: <renting? HOA? budget? DIY vs electrician?>

Please tell me:
1. Recommended charger amperage and circuit size (and why this, not more/less).
2. Whether my daily/worst-case driving is comfortably covered by overnight charging
   at that rate.
3. Whether I need active load management (and roughly when it pays off vs a
   dedicated circuit), given my panel capacity.
4. Hardwired vs plug-in (NEMA receptacle) trade-offs for my case.
5. Wire gauge / breaker implications at my distance, and any derating to flag.
6. Permitting / inspection / utility-program items I should check locally.
7. A short shopping checklist and the open questions you still need answered.

Be specific with numbers. Flag anything that requires a licensed electrician or a
local code check rather than guessing.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- If you already own a specific charger (e.g. Emporia Pro), add that as a
  constraint so the assistant plans around its capabilities instead of recommending
  hardware.
