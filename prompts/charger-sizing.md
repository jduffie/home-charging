# Charger sizing & install — copy-paste prompt

Use when deciding what home EV charger to buy and how to wire it. The answer
depends on your home, car, and habits, so this isn't something a repo can answer
directly — paste the prompt below into Claude, ChatGPT, or any assistant. It uses
whatever you can give it — photos of your panel, a vehicle spec sheet, location
lookups — and interviews you for the rest, then reasons from your answers.

These are starting points. Confirm anything load- or code-related with a licensed
electrician before you buy or wire.

```
You are helping me size and plan a home Level 2 EV charger install. Don't make me
fill in a form. First ask which inputs I can give you, use whatever reduces the
questions, then interview me for the rest — a few at a time, waiting for my answers
and asking follow-ups before you recommend anything.

A. Photos / documents — read what you can from these before asking:
- a photo of my main electrical panel, door open (main breaker amperage, spare
  breaker spaces, and existing big loads inferred from the breaker labels)
- a photo of any sub-panel I'd feed from (feeder breaker, bus rating, spare spaces)
- a photo of where the charger will mount and where the car parks (reach + which
  side the charge port is on)
- my vehicle's window sticker / spec page (onboard AC charge rate, battery size)
- a recent utility bill (identifies my utility for permit/program rules)

B. Lookups — only if you can browse or call APIs:
- which utility serves my address, and any EV charging rebates / programs (e.g. the
  DSIRE incentive database; NREL/OpenEI for the serving utility)
- the electrical code edition (NEC) my state / AHJ has adopted — it affects whether
  managed-load (EVEMS) circuit sizing is allowed; if you can't confirm my local
  adoption, tell me to check with my AHJ rather than assuming
- my vehicle's onboard AC charge rate + battery size by make / model / year / trim

C. Interview me for anything the above didn't cover:
- where I live (climate + likely utility/permit rules)
- which electrical code edition / authority having jurisdiction (AHJ) governs
  where I live — it affects whether managed-load (EVEMS) circuit sizing is allowed
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
4. If my main or sub-panel is the binding constraint, whether an EV
   energy-management / load-management solution (a circuit-sharing device, or a
   charger with built-in load management) would let me install at a useful
   amperage **without** a feeder/panel upgrade — and whether that managed-load
   sizing is permitted under the code edition my AHJ has adopted. If you're unsure
   of my local adoption, tell me to confirm with my AHJ rather than assuming.
5. Whether my daily/worst-case driving is comfortably covered by overnight charging
   at that rate.
6. Whether I need active load management (and roughly when it pays off vs a
   dedicated circuit), given my panel capacity.
7. Hardwired vs plug-in (NEMA receptacle) trade-offs for my case.
8. Wire gauge / breaker implications at my distance, and any derating to flag.
9. Confirm the cord physically reaches the charge port given where the car parks.
10. Permitting / inspection / utility-program items I should check locally.
11. A short shopping checklist and the open questions you still need answered.

Be specific with numbers. Flag anything that requires a licensed electrician or a
local code check rather than guessing. If I already own a charger, plan around its
capabilities instead of recommending new hardware.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- Three input paths, best-first: **photos/docs** (a panel photo is the big one —
  amperage, spare spaces, existing loads at a glance) → **location lookups** (serving
  utility, EV rebates, your AHJ's adopted code edition; needs an assistant that can
  browse) → **interview** for the rest. You don't need every number handy up front.
