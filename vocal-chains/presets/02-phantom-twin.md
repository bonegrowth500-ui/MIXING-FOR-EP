# 02 · Phantom Twin

A clean, bright lead on top, shadowed word for word by a dark, distorted twin an octave down at ghost level.

**Status:** blueprint (Step 2). Settings get dialed in during Step 3.
**Placement:** on top (D6) · **Tune:** Hard · **Builds on:** [foundation](00-foundation.md)

## Sound targets

| Target | Value |
|---|---|
| Tone | **Lead:** clean and bright. Low cut at 80 Hz, body +2 dB near 200 Hz, presence left to the mic, air lifted moderately (a notch below Neon Bleach). **Demon:** confined to about 150 Hz–3 kHz, dark |
| Density | **Lead:** 10–12 dB total. **Demon:** squeezed hard and flattened further by its distortion, so its level barely moves |
| Grit | The lead stays clean, with tube density only. All the audible dirt lives on the demon |
| Space | Two rooms. The lead gets a bright stereo 1/4-note delay about 18 dB under it, softly ducked. The demon gets a dark short room of about 1 s. Overall wet 2/5 |
| Width | Lead and demon mono. Doubles at L/R 70. Width comes from the doubles and the delay |
| Placement | On top, with the demon 12–18 dB under the lead (Q17) |
| Tune | Hard: retune 0–5, humanize and Flex-Tune low |

## Upgrades (Q27)

Phase 1 had none of these. Each one protects the "felt, not heard" ghost.
- **Gate before the distortion.** The demon gets its own hard gate ahead of Saturn, so distortion never turns breaths or room tone into noise.
- **Locked ghost level.** A compressor before the distortion and a ceiling after it hold the twin at a constant level. It can't poke out on a loud word.
- **Ducked angel delay.** The lead's delay dips while you sing, so the clean half stays clean.

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. The demon's Auto-Tune stays on Chromatic (D20).
3. **Key moves:** place the demon surges and the delay throws.

## Track map

| Track | Gets audio from | Routes to | Sends |
|---|---|---|---|
| VOX IN | Lead clips | LEAD, PAR · DEMON | — |
| LEAD | VOX IN | VOX BUS | FX · DELAY |
| PAR · DEMON | VOX IN | VOX BUS | FX · VERB |
| DBL IN L / R | Left / right double clips | DBL, panned L70 / R70 | — |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · DELAY, 6 dB below LEAD's send |
| FX · DELAY | Sends | VOX GROUP | — |
| FX · VERB | Sends | VOX GROUP | — |
| VOX BUS | LEAD, PAR · DEMON, DBL | VOX GROUP | — |
| VOX GROUP | VOX BUS, FX tracks | Master | — |

## VOX IN

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Rumble cut | Foundation standard |
| 2 | Pro-G | Gentle expander | Takes breaths and room down before compression and the demon's distortion can lift them |
| 3 | Auto-Tune Artist | Hard tune in the song's key | The angel's snap. The lead and the demon both inherit it |

## LEAD

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Corrective: low cut, box, resonances | Cleans the angel before any compressor reacts to it |
| 2 | Pro-C | Compressor 1: fast peak catcher | Hard tune makes rapped syllables spiky. Catching peaks early keeps the clean lead steady |
| 3 | Pro-Q | Tone: body support | Adds the chest a thin voice lacks, right before saturation thickens it |
| 4 | Saturn 2 | Subtle tube density | Density with no audible grit, so the dirt stays on the demon's side |
| 5 | Pro-C | Compressor 2: leveler | An even lead keeps the ghost ratio constant from line to line |
| 6 | Fresh Air | Brightness and air | The angel half: bright, a notch below Neon Bleach |
| 7 | Pro-DS | De-esser | Catches the S's the air stage brought up |
| 8 | Pro-Q | Dynamic control, 3–5 kHz | Keeps loud hard-tuned notes from turning sharp |
| 9 | Pro-Q | Polish: final tilt | Sets the lead's contrast against the dark twin |
| 10 | Pro-L 2 | Peak control | Keeps the lead on top without spikes |

