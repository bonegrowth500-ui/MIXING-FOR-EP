# 11 · Silk Stack

Lush, wide and choir-like: the lead blooms into harmonies made from itself, with warm mids and a silky top.

**Status:** blueprint (Step 2). Settings get dialed in during Step 3.
**Placement:** balanced (D6) · **Tune:** Medium · **Builds on:** [foundation](00-foundation.md)

## Sound targets

| Target | Value |
|---|---|
| Tone | Warm and silky. Low cut at 75 Hz, body +2–3 dB near 200–250 Hz, presence eased about 1 dB around 3–4 kHz, gentle air |
| Density | 8–10 dB total: the smoothest of the five, led by opto compression |
| Grit | Warm tube, with no audible dirt |
| Space | A lush long hall of about 3 s with ~70 ms of pre-delay and light ducking. The harmonies sit further back in it than the lead. Wet 4/5 |
| Width | The widest of the five. Lead mono and solid, harmonies chorused wide, doubles at L/R 80, hall fully wide |
| Placement | Balanced: clear, but embedded in the harmonies and the hall |
| Tune | Medium: retune 25–40, humanize and Flex-Tune 20–30 |
| Harmonies | 3rd up at 8–10 dB under the lead, octave down at 10–12 dB under. Sung lines only |

## Upgrades (Q27)

