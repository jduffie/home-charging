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
- Main service: <amps, e.g. 200A> with roughly
  <spare capacity / known large loads like HVAC, range, dryer, hot tub>
- Sub-panel involved? <none | garage sub-panel fed by ___A feeder,
  ___-space bus, ~___ spare breaker spaces>
- Which panel is closer to the install spot, and which do you intend to feed from?
- Charger mount location: <wall in garage / outside wall / driveway pedestal / etc.>
- Where the car parks relative to that, and the charge-port location on the
  vehicle <front/rear, driver/passenger side>
- Cord length needed to reach the port from the mount: <approx feet>
- Wire run from the panel you'd feed from to the charger: <approx feet>
- Vehicle(s): <make/model/year>, onboard AC charger max <kW if known>,
  battery <kWh if known>
- Driving: ~<daily miles>, typically parked at home <hours/night> to charge,
  worst-case day <miles>
- Goals: <future-proofing? second EV later? solar? lowest cost? fastest charge?>
- Constraints: <renting? HOA? budget? DIY vs electrician?>

Please tell me:
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
local code check rather than guessing.
```

## Notes
- Vendor-neutral on purpose — works in any assistant.
- If you already own a specific charger (e.g. Emporia Pro), add that as a
  constraint so the assistant plans around its capabilities instead of recommending
  hardware.
