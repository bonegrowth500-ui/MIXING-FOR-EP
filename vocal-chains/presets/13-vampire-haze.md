# 13 · Vampire Haze

Dark, gothic and drenched: an empty cathedral at 3 AM, with the top rolled soft and long, heavy tails.

**Status:** dialed in (Step 3). Stress-tested in Step 4.
**Placement:** leans into the beat (D6) · **Tune:** Fast · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R.
3. **Key moves:** place the throws and the hall eases (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Dark and warm (Q24). Low cut at 80 Hz, low-mid warmth +2–3 dB near 220 Hz, top rolled off above about 8 kHz by 4–6 dB. 2–4 kHz stays put so rapped words still read: dark, not buried |
| Density | 9–11 dB total, with warm tape saturation |
| Grit | Warm tape on the lead, plus a tape-saturated hall return: the "dirty fog" |
| Space | The wettest of the five. A dark 2–3 s hall (Vintage style) with 50 ms of pre-delay, ducked by the voice. Near-frozen throws on the last word of key lines (Q23). Wet 5/5 |
| Width | Lead mono. Doubles at L/R 70. Hall and throws fully wide |
| Placement | Leans into the beat: the least presence and the most wet of the five |
| Tune | Fast: retune 10–20, humanize and Flex-Tune around 20 |

## Upgrades (Q27)

- **Throws on their own return.** A separate near-frozen return lets the main hall stay a tidy 2–3 s. (Phase 1 put freeze and long throws on the hall itself.)
- **Grainier hall.** Pro-R 2's Vintage style gives the space an older, grainier character before the tape even touches it.
- **Low-mid bloom control.** A multiband stage keeps the added warmth from turning into boom when room box and long tails stack up.
- **Band-limited throws.** The frozen tails are filtered to about 300 Hz–5 kHz, so they never cloud the low end or hiss.

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD | — | 0 dB |
| LEAD | VOX IN | VOX BUS | FX · HALL 100%, FX · THROW 0% (automated only) | 0 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L70 / R70 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · HALL 100% | −8 dB |
| FX · HALL | Sends | VOX GROUP | — | −8 dB |
| FX · THROW | Sends | VOX GROUP | — | −10 dB |
| VOX BUS | LEAD, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX tracks | Master | — | Set against the beat, with peaks at or below −6 dBFS |

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct · Zero Latency | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −45 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | In a sound this wet, breaths turn into long, ghostly tails. Taking them down here keeps them out of the hall |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 15 · Humanize 20 · Flex-Tune 20 · Natural Vibrato 0 · Formant off · Classic Mode off | Quick correction that still lets the melancholy slides through |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 80 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −4 dB · optional: a narrow dynamic cut on any ringing resonance · Zero Latency | Box control matters more here, because a long reverb exaggerates boxiness |
| 2 | Pro-C | Classic style · Ratio 4:1 · Attack 3 ms · Release 80 ms · Knee 9 dB · Threshold about −15 dB, for 3–5 dB GR · Gain to level-match | Peaks would splash the hall and the throws |
| 3 | Pro-Q | Bell 220 Hz, Q 0.7, +2.5 dB | Warm body for the gothic weight |
| 4 | Saturn 2 | 1 band · Warm Tape · Drive 25% · Mix 60% · HQ on · Level to match | Thickens the darkness (Phase 1). Warm Tape adds lows and gently softens the very top |
| 5 | Pro-C | Opto style · Ratio 3:1 · Attack 10 ms · Release Auto · Knee 18 dB · Threshold about −19 dB, for 2–3 dB GR · Gain to level-match | A steady level into the hall means steady tails |
| 6 | Pro-Q | High Shelf 8 kHz, Q 0.7, −5 dB · High Cut 14 kHz, 12 dB/oct | The dark half of the tone curve (Q24), leaving 2–4 kHz alone |
| 7 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB, for 3–5 dB on S's · Range 10 dB · detection 4.5–10 kHz · Lookahead 5 ms | S's in a long hall and in the throws turn into splashes, so they're caught before the sends. The detection sits a little lower to match the darker tone |
| 8 | Pro-MB | Band 1: 150–450 Hz · Compress, downward · Ratio 3:1 · Range 4 dB · Attack 10 ms · Release 150 ms. Band 2: 2.5–5 kHz · Compress, downward · Ratio 3:1 · Range 3 dB · Attack 2 ms · Release 80 ms. Each threshold set so the band only acts when it builds | Warmth, room box and long tails can add up to boom (band 1). Band 2 catches upper-mid spikes |
| 9 | Pro-Q | Bell 1.2 kHz, Q 1.0, −1 dB | Takes a little forwardness out of the mids, so the lead leans back into the beat without losing the 2–4 kHz words |
| 10 | Pro-L 2 | Transparent style · Gain +2 dB, raised until the loudest lines show 1–2 dB GR · Output −3.0 dBFS · Lookahead 3 ms | Keeps what goes into the hall and throws consistent |

**Density check:** about 4 + 1.5 + 2.5 + 1.5 dB, roughly 9.5 dB total (target 9–11). Pro-MB only adds when a band builds.

**Order notes:** the darkening EQ (6) comes before the de-esser (7), so it de-esses the final tone. Everything that feeds the hall and the throws is under control before the sends.

## Parallel tracks

None. This preset's character lives in the space, so it doesn't need a parallel layer.

## FX returns

**The throw and dark-return engine.**

### FX · HALL

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Vintage style · Space 2.5 s · Decay Rate 100% · Predelay 50 ms · Brightness −50% · Character 40% · Distance 50% · Thickness 50% · Stereo Width 100% · Mix 100% · Ducking about 8 dB | The long dark hall (Q23). Heavy ducking keeps the words clear through a 5/5-wet sound (D15) |
| 2 | Saturn 2 | 1 band · Warm Tape · Drive 35% · Mix 100% · HQ on · Level to match | Turns the tail into Phase 1's dirty fog |
| 3 | Pro-Q | Low Cut 200 Hz, 12 dB/oct · Low Cut 400 Hz on Side only · High Cut 6 kHz, 12 dB/oct · Zero Latency | Dark, out of the low end, with mono lows (D7) |

**Level:** fader at −8 dB.

### FX · THROW

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Vintage style · Space at maximum (about 10 s) · Decay Rate 400% (use 200% if that's your maximum) · Predelay 0 ms · Brightness −60% · Character 30% · Distance 60% · Thickness 40% · Stereo Width 100% · Mix 100% · Ducking off · Freeze off | A tail long enough to feel frozen, on key line endings only (Q23) |
| 2 | Pro-Q | Low Cut 300 Hz, 24 dB/oct · High Cut 5 kHz, 24 dB/oct · Zero Latency | Frozen tails stay out of the low end and don't hiss |

**Level:** fader at −10 dB. LEAD's send to this track sits at 0% except during throws.

**Buildable:** yes. Pro-R 2's Space, Decay Rate, Vintage style, Brightness, Thickness, Ducking and Freeze, and Saturn 2's Warm Tape, are all confirmed (foundation §1).

## Buses

| Track | Slot | Plugin | Settings | Why |
|---|---|---|---|---|
| VOX BUS | 1 | Pro-C | Opto style · Ratio 2:1 · Attack 30 ms · Release Auto · Knee 18 dB · Threshold about −12 dB, for 1–2 dB GR · Gain to level-match | Glues the lead and doubles before the space takes over |

VOX GROUP stays empty.

## DBL

**DBL IN L / DBL IN R:** the VOX IN chain exactly (same three slots, same settings), faders at 0 dB, panned L70 / R70.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 120 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −4 dB · Zero Latency | The lead carries the body |
| 2 | Pro-C | Classic style · Ratio 6:1 · Attack 3 ms · Release 80 ms · Knee 9 dB · Threshold about −17 dB, for 5–7 dB GR · Gain to level-match | Tighter than the lead, so the doubles blend |
| 3 | Saturn 2 | 1 band · Warm Tape · Drive 25% · Mix 60% · HQ on · Level to match | Matches the lead's grain |
| 4 | Pro-Q | High Shelf 7 kHz, −6 dB · Bell 3 kHz, Q 1.0, −1.5 dB | Darker than the lead, so the lead stays in front |
| 5 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB · Range 12 dB · detection 4.5–10 kHz | S's stack up across takes, and the hall exaggerates them |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · HALL only, at 100%, which lands 6–10 dB below LEAD's because sends are post-fader. Throws stay a solo-voice moment.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Cathedral throw | LEAD › send to FX · THROW | 0% → 100% → 0% | The last word of key lines: open just before the word, close right after it | The signature moment (Q23). Only that word feeds the frozen tail |
| 2 | Hall eases | LEAD › send to FX · HALL | 100% → 60% → 100% | Dense rap lines | Keeps words readable in the fastest bars |
| 3 | Endless ending (optional) | FX · THROW › Pro-R 2 Freeze | Off → on | Right after the song's final word enters the throw | Lets the last tail hang forever |

## Ear checks

Added in Step 5.

## Translation notes

- **Quiet listening:** this preset's biggest risk, because it's the wettest. Every word still has to read at low volume. Step 4 checks it.
- **Small speakers:** with the top rolled off, presence matters even more on phones. That's why 2–4 kHz is protected.
- **Mono:** the hall and the throws are the stereo elements. Check they don't go hollow.