- **Harmonies fed from the finished lead.** They inherit its warmth, compression and de-essing, so all three voices blend like one.
- **Octave kept out of the sub.** The octave-down voice is high-passed, so it adds low-mid weight (right where a thin voice needs it) without muddying the beat.
- **Ducked hall.** Light ducking on top of the pre-delay keeps the words upfront in a sound this wet.
- **Harmonies skip the raps.** The 3rd's MIDI line leaves rap sections empty, and the octave rides down there (key move). A harmony stack on rap bars sounds like a mistake.

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. PAR · OCT stays on Chromatic (D20), and Pitcher follows the 3rd line instead of a key.
3. **The 3rd line:** see [Making the 3rd line](#making-the-3rd-line-per-song).
4. **Key moves:** place the harmony rides and the hall swells.

## Track map

| Track | Gets audio from | Routes to | Sends |
|---|---|---|---|
| VOX IN | Lead clips | LEAD | — |
| LEAD | VOX IN | VOX BUS, PAR · OCT, PAR · 3RD | FX · HALL |
| PAR · OCT | LEAD | VOX BUS | FX · HALL, more than LEAD's |
| PAR · 3RD | LEAD, with its pitch set by the 3RD LINE channel | VOX BUS | FX · HALL, more than LEAD's |
| DBL IN L / R | Left / right double clips | DBL, panned L80 / R80 | — |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · HALL, 6 dB below LEAD's send |
| FX · HALL | Sends | VOX GROUP | — |
| VOX BUS | LEAD, PAR · OCT, PAR · 3RD, DBL | VOX GROUP | — |
| VOX GROUP | VOX BUS, FX · HALL | Master | — |

Plus one Channel Rack channel, **3RD LINE**: a MIDI Out channel that holds the 3rd line and drives Pitcher.

## VOX IN

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Rumble cut | Foundation standard |
| 2 | Pro-G | Gentle expander | Breaths would be copied into both harmonies. Taking them down here fixes all three voices at once |
| 3 | Auto-Tune Artist | Medium tune in the song's key | Smooth correction that keeps slides silky. The harmonies inherit it |

## LEAD

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Corrective: low cut at 75 Hz, box | Keeps the natural weight a lush sound needs |
| 2 | Pro-C | Compressor 1: gentle peak catcher | A slower grab: silk, not snap |
| 3 | Pro-Q | Tone: warm body | Phase 1's rich warm mids start here |
| 4 | Saturn 2 | Warm tube | Phase 1's warmth and density. The harmonies share it because they're fed from here |
| 5 | Pro-C | Compressor 2: smooth opto | Phase 1's opto leveling, for a silky, even line |
| 6 | Fresh Air | Silky air, kept low | A touch of top without edge |
| 7 | Pro-DS | Smooth de-essing | Every S here gets copied into two harmonies, so it's caught before the split |
| 8 | Pro-Q | Dynamic control, 2.5–5 kHz | Belted notes stay smooth |
| 9 | Pro-Q | Polish: warm tilt, slight presence ease | Balanced placement: clear but embedded |
| 10 | Pro-L 2 | Gentle peak control | Protects the harmony feed and the hall from spikes |

**Order notes:** LEAD is also the source for both harmonies, so every stage here shapes three voices. That's why de-essing and peak control come before the split.

## Parallel tracks

**The harmony engine.** Both harmony tracks are fed from LEAD, so they come from the finished lead and share its tone.

### PAR · OCT (octave down)

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Auto-Tune Artist | Transpose −12, Formant on, Throat 100, Chromatic, minimal correction | A natural lower voice rather than a monster, the opposite of Phantom Twin's demon. Always in key (D20) |
| 2 | Pro-Q | High-pass ~120 Hz, softer top, Zero Latency | Low-mid weight without sub mud |
| 3 | Pro-C | Steady level | Support layers stay put |
| 4 | Vintage Chorus | Wide | Phase 1: wide chorus on the harmonies only |

**Level:** 10–12 dB under LEAD.

### PAR · 3RD (3rd up)

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pitcher | MIDI mode, following the 3RD LINE channel | Moves the lead to its in-key 3rd, note by note |
| 2 | Pro-Q | High-pass ~200 Hz, softened presence, Zero Latency | Sits behind the lead |
| 3 | Pro-C | Steady level | Support layers stay put |
| 4 | Vintage Chorus | Wide, a different mode from PAR · OCT | Decorrelates the two harmonies so they spread instead of stacking |

**Level:** 8–10 dB under LEAD.

### Making the 3rd line (per song)

1. Add a MIDI Out channel named 3RD LINE, and set its port to match Pitcher's MIDI input port.
2. Open the lead vocal in NewTone and send its notes to 3RD LINE as a MIDI score.
3. In the piano roll, select all notes and move them up 4 semitones. With the song's scale highlighted, move any note that lands outside the key down 1 semitone. That leaves a true in-key 3rd above every note.
4. Delete the notes on rap sections.

**Fallback:** duplicate the lead's clips, open them in NewTone, raise each note to its in-key 3rd, and route that audio into PAR · 3RD in place of Pitcher. That audio skips LEAD's processing, so Step 3 adds the slots it needs.

**Buildable:** yes. Pitcher's MIDI mode takes its pitch from the MIDI Out notes, NewTone exports notes as a MIDI score, and Vintage Chorus and Auto-Tune's transpose are confirmed (foundation §1). The "up 4, then pull out-of-key notes down 1" rule gives exact 3rds in major and natural minor keys.

## FX returns

### FX · HALL

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Lush long hall, about 3 s, ~70 ms pre-delay, light Ducking, full width | Phase 1's lush hall. Ducking and pre-delay keep the words upfront (D15) |
| 2 | Pro-Q | Low cut ~250 Hz, softened above ~9 kHz, lows kept mono | A silky, clean tail. Vampire Haze gets the dirty one |

## Buses

- **VOX BUS:** one slot. Pro-C, Opto style, 1–2 dB of glue, so the lead, both harmonies and the doubles sing as one choir.
- **VOX GROUP:** empty.

## DBL

**DBL IN L / DBL IN R:** the foundation front end (rumble cut, gentle expander, Auto-Tune matching VOX IN), panned L80 / R80.

| Slot | Plugin | Job | Why |
|---|---|---|---|
| 1 | Pro-Q | Low cut ~120 Hz, box | The lead and the octave carry the low mids |
| 2 | Pro-C | Tighter opto compression | Steady doubles blend better |
| 3 | Saturn 2 | Warm tube | Matches the lead's warmth |
| 4 | Pro-DS | Harder de-essing | S's stack across takes and harmonies |
| 5 | Pro-Q | Tone offset: warm, less presence | Keeps the lead in front |

**Level:** 6–10 dB under LEAD. **Send:** FX · HALL, 6 dB below LEAD's send.

## Key moves

| # | Move | Track › Parameter | When | Why |
|---|---|---|---|---|
| 1 | Harmony ride | PAR · OCT › fader (PAR · 3RD follows its MIDI line) | Up on sung lines, down on raps | Keeps the stack on the melodies |
| 2 | Hall swell | LEAD › send to FX · HALL | Last line of each hook | The hook exhales into the hall |

From/to values are set in Step 3.

## Ear checks

Added in Step 5.

## Translation notes

- **Mono:** this preset's biggest risk, because it's the widest. Chorus and hall narrow in mono, and the harmonies still have to be heard. Step 4 checks it.
- **Small speakers:** the warmth below 300 Hz fades on phones. Presence is only eased by about 1 dB, so the words still read.
- **Loud playback:** the octave's high-pass keeps it clear of the 808.