**Order notes:** body EQ (3) comes before saturation (4), so the saturation thickens the new body. The de-esser (7) follows the air (6), so it catches every S the air lifted.

## Parallel tracks

### PAR · DEMON (the demon engine)

**Feed:** VOX IN. The demon starts from the tuned but unprocessed voice, so it's dark from the source instead of inheriting the lead's brightening.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-G | Hard gate | Silence between words, so the distortion only ever sees voice |
| 2 | Auto-Tune Artist | Transpose −12, Formant on, Throat above 100, Chromatic, minimal correction | An octave down with a darker formant (Q18). Formant keeps it a voice instead of a cartoon, and a longer throat makes it bigger and darker. Chromatic works because the input is already tuned (D20) |
| 3 | Pro-C | Hard compression | Feeds the distortion a steady level, so the grit doesn't come and go |
| 4 | Saturn 2 | Heavy distortion, HQ on | The demon's texture (D18) |
| 5 | Pro-Q | Band-limit to about 150 Hz–3 kHz, Zero Latency | Keeps the twin under the lead's presence and out of the beat's sub |
| 6 | Pro-L 2 | Ghost ceiling, lookahead 0 | The twin can never poke out on a loud word (Q17) |

**Level:** 12–18 dB under LEAD at VOX BUS. Mono (D7).

**Buildable:** yes. Transpose −12 is Auto-Tune's limit. Formant and Throat need the Modern algorithm (D16), and Throat stays inside 80–140 (foundation §1). The gate, distortion, EQ and limiter controls are all confirmed or long-standing.

## FX returns

### FX · DELAY (the angel's delay)

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Timeless 3 | Stereo 1/4-note delay with bright filtering. The envelope follower pulls the Mix down while you sing | Phase 1's bright delay, ducked so the angel stays clean (D15) |
| 2 | Pro-Q | Low cut, lows kept mono | D7 |

### FX · VERB (the demon's room)

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Dark short room, about 1 s, narrow width | The demon's own darker room: Phase 1's "two rooms" |
| 2 | Pro-Q | Low cut ~200 Hz, high cut ~4 kHz | Keeps the demon's room dark and out of the low end |

## Buses

- **VOX BUS:** one slot. Pro-C, Bus style, 1–2 dB of glue, so the angel, the demon and the doubles read as one performance.
- **VOX GROUP:** empty.

## DBL

**DBL IN L / DBL IN R:** the foundation front end (rumble cut, gentle expander, Auto-Tune matching VOX IN), panned L70 / R70.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Low cut ~120 Hz, box | The lead carries the body |
| 2 | Pro-C | Tighter compression than the lead | Steady doubles blend better |
| 3 | Saturn 2 | Subtle tube | Matches the lead's density |
| 4 | Fresh Air | Set lower than the lead | Bright, but a step behind |
| 5 | Pro-DS | Harder de-essing | S's stack up across takes |
| 6 | Pro-Q | Tone offset: less 3–5 kHz and air | Keeps the lead in front |

**Level:** 6–10 dB under LEAD. **Send:** FX · DELAY, 6 dB below LEAD's send.

## Key moves

| # | Move | Track › Parameter | When | Why |
|---|---|---|---|---|
| 1 | Demon surge | PAR · DEMON › fader | Punchlines and key words | Phase 1's signature: the twin steps forward for a moment |
| 2 | Delay throw | LEAD › send to FX · DELAY | Last word of hook lines | Lifts the angel's line endings |

From/to values are set in Step 3.

## Ear checks

Added in Step 5.

## Translation notes

- **Mono:** the lead and the demon are mono by design. Only the doubles and the delay carry width, so those two get the mono check.
- **Small speakers:** most of the demon's weight sits below 300 Hz and fades on phones. Its distortion harmonics up to 3 kHz keep a trace of it there, which is intended.
- **Loud playback:** the demon is high-passed at about 150 Hz, so it never fights the 808.
