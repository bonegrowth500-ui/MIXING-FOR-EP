# 04 · Neon Bleach

Glossy, very bright and expensive: a hard-tuned lead right in your face, with crystalline air on top.

**Status:** blueprint (Step 2). Settings get dialed in during Step 3.
**Placement:** on top, the most upfront of the five (D6) · **Tune:** Hard · **Builds on:** [foundation](00-foundation.md)

## Sound targets

| Target | Value |
|---|---|
| Tone | Very bright (Q19). Low cut at 80 Hz. Body +2 dB near 200 Hz, because bright chains make a thin voice thinner. Presence mostly from the mic. Strong air from Fresh Air plus a gentle 12 kHz shelf, about +4–6 dB of top end beyond the mic's own. S's held by a de-esser after all the brightness |
| Density | 11–13 dB total: a fast FET-style grab, then smooth opto leveling |
| Grit | Hidden. Saturn is blended in parallel inside the plugin, adding loudness with no audible dirt |
| Space | A soft 1/8 ping-pong bed that ducks while you sing and blooms in the gaps (Q20), 16–20 dB under the lead. A short bright plate of about 1 s, kept low. Wet 2/5 |
| Width | Lead mono. The widest doubles of the five (L/R 90), the ping-pong's motion, and an octave-up ghost layer chorused wide, 14–18 dB under the lead |
| Placement | On top, most upfront: the most presence and density of the five |
| Tune | Hard: retune 0–3, with the lowest humanize and Flex-Tune of the five |

## Upgrades (Q27)

- **Dynamic air.** Phase 1's single big air shelf becomes Fresh Air, which rises and falls with the voice, followed by a gentle static shelf. That gives more sparkle with less sibilance.
- **Harsh-zone clamp.** A dynamic band on 3–5 kHz after the de-esser catches loud notes that go glassy under hard tune.
- **Ghost layer built as an octave up.** Phase 1's ghost harmony becomes an octave-up layer. It always lands in key and needs no per-song setup (D11).

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. PAR · OCT UP stays on Chromatic (D20).
3. **Key moves:** place the hook lifts and the bed dips.

## Track map

| Track | Gets audio from | Routes to | Sends |
|---|---|---|---|
| VOX IN | Lead clips | LEAD | — |
| LEAD | VOX IN | VOX BUS, PAR · OCT UP | FX · DELAY, FX · PLATE |
| PAR · OCT UP | LEAD | VOX BUS | FX · PLATE, a little |
| DBL IN L / R | Left / right double clips | DBL, panned L90 / R90 | — |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · DELAY and FX · PLATE, 6 dB below LEAD's sends |
| FX · DELAY | Sends | VOX GROUP | — |
| FX · PLATE | Sends | VOX GROUP | — |
| VOX BUS | LEAD, PAR · OCT UP, DBL | VOX GROUP | — |
| VOX GROUP | VOX BUS, FX tracks | Master | — |

## VOX IN

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Rumble cut | Foundation standard |
| 2 | Pro-G | Gentle expander | A very bright chain makes breaths bright too. Taking them down early keeps them from sparkling |
| 3 | Auto-Tune Artist | Hard tune in the song's key | Every note snaps. The gloss starts here |

