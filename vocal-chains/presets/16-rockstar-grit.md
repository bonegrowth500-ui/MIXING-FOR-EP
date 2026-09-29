# 16 · Rockstar Grit

Upfront, gritty and rock-coded: amp-driven snarl, biting mids and a classic slapback, still tuned.

**Status:** dialed in (Step 3). Stress-tested in Step 4.
**Placement:** on top (D6) · **Tune:** Fast · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R.
3. **Key moves:** place the crunch pushes, plus the yell guard if a yell still spikes (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Biting mids. Low cut at 90 Hz, body +1.5–2 dB near 200 Hz, snarl around 1–2 kHz. Presence raised carefully, since the mic already adds about 3.5 dB at 4 kHz. Moderate air, led by Mid Air rather than High Air |
| Density | 12–14 dB total including saturation: the most compressed of the five |
| Grit | Crunch (Q25): moderate saturation in the lead, plus a parallel British Rock amp layer 6–10 dB under the lead |
| Space | A ~100 ms slapback plus a small live room of about 0.7 s. Wet 2/5 |
| Width | The narrowest of the five. Lead, crunch and slap centered. Doubles at L/R 60. Room about 70% wide |
| Placement | On top |
| Tune | Fast: retune 10–15, humanize around 15, Flex-Tune 15–20 so yells and rap pass naturally |

## Upgrades (Q27)

- **Crunch fed from the finished lead.** Yells reach the amp already controlled, so the crunch stays consistent instead of exploding.
- **Gate before the amp.** Distortion never turns breaths into noise.
- **Band-limited snarl.** The crunch is kept between about 250 Hz and 7 kHz, so it bites without fizz or mud.
- **Tape slap.** The slapback uses Timeless's Tape mode with a touch of Drive, for a vintage feel.
- **Crunchier doubles.** The doubles get more amp than the lead, for a gang-vocal edge.

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD | — | 0 dB |
| LEAD | VOX IN | VOX BUS, and PAR · CRUNCH at 100% | FX · SLAP 100%, FX · ROOM 100% | 0 dB |
| PAR · CRUNCH | LEAD | VOX BUS | — | −4 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L60 / R60 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · ROOM 100% | −8 dB |
| FX · SLAP | Sends | VOX GROUP | — | −14 dB |
| FX · ROOM | Sends | VOX GROUP | — | −16 dB |
| VOX BUS | LEAD, PAR · CRUNCH, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX tracks | Master | — | Set against the beat, with peaks at or below −6 dBFS |

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct · Zero Latency | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −45 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | Distortion lifts everything quiet, so breaths and room go down before the grit sees them |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 12 · Humanize 15 · Flex-Tune 18 · Natural Vibrato 0 · Formant off · Classic Mode off | Still tuned (Phase 1), but loose enough at the edges for yells and rap |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 90 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · Zero Latency | A tighter low end: rock vocals sit higher |
| 2 | Pro-C | Punch style · Ratio 8:1 · Attack 0.3 ms · Release 40 ms · Knee 3 dB · Threshold about −16 dB, for 5–6 dB GR · Gain to level-match | Phase 1's rock pump, and the first line of yell control (Q26) |
| 3 | Pro-Q | Bell 200 Hz, Q 0.8, +1.5 dB · Bell 1.5 kHz, Q 1.0, +2 dB | Body, plus the snarl zone where the grit will bite |
| 4 | Saturn 2 | 1 band · Warm Tube · Drive 30% · Mix 50% · HQ on · Level to match | The first half of the crunch. A tube here, so the parallel amp layer adds a different color |
| 5 | Pro-C | Classic style · Ratio 4:1 · Attack 5 ms · Release 100 ms · Knee 12 dB · Threshold about −19 dB, for 3–4 dB GR · Gain to level-match | Keeps the saturated line steady |
| 6 | Fresh Air | Mid Air 30% · High Air 20% · Trim to level-match | Upper-mid bite with a little air. Kept at 30% because the mic already peaks at 4 kHz |
| 7 | Pro-DS | Single Vocal · Split Band · Threshold −30 dB, for 3–6 dB on S's · Range 10 dB · detection 5–11 kHz · Lookahead 5 ms | Distortion and air both sharpen S's |
| 8 | Pro-MB | 1 band, 2–5 kHz · Compress mode · Range −6 dB (negative = downward, so the band's gain dips, never rises) · Ratio 4:1 · Attack 2 ms · Release 80 ms · Knee 6 dB · Lookahead 2 ms · Threshold lowered until only yells trigger 3–6 dB | Clamps upper-mid harshness only when a yell spikes (Q26) |
| 9 | Pro-Q | Bell 3 kHz, Q 1.2, +1 dB · High Shelf 10 kHz, +1 dB | Final bite, kept small because the mic already lifts 4 kHz |
| 10 | Pro-L 2 | Punchy style · Gain about +10 dB, adjusted until the loudest lines show 2–3 dB GR · Output −3.0 dBFS · Lookahead 1 ms | The last catch for yells (Q26). Punchy suits a single rock vocal |

**Density check:** about 5.5 + 2 + 3.5 + 2.5 dB, roughly 13.5 dB total (target 12–14). Pro-MB only adds on yells.

**Order notes:** the yell clamp (8) sits after the de-esser (7), so it only handles yell harshness. Compression on both sides of the saturation (2, 5) keeps the grit steady whether you're talking or yelling.

## Parallel tracks

### PAR · CRUNCH (the crunch engine)

**Feed:** LEAD, with the route at 100%. The amp gets the finished, compressed lead, so yells arrive under control.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-G | Classic style · Threshold −24 dB · Ratio ∞:1 · Range 40 dB · Attack 0.5 ms · Hold 40 ms · Release 80 ms · Lookahead 0 ms | The distortion only ever sees voice. The feed is the compressed, limited lead, which lifts breaths to roughly −33 to −23 dBFS, so this threshold sits well above the demon's |
| 2 | Pro-Q | Low Cut 250 Hz, 24 dB/oct · Zero Latency | Tight distortion: no low end going into the amp |
| 3 | Saturn 2 | 1 band · British Rock (Amp) · Drive 45% · Mix 100% · HQ on · Level to match | The crunch (Q25) |
| 4 | Pro-Q | High Cut 7 kHz, 24 dB/oct · Bell 5 kHz, Q 3, −3 dB (slide it to wherever fizz sits) · Zero Latency | Snarl without fizz |
| 5 | Pro-C | Classic style · Ratio 4:1 · Attack 5 ms · Release 80 ms · Knee 12 dB · Threshold about −10 dB, for 3–4 dB GR · Gain to level-match | Keeps the snarl a constant support layer |

**Level:** fader at −4 dB. The 250 Hz high-pass trims about 4 dB first, so that lands about 8 dB under LEAD. Adjust until it adds edge without pulling focus: 6–10 dB under. Mono (D7). It's at the same pitch as the lead, so it connects through mixer routes only and relies on FL's automatic delay compensation (D5, D18).

**Buildable:** yes. Saturn 2's British Rock amp style is confirmed (its exact on-screen label is a Check item), and Pro-G, Pro-Q and Pro-C are confirmed (foundation §1).

### Yell control inside the chain (Q26)

Four layers, no second chain:
1. LEAD slot 2: the fast compressor grabs the yell's front edge.
2. LEAD slot 8: Pro-MB clamps upper-mid harshness only when it spikes.
3. LEAD slot 10: Pro-L 2 catches whatever is left.
4. PAR · CRUNCH is fed after all of that, so the amp never gets an uncontrolled yell.

## FX returns

### FX · SLAP

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Timeless 3 | Sync off · 100 ms on both sides · Ping Pong off · Feedback 5% · Tape mode · Drive 20% · Filters: High Pass 300 Hz, Low Pass 5 kHz · Dry off · Wet 0 dB · no ducking | Phase 1's classic slapback. It's part of the sound, so it doesn't duck |
| 2 | Pro-Q | Low Cut 300 Hz, 12 dB/oct · Zero Latency | Keeps the slap off the body |

**Level:** fader at −14 dB.

### FX · ROOM

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Default style · Space 0.7 s · Decay Rate 100% · Predelay 10 ms · Brightness 0% · Character 60% · Distance 40% · Thickness 30% · Stereo Width 70% · Mix 100% · Ducking off | Phase 1's small live room. The high Character makes it lively |
| 2 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Low Cut 400 Hz on Side only · Zero Latency | Keeps the room off the body, with mono lows (D7) |

**Level:** fader at −16 dB.

## Buses

| Track | Slot | Plugin | Settings | Why |
|---|---|---|---|---|
| VOX BUS | 1 | Pro-C | Punch style · Ratio 2:1 · Attack 20 ms · Release Auto · Knee 6 dB · Threshold about −10 dB, for 1–2 dB GR · Gain to level-match | Punchy rock glue for the lead, crunch and doubles |

VOX GROUP stays empty.

## DBL

**DBL IN L / DBL IN R:** the VOX IN chain exactly (same three slots, same settings), faders at 0 dB, panned L60 / R60.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 130 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · Zero Latency | The lead carries the body |
| 2 | Pro-C | Punch style · Ratio 10:1 · Attack 0.5 ms · Release 40 ms · Knee 3 dB · Threshold about −19 dB, for 7–9 dB GR · Gain to level-match | Rock doubles sit flat and dense |
| 3 | Saturn 2 | 1 band · British Rock (Amp) · Drive 35% · Mix 60% · HQ on · Level to match | More amp than the lead, for a gang-vocal edge (upgrade) |
| 4 | Pro-Q | Bell 3.5 kHz, Q 1.0, −2 dB · High Cut 8 kHz, 12 dB/oct | Less presence than the lead, so the lead stays in front |
| 5 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB · Range 12 dB · detection 5–11 kHz | Crunch sharpens S's, and they stack across takes |
| 6 | Pro-L 2 | Punchy style · Output −3.0 dBFS · Gain about +10 dB, for 1–2 dB GR · Lookahead 1 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · ROOM at 100%, which lands 6–10 dB below LEAD's because sends are post-fader.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Crunch push | PAR · CRUNCH › fader | −4 dB → −1 dB | Hooks, with 1-beat ramps | More snarl where the energy peaks |
| 2 | Yell guard | PAR · CRUNCH › fader | −4 dB → −8 dB | The biggest yell of the song, only if needed | The chain already handles yells (Q26). This is the safety for one that still spikes |

## Ear checks

Added in Step 5.

## Translation notes

- **Loud playback:** this preset's biggest risk. Grit plus bite can turn harsh at volume, and the Pro-MB clamp and the crunch's high cut are the guard. Step 4 checks it.
- **Small speakers:** crunch fizz shows up on phones first. The 7 kHz high cut and the 5 kHz fizz notch handle it.
- **Mono:** nearly everything is centered. The room and the doubles are the only width.
