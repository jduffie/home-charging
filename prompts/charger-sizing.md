# Charger sizing & install — copy-paste prompt

Use when deciding what home EV charger to buy and how to wire it. The answer
depends on your home, car, and habits, so this isn't something a repo can answer
directly — paste the prompt below into Claude, ChatGPT, or any assistant and let
it interview you about your situation, then reason from your answers.

These are starting points. Confirm anything load- or code-related with a licensed
electrician before you buy or wire.

```
You are helping me size and plan a home Level 2 EV charger install. Don't make me
fill in a form — interview me. Ask for the details below a few at a time, wait for
my answers, and ask follow-ups on anything unclear before you recommend anything.

Gather:
- where I live (climate + likely utility/permit rules)
- my main electrical service size, and roughly how much spare capacity it has /
  what big loads it already runs (HVAC, range, dryer, hot tub)
- whether a sub-panel is involved (e.g. a garage sub-panel): its feeder amperage,
  bus rating, and roughly how many spare breaker spaces
- which panel is closer to the install spot, and which I intend to feed from
- where the charger will mount, where the car parks relative to it, and the
  charge-port location on the vehicle (front/rear, driver/passenger side)
- the cord length needed to reach the port, and the wire run from the panel I'd
  feed from to the charger
- my vehicle(s), onboard AC charge rate, and battery size
- my driving: daily miles, hours parked at home to charge, worst-case day
- my goals (future-proofing, second EV later, solar, lowest cost, fastest charge)
- my constraints (renting, HOA, budget, DIY vs electrician)

Once you have what you need, tell me:
1. Recommended charger amperage and circuit size (and why this, not more/less).
2. Which panel to tap (main vs sub-panel) and why.
3. Whether the sub-panel feeder + bus can carry the new load, or needs upgrading
   first — run the load calc at the sub-panel level, not just the main service.
4. Whether my daily/worst-case driving is comfortably covered by overnight charging
   at that rate.
5. Whether I need active load management (and roughly when it pays off vs a
   dedicated circuit), given my panel capacity.
6. Hardwired vs plug-in (NEMA receptacle) trade-offs for my case.
7. Wire gauge / breaker implications at my distance, and any derating to flag.
8. Confirm the cord physically reaches the charge port given where the car parks.
9. Permitting / inspection / utility-program items I should check locally.
10. A short shopping checklist and the open questions you still need answered.

Be specific with numbers. Flag anything that requires a licensed electrician or a
local code check rather than guessing. If I already own a charger (e.g. Emporia
Pro), plan around its capabilities instead of recommending new hardware.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- It interviews you rather than asking you to pre-fill a form — so you don't need
  every number handy up front; answer what you know and it'll ask for the rest.