## LEAD

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Corrective: low cut, box, resonances | A very bright chain exaggerates every resonance, so they go first |
| 2 | Pro-C | Compressor 1: fast FET-style grab | Grabs peaks instantly for the dense, glossy sound (Phase 1) |
| 3 | Pro-Q | Tone: body support | Body first, before the brightness |
| 4 | Saturn 2 | Hidden parallel saturation (band Mix) | Loudness and density without audible dirt (Phase 1's Ken DNA) |
| 5 | Pro-C | Compressor 2: smooth opto leveling | Glues each line into a steady, expensive level (Phase 1) |
| 6 | Fresh Air | Dynamic air and presence | Air that follows the voice (upgrade) |
| 7 | Pro-Q | Gentle static air shelf | Finishes Phase 1's big air shelf on top of Fresh Air |
| 8 | Pro-DS | De-esser | Every brightness stage is behind it, so it catches all the lifted S's (Phase 1) |
| 9 | Pro-Q | Dynamic control, 3–5 kHz | Clamps loud notes that turn glassy, only when they spike (upgrade) |
| 10 | Pro-L 2 | Peak control | Holds the most upfront lead of the five flat |

**Order notes:** both brightness stages (6, 7) sit before the de-esser (8), so it sees the final top end. The harsh-zone clamp (9) comes after the de-esser, so it only deals with glassy notes, not S's. This moves de-essing and dynamic control one slot later than the foundation template to make room for the second air stage.

## Parallel tracks

### PAR · OCT UP (the ghost layer)

**Feed:** LEAD. The layer inherits the finished gloss, compression and de-essing before it's shifted, so it arrives as a bright, controlled voice.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Auto-Tune Artist | Transpose +12, Formant on, Chromatic, minimal correction | An octave up that stays a voice, not a chipmunk. Always in key (D20) |
| 2 | Pro-Q | High-pass ~400 Hz, tame the harsh top, Zero Latency | Shimmer only, no low-mid clutter |
| 3 | Pro-C | Steady level | A ghost has to stay constant |
| 4 | Vintage Chorus | Wide stereo spread | Phase 1's "tucked wide". The lead stays mono |

**Level:** 14–18 dB under LEAD at VOX BUS.

**Buildable:** yes. Transpose +12 is within Auto-Tune's ±12, Formant needs the Modern algorithm (D16), and Vintage Chorus is FL stock (foundation §1).

## FX returns

### FX · DELAY (the soft bed)

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Timeless 3 | 1/8 ping-pong with HP/LP filtering. The envelope follower pulls the Mix down while you sing | Q20: ducks under the words and blooms in the gaps (D15) |
| 2 | Pro-Q | Low cut, lows kept mono | D7 |

### FX · PLATE

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Plate style, about 1 s, bright | Phase 1's short bright plate |
| 2 | Pro-Q | Low cut ~250 Hz | Keeps the plate off the body |

## Buses

- **VOX BUS:** one slot. Pro-C, Bus style, 1–2 dB of glue.
- **VOX GROUP:** empty.

## DBL

**DBL IN L / DBL IN R:** the foundation front end (rumble cut, gentle expander, Auto-Tune matching VOX IN), panned L90 / R90.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Low cut ~120 Hz, box | The lead carries the body |
| 2 | Pro-C | Tighter compression than the lead | Steady doubles blend better |
| 3 | Saturn 2 | Hidden saturation, as on the lead | Matching density |
| 4 | Fresh Air | Set lower than the lead | Bright, but a step behind |
| 5 | Pro-DS | Harder de-essing | Very bright doubles stack S's fastest |
| 6 | Pro-Q | Tone offset: less 3–5 kHz and air | Keeps the lead in front |

**Level:** 6–10 dB under LEAD. **Sends:** FX · DELAY and FX · PLATE, 6 dB below LEAD's.

## Key moves

No throws here: Q20 chose a soft bed.

| # | Move | Track › Parameter | When | Why |
|---|---|---|---|---|
| 1 | Ghost opens | PAR · OCT UP › fader | Hooks | More gloss where it counts, cleaner verses |
| 2 | Air lift | LEAD › Fresh Air High Air | Hooks | Extra shine on the hook |
| 3 | Bed dips | LEAD › send to FX · DELAY | Dense rap lines | Keeps fast bars clear |

From/to values are set in Step 3.

## Ear checks

Added in Step 5.

## Translation notes

- **Small speakers:** phones exaggerate 2–5 kHz, so the de-esser and the harsh-zone clamp matter most there. Test on a phone first.
- **Mono:** the ping-pong folds into a single repeating echo, and the ghost's chorus narrows. Both are fine at their levels.
- **Loud playback:** very bright chains tire the ear at volume. The de-esser after the air stages is the safeguard.
