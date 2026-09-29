# 13 · Vampire Haze

Dark, gothic and drenched: an empty cathedral at 3 AM, with the top rolled soft and long, heavy tails.

**Status:** blueprint (Step 2). Settings get dialed in during Step 3.
**Placement:** leans into the beat (D6) · **Tune:** Fast · **Builds on:** [foundation](00-foundation.md)

## Sound targets

| Target | Value |
|---|---|
| Tone | Dark and warm (Q24). Low cut at 80 Hz, low-mid warmth +2–3 dB near 220 Hz, top rolled off above about 8 kHz by 4–6 dB. 2–4 kHz stays put so rapped words still read: dark, not buried |
| Density | 9–11 dB total, with warm tape saturation |
| Grit | Warm tape on the lead, plus a tape-saturated hall return: the "dirty fog" |
| Space | The wettest of the five. A dark 2–3 s hall (Vintage style) with ~50 ms of pre-delay, ducked by the voice. Near-frozen throws on the last word of key lines (Q23). Wet 5/5 |
| Width | Lead mono. Doubles at L/R 70. Hall and throws fully wide |
| Placement | Leans into the beat: the least presence and the most wet of the five |
| Tune | Fast: retune 10–20, humanize and Flex-Tune around 20 |

## Upgrades (Q27)

- **Throws on their own return.** A separate near-frozen return lets the main hall stay a tidy 2–3 s. (Phase 1 put freeze and long throws on the hall itself.)
- **Grainier hall.** Pro-R 2's Vintage style gives the space an older, grainier character before the tape even touches it.
- **Low-mid bloom control.** A multiband stage keeps the added warmth from turning into boom when room box and long tails stack up.
- **Band-limited throws.** The frozen tails are filtered to about 300 Hz–5 kHz, so they never cloud the low end or hiss.

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R.
3. **Key moves:** place the throws and the hall eases.

## Track map

| Track | Gets audio from | Routes to | Sends |
|---|---|---|---|
| VOX IN | Lead clips | LEAD | — |
| LEAD | VOX IN | VOX BUS | FX · HALL (steady), FX · THROW (automated only) |
| DBL IN L / R | Left / right double clips | DBL, panned L70 / R70 | — |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · HALL, 6 dB below LEAD's send |
| FX · HALL | Sends | VOX GROUP | — |
| FX · THROW | Sends | VOX GROUP | — |
| VOX BUS | LEAD, DBL | VOX GROUP | — |
| VOX GROUP | VOX BUS, FX tracks | Master | — |

## VOX IN

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Rumble cut | Foundation standard |
| 2 | Pro-G | Gentle expander | In a sound this wet, breaths turn into long, ghostly tails. Taking them down here keeps them out of the hall |
| 3 | Auto-Tune Artist | Fast tune in the song's key | Quick correction that still lets the melancholy slides through |

## LEAD

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Corrective: low cut, box, resonances | Box control matters more here, because a long reverb exaggerates boxiness |
| 2 | Pro-C | Compressor 1: peak catcher | Peaks would splash the hall and the throws |
| 3 | Pro-Q | Tone: low-mid warmth | Warm body for the gothic weight |
| 4 | Saturn 2 | Warm Tape | Thickens the darkness (Phase 1) |
| 5 | Pro-C | Compressor 2: opto leveler | A steady level into the hall means steady tails |
| 6 | Pro-Q | Darkening: top rolled off | The dark half of the tone curve (Q24) |
| 7 | Pro-DS | De-esser | S's in a long hall and in the throws turn into splashes, so they're caught before the sends |
| 8 | Pro-MB | Low-mid bloom and upper-mid spike control | Warmth, room box and long tails can add up to boom. It clamps only when that builds |
| 9 | Pro-Q | Polish: placement | Leans the lead into the beat without losing words |
| 10 | Pro-L 2 | Peak control | Keeps what goes into the hall and throws consistent |

**Order notes:** the darkening EQ (6) comes before the de-esser (7), so it de-esses the final tone. Everything that feeds the hall and the throws is under control before the sends.

## Parallel tracks

None. This preset's character lives in the space, so it doesn't need a parallel layer.

## FX returns

**The throw and dark-return engine.**

### FX · HALL

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Vintage style, 2–3 s, ~50 ms pre-delay, low Brightness, Thickness up, Ducking on | The long dark hall (Q23), ducked so the words stay clear (D15) |
| 2 | Saturn 2 | Warm Tape, HQ on | Turns the tail into Phase 1's dirty fog |
| 3 | Pro-Q | Low cut ~200 Hz, high cut ~6 kHz, lows kept mono | Dark, and out of the low end |

### FX · THROW

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Largest Space, Decay Rate 200%, low Brightness, no Ducking. Freeze optional | Near-frozen tails on key line endings (Q23) |
| 2 | Pro-Q | Band-limit to about 300 Hz–5 kHz | Frozen tails stay out of the low end and don't hiss |

**Send:** LEAD's send to FX · THROW sits at zero except during throws.

**Buildable:** yes. Pro-R 2's Space, Decay Rate (50–200%), Vintage style, Brightness, Thickness, Ducking and Freeze, and Saturn 2's Warm Tape, are all confirmed (foundation §1).

## Buses

- **VOX BUS:** one slot. Pro-C, Opto style, 1–2 dB of glue.
- **VOX GROUP:** empty.

## DBL

**DBL IN L / DBL IN R:** the foundation front end (rumble cut, gentle expander, Auto-Tune matching VOX IN), panned L70 / R70.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Low cut ~120 Hz, box | The lead carries the body |
| 2 | Pro-C | Tighter compression than the lead | Steady doubles blend better |
| 3 | Saturn 2 | Warm Tape | Matches the lead's grain |
| 4 | Pro-Q | Darker than the lead | Keeps the lead in front |
| 5 | Pro-DS | Harder de-essing | S's stack up across takes, and the hall exaggerates them |

**Level:** 6–10 dB under LEAD. **Send:** FX · HALL only, 6 dB below LEAD's send. Throws stay a solo-voice moment.

## Key moves

| # | Move | Track › Parameter | When | Why |
|---|---|---|---|---|
| 1 | Cathedral throw | LEAD › send to FX · THROW | Last word of key lines | The signature moment (Q23) |
| 2 | Hall eases | LEAD › send to FX · HALL | Dense rap lines | Keeps words readable in the fastest bars |
| 3 | Endless ending (optional) | FX · THROW › Pro-R 2 Freeze | The song's final word | Lets the last tail hang forever |

From/to values are set in Step 3.

## Ear checks

Added in Step 5.

## Translation notes

- **Quiet listening:** this preset's biggest risk, because it's the wettest. Every word still has to read at low volume. Step 4 checks it.
- **Small speakers:** with the top rolled off, presence matters even more on phones. That's why 2–4 kHz is protected.
- **Mono:** the hall and the throws are the stereo elements. Check they don't go hollow.
