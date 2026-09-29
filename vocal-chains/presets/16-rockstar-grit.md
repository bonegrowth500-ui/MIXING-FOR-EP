# 16 · Rockstar Grit

Upfront, gritty and rock-coded: amp-driven snarl, biting mids and a classic slapback, still tuned.

**Status:** blueprint (Step 2). Settings get dialed in during Step 3.
**Placement:** on top (D6) · **Tune:** Fast · **Builds on:** [foundation](00-foundation.md)

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

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R.
3. **Key moves:** place the crunch pushes, plus the yell guard if a yell still spikes.

## Track map

| Track | Gets audio from | Routes to | Sends |
|---|---|---|---|
| VOX IN | Lead clips | LEAD | — |
| LEAD | VOX IN | VOX BUS, PAR · CRUNCH | FX · SLAP, FX · ROOM |
| PAR · CRUNCH | LEAD | VOX BUS | — |
| DBL IN L / R | Left / right double clips | DBL, panned L60 / R60 | — |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · ROOM, 6 dB below LEAD's send |
| FX · SLAP | Sends | VOX GROUP | — |
| FX · ROOM | Sends | VOX GROUP | — |
| VOX BUS | LEAD, PAR · CRUNCH, DBL | VOX GROUP | — |
| VOX GROUP | VOX BUS, FX tracks | Master | — |

## VOX IN

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Rumble cut | Foundation standard |
| 2 | Pro-G | Gentle expander | Distortion lifts everything quiet, so breaths and room go down before the grit sees them |
| 3 | Auto-Tune Artist | Fast tune in the song's key | Still tuned (Phase 1), but loose enough at the edges for yells and rap |

## LEAD

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Corrective: low cut at 90 Hz, box | A tighter low end: rock vocals sit higher |
| 2 | Pro-C | Compressor 1: aggressive fast grab | The rock pump from Phase 1, and the first line of yell control (Q26) |
| 3 | Pro-Q | Tone: body and midrange snarl | Shapes where the grit will bite |
| 4 | Saturn 2 | Inline grit, moderate | The first half of the crunch. The parallel layer adds the snarl |
| 5 | Pro-C | Compressor 2: leveler | Keeps the saturated line steady |
| 6 | Fresh Air | Bite, led by Mid Air | Upper-mid bite with a little air |
| 7 | Pro-DS | De-esser | Distortion and air both sharpen S's |
| 8 | Pro-MB | Yell control | Clamps the upper mids only when a yell spikes (Q26) |
| 9 | Pro-Q | Polish: presence contour | Final bite and tilt |
| 10 | Pro-L 2 | Peak control | The last catch for yells (Q26) |

**Order notes:** the yell clamp (8) sits after the de-esser (7), so it only handles yell harshness. Compression on both sides of the saturation (2, 5) keeps the grit steady whether you're talking or yelling.

## Parallel tracks

### PAR · CRUNCH (the crunch engine)

**Feed:** LEAD. The amp gets the finished, compressed lead, so yells arrive under control.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-G | Gate, lookahead 0 | The distortion only ever sees voice |
| 2 | Pro-Q | High-pass ~250 Hz, Zero Latency | Tight distortion: no low end going into the amp |
| 3 | Saturn 2 | Amp: British Rock, HQ on | The crunch (Q25) |
| 4 | Pro-Q | Low-pass ~7 kHz, fizz notch, Zero Latency | Snarl without fizz |
| 5 | Pro-C | Steady level | Keeps the snarl a constant support layer |

**Level:** 6–10 dB under LEAD at VOX BUS. Mono (D7). It's at the same pitch as the lead, so it connects through mixer routes only and relies on FL's automatic delay compensation (D5, D18).

**Buildable:** yes. Saturn 2's British Rock amp style is confirmed (the exact on-screen label is a Check item), and Pro-G, Pro-Q and Pro-C are confirmed (foundation §1).

### Yell control inside the chain (Q26)

Four layers, no second chain:
1. LEAD slot 2: the fast compressor grabs the yell's front edge.
2. LEAD slot 8: Pro-MB clamps upper-mid harshness only when it spikes.
3. LEAD slot 10: Pro-L 2 catches whatever is left.
4. PAR · CRUNCH is fed after all of that, so the amp never gets an uncontrolled yell.

## FX returns

### FX · SLAP

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Timeless 3 | About 100 ms slap set in ms (not synced), Tape mode, a touch of Drive, little feedback, vintage filtering, centered | Phase 1's classic rock slapback |
| 2 | Pro-Q | Low cut ~300 Hz | Keeps the slap off the body |

### FX · ROOM

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Small live room, about 0.7 s, lively Character | Phase 1's small live room |
| 2 | Pro-Q | Low cut ~250 Hz, lows kept mono | D7 |

## Buses

- **VOX BUS:** one slot. Pro-C, 1–2 dB of punchy glue.
- **VOX GROUP:** empty.

## DBL

**DBL IN L / DBL IN R:** the foundation front end (rumble cut, gentle expander, Auto-Tune matching VOX IN), panned L60 / R60.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Low cut ~130 Hz, box | The lead carries the body |
| 2 | Pro-C | Aggressive compression | Rock doubles sit flat and dense |
| 3 | Saturn 2 | Amp crunch, more than the lead | A gang-vocal edge (upgrade) |
| 4 | Pro-Q | Band-limit, less presence than the lead | Keeps the lead in front |
| 5 | Pro-DS | Harder de-essing | Crunch sharpens S's, and they stack across takes |

**Level:** 6–10 dB under LEAD. **Send:** FX · ROOM, 6 dB below LEAD's send.

## Key moves

| # | Move | Track › Parameter | When | Why |
|---|---|---|---|---|
| 1 | Crunch push | PAR · CRUNCH › fader | Hooks | More snarl where the energy peaks |
| 2 | Yell guard | PAR · CRUNCH › fader | The biggest yell of the song, only if needed | The chain already handles yells (Q26). This is the safety for one that still spikes |

From/to values are set in Step 3.

## Ear checks

Added in Step 5.

## Translation notes

- **Loud playback:** this preset's biggest risk. Grit plus bite can turn harsh at volume, and the Pro-MB clamp and the crunch's low-pass are the guard. Step 4 checks it.
- **Small speakers:** crunch fizz shows up on phones first. The ~7 kHz low-pass handles it.
- **Mono:** nearly everything is centered. The room and the doubles are the only width.
