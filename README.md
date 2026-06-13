# Slate Auto: Reservation-to-Revenue POV

## Live Demo : https://claude.ai/public/artifacts/553d7c5a-91bc-49e0-ad0f-6811e408cf7d

An interactive, single-file point of view on the question a commercial strategy role at Slate Auto actually exists to answer: **not how many reservations exist, but how many of them convert to paid.**

> Built as first-round prep for a Strategy Analyst conversation. Public inputs only, with conversion and revenue-per-unit treated as assumptions used to size the question.

## The thesis

Slate has 160,000+ reservations, but those were $50 fully refundable deposits placed before anyone saw a price. On June 24, reservations switch to $300 non-refundable preorders against real pricing in the mid-$20Ks. That is the first honest test of demand, and it lands without the $7,500 federal credit the affordability story was originally built on.

So the headline number (reservations) and the number that drives revenue (paid conversion) are not the same thing. This page makes that gap tangible and lets you stress-test it.

## What it does

The page is a working model, not a static slide:

- **Conversion bench.** Drag reservation-to-paid conversion (5 to 35 percent) and revenue per unit ($27K base to $35K loaded) and watch launch-window revenue recalculate live.
- **Fleet anchor toggle.** Layer in 8,000 commercial units to see how block buyers smooth lumpy consumer demand.
- **Three strategic levers.** Reframe value over price, grow revenue per unit through attach, and anchor with fleet. Each expands to a short "how I'd test it" note so the recommendation comes with a measurement plan, not just an opinion.

## Why it is built this way

A strategy hire should be able to separate a vanity metric from the operating metric and then show what they would do about the gap. The interactivity is the point: it invites the interviewer to push the assumptions themselves and see that the conclusion (conversion is the lever worth managing) holds across the range.

## Run it

No build step, no dependencies. Clone and open the file:

```bash
git clone https://github.com/PaarthShah-2001/slate-reservation-pov.git
cd slate-reservation-pov
open index.html
```

Or just open `index.html` in any modern browser. Fonts load from Google Fonts, so an internet connection gives you the intended typography (Space Grotesk, Inter, IBM Plex Mono).

## Data and assumptions

| Input | Source |
| --- | --- |
| 160K+ reservations, preorder mechanics, mid-$20Ks pricing | Public reporting, June 2026 |
| Competitor MSRPs (Maverick $28.8K, Santa Cruz $31.1K) | Public listings, June 2026 |
| Conversion rate, revenue per unit, fleet volume | Illustrative assumptions, not Slate figures |

The model is meant to size a question, not to forecast Slate's actual results. Every assumption is exposed as a control so you can substitute your own.

## Tech

Plain HTML, CSS, and vanilla JavaScript in a single file. No framework, no localStorage, no external scripts beyond web fonts. Responsive down to a single column on narrow screens, with reduced-motion support.

## A note on the model

The swing figure ("a 15 point conversion swing is worth roughly $X") is anchored to a fixed 10-to-25 percent reference band and scales with revenue per unit, so it stays comparable as you move the revenue slider. It does not track the live conversion slider position by design, to keep the reference point stable.

---

Built by Paarth Shah. Part of an ongoing portfolio of product and strategy artifacts.
