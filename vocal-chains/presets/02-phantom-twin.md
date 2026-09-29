# 02 · Phantom Twin

A clean, bright lead on top, shadowed word for word by a dark, distorted twin an octave down at ghost level.

**Status:** dialed in (Step 3). Stress-tested in Step 4.
**Placement:** on top (D6) · **Tune:** Hard · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. The demon's Auto-Tune stays on Chromatic (D20).
3. **Key moves:** place the demon surges and the delay throws in [Key moves](#key-moves).

## Sound targets

| Target | Value |
|---|---|
| Tone | **Lead:** clean and bright. Low cut at 80 Hz, body +2 dB near 200 Hz, presence left to the mic, air lifted moderately (a notch below Neon Bleach). **Demon:** confined to about 150 Hz–3 kHz, dark |
| Density | **Lead:** 10–12 dB total. **Demon:** squeezed hard and flattened further by its distortion, so its level barely moves |
| Grit | The lead stays clean, with tube density only. All the audible dirt lives on the demon |
| Space | Two rooms. The lead gets a bright stereo delay (1/4 left, dotted 1/8 right) about 18 dB under it, softly ducked. The demon gets a dark short room of about 1 s. Overall wet 2/5 |
| Width | Lead and demon mono. Doubles at L/R 70. Width comes from the doubles and the delay |
| Placement | On top, with the demon 12–18 dB under the lead (Q17) |
| Tune | Hard: retune 0–5, humanize and Flex-Tune low |

## Upgrades (Q27)

Phase 1 had none of these. Each one protects the "felt, not heard" ghost.
- **Gate before the distortion.** The demon gets its own hard gate ahead of Saturn, so distortion never turns breaths or room tone into noise.
- **Locked ghost level.** A compressor before the distortion and a ceiling after it hold the twin at a constant level. It can't poke out on a loud word.
- **Ducked angel delay.** The lead's delay dips while you sing, so the clean half stays clean.

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD, and PAR · DEMON at 100% | — | 0 dB |
| LEAD | VOX IN | VOX BUS | FX · DELAY 100% | 0 dB |
| PAR · DEMON | VOX IN | VOX BUS | FX · VERB 100% | −15 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L70 / R70 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · DELAY 100% | −8 dB |
| FX · DELAY | Sends | VOX GROUP | — | −18 dB |
| FX · VERB | Sends | VOX GROUP | — | −6 dB |
| VOX BUS | LEAD, PAR · DEMON, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX tracks | Master | — | Set against the beat, with peaks at or below −6 dBFS |

Sends are post-fader. The demon's send leaves an already quiet track, so FX · VERB's −6 dB puts the room about 6 dB under the demon.

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct · Zero Latency | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −45 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | Takes breaths and room down before compression and the demon's distortion can lift them |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 3 · Humanize 10 · Flex-Tune 10 · Natural Vibrato 0 · Formant off · Classic Mode off | The angel's snap, a hair softer than Neon Bleach. The lead and the demon both inherit it |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 80 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · optional: a narrow dynamic cut on any ringing resonance · Zero Latency | Cleans the angel before any compressor reacts to it |
| 2 | Pro-C | Clean style · Ratio 5:1 · Attack 1 ms · Release 60 ms · Knee 6 dB · Threshold about −16 dB, for 4–5 dB GR · Gain to level-match | Hard tune makes rapped syllables spiky. Catching them early keeps the clean lead steady, and Clean style adds no color |
| 3 | Pro-Q | Bell 200 Hz, Q 0.8, +2 dB | Adds the chest a thin voice lacks, right before saturation thickens it |
| 4 | Saturn 2 | 1 band · Clean Tube · Drive 15% · Mix 20% · HQ on · Level to match | Density with no audible grit, so the dirt stays on the demon's side |
| 5 | Pro-C | Vocal style · Ratio 3:1 · Attack 8 ms · Release Auto · Knee 18 dB · Threshold about −19 dB, for about 3 dB GR · Gain to level-match | An even lead keeps the ghost ratio constant from line to line |
| 6 | Fresh Air | Mid Air 20% · High Air 40% · Trim to level-match | The angel half: bright, but a notch below Neon Bleach's 25% / 55% |
| 7 | Pro-DS | Single Vocal · Split Band · Threshold −30 dB, for 3–5 dB on S's · Range 8 dB · detection 5–11 kHz · Lookahead 5 ms | Catches the S's the air stage lifted |
| 8 | Pro-Q | Bell 3.8 kHz, Q 1.5, dynamic −3 dB | Keeps loud hard-tuned notes from turning sharp |
| 9 | Pro-Q | Bell 300 Hz, Q 1.0, −1 dB · High Shelf 10 kHz, +1 dB | Leaves a little low-mid room for the demon and adds angel sheen: maximum contrast between the two |
| 10 | Pro-L 2 | Allround style · Gain about +10 dB, adjusted until the loudest lines show 1–3 dB GR · Output −3.0 dBFS · Lookahead 2 ms | Keeps the lead on top without spikes |

**Density check:** about 4.5 + 1 + 3 + 2 dB, roughly 10.5 dB total (target 10–12).

**Order notes:** body EQ (3) comes before saturation (4), so the saturation thickens the new body. The de-esser (7) follows the air (6), so it catches every S the air lifted.

## Parallel tracks

### PAR · DEMON (the demon engine)

**Feed:** VOX IN, with the route at 100%. The demon starts from the tuned but unprocessed voice, so it's dark from the source instead of inheriting the lead's brightening.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-G | Classic style · Threshold −35 dB · Ratio ∞:1 · Range 40 dB · Attack 0.5 ms · Hold 40 ms · Release 80 ms · Lookahead 0 ms | Silence between words, so the distortion only ever sees voice. Set it to open on every word and stay shut on breaths |
| 2 | Auto-Tune Artist | Alto/Tenor · Chromatic · Retune Speed 50 · Flex-Tune 100 · Humanize 0 · Transpose −12 · Formant on · Throat 120 | An octave down with a longer throat, so the voice gets darker and bigger (Q18). It shifts without re-tuning (D20) |
| 3 | Pro-C | Clean style · Ratio 8:1 · Attack 2 ms · Release 60 ms · Knee 6 dB · Threshold about −20 dB, for 8–10 dB GR · Gain to bring it back up | Feeds the distortion a steady level, so the grit doesn't come and go |
| 4 | Saturn 2 | 1 band · Warm Tube · Drive 60% · Mix 100% · Tone: Presence −3 dB · HQ on · Level to match | Heavy, dark grit. A tube style keeps it from sounding like a guitar amp, which is Rockstar Grit's color |
| 5 | Pro-Q | Low Cut 150 Hz, 24 dB/oct · High Cut 3 kHz, 24 dB/oct · Zero Latency | Keeps the twin under the lead's presence and out of the beat's sub |
| 6 | Pro-L 2 | Aggressive style · Output −6.0 dBFS · Gain about +8 dB, adjusted for 2–3 dB GR · Lookahead 0 ms | A ceiling, so the twin can never poke out on a loud word (Q17). Aggressive suits a distorted source and works without lookahead |

**Level:** fader at −15 dB. Adjust until it passes the ghost test (foundation §4): 12–18 dB under LEAD. Mono (D7).

**Buildable:** yes. Transpose −12 is Auto-Tune's limit. Formant and Throat need the Modern algorithm (D16), and Throat 120 sits inside the 80–140 range the sheets allow (foundation §1).

## FX returns

### FX · DELAY (the angel's delay)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Timeless 3 | Sync on · Left 1/4, Right dotted 1/8 · Ping Pong off · Feedback 25% · Filters: High Pass 300 Hz, Low Pass 9 kHz · Stretch mode · Dry off · Wet 0 dB · envelope follower → Wet level, about −9 dB of range · EF attack short, release about 250 ms | Phase 1's bright delay. The two times give it stereo movement, and it ducks softly so the angel stays clean (D15) |
| 2 | Pro-Q | Low Cut 300 Hz, 12 dB/oct · Low Cut 500 Hz on Side only · Zero Latency | Clean repeats with mono lows (D7) |

**Level:** fader at −18 dB.

### FX · VERB (the demon's room)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Default style · Space 1.0 s · Decay Rate 100% · Predelay 10 ms · Brightness −40% · Character 20% · Distance 50% · Thickness 30% · Stereo Width 50% · Mix 100% · Ducking off | The demon's own darker, narrower room: Phase 1's "two rooms" |
| 2 | Pro-Q | Low Cut 200 Hz, 24 dB/oct · High Cut 4 kHz, 12 dB/oct · Zero Latency | Keeps the room dark and out of the low end |

**Level:** fader at −6 dB, which puts the room about 6 dB under the demon.

## Buses

| Track | Slot | Plugin | Settings | Why |
|---|---|---|---|---|
| VOX BUS | 1 | Pro-C | Bus style · Ratio 2:1 · Attack 30 ms · Release Auto · Knee 12 dB · Threshold about −10 dB, for 1–2 dB GR · Gain to level-match | The angel, the demon and the doubles read as one performance |

VOX GROUP stays empty.

## DBL

**DBL IN L / DBL IN R:** the VOX IN chain exactly (same three slots, same settings), faders at 0 dB, panned L70 / R70.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 120 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · Zero Latency | The lead carries the body |
| 2 | Pro-C | Clean style · Ratio 6:1 · Attack 1 ms · Release 60 ms · Knee 6 dB · Threshold about −18 dB, for 6–8 dB GR · Gain to level-match | Tighter than the lead, so the doubles blend |
| 3 | Saturn 2 | 1 band · Clean Tube · Drive 15% · Mix 20% · HQ on · Level to match | Matches the lead's density |
| 4 | Fresh Air | Mid Air 10% · High Air 25% · Trim to level-match | Bright, but a step behind |
| 5 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB · Range 10 dB · detection 5–11 kHz | S's stack up across takes |
| 6 | Pro-Q | Bell 4 kHz, Q 1.0, −2 dB · High Shelf 10 kHz, −2 dB | Tone offset that keeps the lead in front |
| 7 | Pro-L 2 | Allround style · Output −3.0 dBFS · Gain about +10 dB, for 1–2 dB GR · Lookahead 2 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · DELAY at 100%, which lands 6–10 dB below LEAD's because sends are post-fader.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Demon surge | PAR · DEMON › fader | −15 dB → −9 dB → −15 dB | Punchlines and key words, with 1/16-note ramps | Phase 1's signature: the twin steps forward for a moment |
| 2 | Delay throw | FX · DELAY › fader | −18 dB → −8 dB → −18 dB | Last word of hook lines: up on the word, back down after two repeats | Lifts the angel's line endings. LEAD's send is already at 100%, so the throw rides the return instead (D22) |

## Ear checks

Added in Step 5.

## Translation notes

- **Mono:** the lead and the demon are mono by design. Only the doubles and the delay carry width, so those two get the mono check.
- **Small speakers:** most of the demon's weight sits below 300 Hz and fades on phones. Its distortion harmonics up to 3 kHz keep a trace of it there, which is intended.
- **Loud playback:** the demon is high-passed at 150 Hz, so it never fights the 808.
