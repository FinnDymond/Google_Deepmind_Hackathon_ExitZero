# ExitZero demo guide

This guide is for somebody opening the project for the first time. It is a suggested route through the prototype, not a scripted performance claim.

## Setup

From the repository root:

```bash
npm install
cp .env.example .env.local
npm run dev
```

Then open `http://localhost:3000`. For Gemini features, add your own key to `.env.local` following `.env.example`. Do not commit that file or reveal the key in screenshots.

## A short walkthrough

1. Open `/lab?b=clinic`.
2. Look at the building model and identify possible routes to an exit.
3. Inspect one of the available disruption or blocked-route controls.
4. Compare the layout before and after the disruption. Which connections still lead to an exit?
5. Explore the attacker/defender workflow: the attacker searches for a difficult failure; the defender suggests a change; the simulation evaluates it.
6. Review the findings and any available report or export controls.

You can repeat the exercise with `/lab?b=industrial`.

## What to look for

- **Single points of failure:** Is there a doorway, stair or corridor that several routes rely on?
- **Multiple failures:** Does the outcome change if more than one connection is removed?
- **Proposed improvements:** Does a suggested change actually create a usable alternative route in the model?
- **Cost vs resilience:** How does an indicative intervention cost relate to the modelled improvement?

## Known limits

This is a simplified graph simulation, not a real-world evacuation certification. Treat recommendations and cost estimates as prototype outputs; actual building decisions require qualified professional review.
