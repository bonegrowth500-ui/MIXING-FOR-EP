# 11 · Silk Stack

Lush, wide and choir-like: the lead blooms into harmonies made from itself, with warm mids and a silky top.

**Status:** dialed in (Step 3). Stress-tested in Step 4.
**Placement:** balanced (D6) · **Tune:** Medium · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. PAR · OCT stays on Chromatic (D20), and Pitcher follows the 3rd line instead of a key.
3. **The 3rd line:** see [Making the 3rd line](#making-the-3rd-line-per-song).
4. **Key moves:** place the harmony rides and the hall swells (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Warm and silky. Low cut at 75 Hz, body +2–3 dB near 200–250 Hz, presence eased about 1 dB around 3–4 kHz, gentle air |
| Density | 8–10 dB total: the smoothest of the five, led by opto compression |
| Grit | Warm tube, with no audible dirt |
| Space | A lush long hall of about 3 s with 70 ms of pre-delay and light ducking. The harmonies sit further back in it than the lead. Wet 4/5 |
| Width | The widest of the five. Lead mono and solid, harmonies chorused wide, doubles at L/R 80, hall fully wide |
| Placement | Balanced: clear, but embedded in the harmonies and the hall |
| Tune | Medium: retune 25–40, humanize and Flex-Tune 20–30 |
| Harmonies | 3rd up at 8–10 dB under the lead, octave down at 10–12 dB under. Sung lines only |

## Upgrades (Q27)

- **Harmonies fed from the finished lead.** They inherit its warmth, compression and de-essing, so all three voices blend like one.
- **Octave kept out of the sub.** The octave-down voice is high-passed, so it adds low-mid weight (right where a thin voice needs it) without muddying the beat.
- **Ducked hall.** Light ducking on top of the pre-delay keeps the words upfront in a sound this wet.
- **Harmonies skip the raps.** The 3rd's MIDI line leaves rap sections empty, and both harmonies ride out there (key move). A harmony stack on rap bars sounds like a mistake.

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD | — | 0 dB |
| LEAD | VOX IN | VOX BUS, and PAR · OCT and PAR · 3RD at 100% | FX · HALL 50% | 0 dB |
| PAR · OCT | LEAD | VOX BUS | FX · HALL 100% | −8 dB |
| PAR · 3RD | LEAD, with its pitch set by the 3RD LINE channel | VOX BUS | FX · HALL 100% | −6 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L80 / R80 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · HALL 50% | −8 dB |
| FX · HALL | Sends | VOX GROUP | — | −10 dB |
| VOX BUS | LEAD, PAR · OCT, PAR · 3RD, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX · HALL | Master | — | Set against the beat, with peaks at or below −6 dBFS |

LEAD and DBL send to the hall at 50% while the harmonies send at 100%, so the harmonies sit further back.

Plus one Channel Rack channel, **3RD LINE**: a MIDI Out channel that holds the 3rd line and drives Pitcher.

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct · Zero Latency | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −45 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | Breaths would be copied into both harmonies. Taking them down here fixes all three voices at once |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 30 · Humanize 25 · Flex-Tune 25 · Natural Vibrato 0 · Formant off · Classic Mode off | Smooth correction that keeps slides silky. The harmonies inherit it |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 75 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · Zero Latency | Keeps the natural weight a lush sound needs |
| 2 | Pro-C | Vocal style · Ratio 3:1 · Attack 5 ms · Release 80 ms · Knee 12 dB · Threshold about −15 dB, for 3–4 dB GR · Gain to level-match | A slower, gentler grab: silk, not snap |
| 3 | Pro-Q | Bell 220 Hz, Q 0.7, +2.5 dB | Phase 1's rich warm mids start here |
| 4 | Saturn 2 | 1 band · Warm Tube · Drive 25% · Mix 40% · HQ on · Level to match | Phase 1's warmth and density. The harmonies share it because they're fed from here |
| 5 | Pro-C | Opto style · Ratio 2:1 · Attack 15 ms · Release Auto · Knee 24 dB · Threshold about −20 dB, for 2–3 dB GR · Gain to level-match | Phase 1's opto leveling, for a silky, even line |
| 6 | Fresh Air | Mid Air 10% · High Air 25% · Trim to level-match | A touch of top without edge |
| 7 | Pro-DS | Single Vocal · Split Band · Threshold −28 dB, for 3–5 dB on S's · Range 8 dB · detection 5–11 kHz · Lookahead 10 ms | Every S here gets copied into two harmonies, so it's caught before the split. The longer lookahead keeps it smooth |
| 8 | Pro-Q | Bell 3.5 kHz, Q 1.2, dynamic −3 dB | Belted notes stay smooth |
| 9 | Pro-Q | Tilt Shelf 1 kHz, −1.5 dB | A warm tilt that eases presence about 1 dB around 3–4 kHz: clear but embedded |
| 10 | Pro-L 2 | Transparent style · Gain about +10 dB, adjusted until the loudest lines show 1–2 dB GR · Output −3.0 dBFS · Lookahead 3 ms | Protects the harmony feed and the hall from spikes |

**Density check:** about 3.5 + 1.5 + 2.5 + 1.5 dB, roughly 9 dB total (target 8–10).

**Order notes:** LEAD is also the source for both harmonies, so every stage here shapes three voices. That's why de-essing and peak control come before the split.

## Parallel tracks

**The harmony engine.** Both harmony tracks are fed from LEAD, with the routes at 100%, so they come from the finished lead and share its tone.

### PAR · OCT (octave down)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Auto-Tune Artist | Alto/Tenor · Chromatic · Retune Speed 50 · Flex-Tune 100 · Humanize 0 · Transpose −12 · Formant on · Throat 100 | A natural lower voice rather than a monster, the opposite of Phantom Twin's demon. It shifts without re-tuning (D20) |
| 2 | Pro-Q | Low Cut 120 Hz, 18 dB/oct · High Shelf 6 kHz, −3 dB · Zero Latency | Low-mid weight without sub mud, softer on top |
| 3 | Pro-C | Vocal style · Ratio 3:1 · Attack 10 ms · Release 100 ms · Knee 12 dB · Threshold about −10 dB, for 3–4 dB GR · Gain to level-match | Support layers stay put |
| 4 | Vintage Chorus | Mode I · Mix 50% · H Pass 250 Hz | Phase 1: wide chorus on the harmonies only. H Pass keeps the chorus off the low end, which keeps the lows clean and mono-safe |

**Level:** fader at −8 dB. The 120 Hz high-pass trims about 3 dB first, so that lands about 11 dB under LEAD (target 10–12).

### PAR · 3RD (3rd up)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pitcher | MIDI mode · Speed fully up · formant control on, nudged slightly toward the male side · low-frequency setting 80 Hz · MIDI input port matching 3RD LINE | Moves the lead to its in-key 3rd, note by note. The formant nudge offsets the upward shift, so the harmony doesn't sound smaller than you |
| 2 | Pro-Q | Low Cut 200 Hz, 18 dB/oct · Bell 3.5 kHz, Q 1.0, −2 dB · Zero Latency | Sits behind the lead |
| 3 | Pro-C | Vocal style · Ratio 3:1 · Attack 10 ms · Release 100 ms · Knee 12 dB · Threshold about −10 dB, for 3–4 dB GR · Gain to level-match | Support layers stay put |
| 4 | Vintage Chorus | Mode II · Mix 50% · H Pass 250 Hz | A different mode from PAR · OCT, so the two harmonies spread instead of stacking |

**Level:** fader at −6 dB. The 200 Hz high-pass trims about 3 dB first, so that lands about 9 dB under LEAD (target 8–10).

### Making the 3rd line (per song)

1. Add a MIDI Out channel named 3RD LINE. Set its port and Pitcher's MIDI input port to the same number (port 10, for example).
2. Open the lead vocal in NewTone and send its notes to 3RD LINE as a MIDI score.
3. In the piano roll, select all notes and move them up 4 semitones. With the song's scale highlighted, move any note that lands outside the key down 1 semitone. That leaves a true in-key 3rd above every note. Then run Tools › Quick legato, so each note runs into the next with no gaps inside a phrase.
4. Delete the notes on rap sections.

**Fallback:** duplicate the lead's clips, open them in NewTone, raise each note to its in-key 3rd, and point that clip channel at PAR · 3RD. Remove LEAD's route to PAR · 3RD. That audio skips LEAD's processing, so the slots change to:
1. Pro-Q: Low Cut 200 Hz, 18 dB/oct · Bell 3.5 kHz, −2 dB
2. Pro-C: Vocal · Ratio 4:1 · about 6 dB GR
3. Saturn 2: Warm Tube · Drive 25% · Mix 40%
4. Pro-DS: Single Vocal · Threshold −30 dB · Range 8 dB
5. Vintage Chorus: Mode II

**Buildable:** yes. Pitcher's MIDI mode takes its pitch from the MIDI Out notes, NewTone exports notes as a MIDI score, and Vintage Chorus and Auto-Tune's transpose are confirmed (foundation §1). The "up 4, then pull out-of-key notes down 1" rule gives exact 3rds in major and natural minor keys.

## FX returns

### FX · HALL

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Default style · Space 3.0 s · Decay Rate 100% · Predelay 70 ms · Brightness −10% · Character 30% · Distance 40% · Thickness 20% · Stereo Width 100% · Mix 100% · Ducking about 4 dB | Phase 1's lush hall. Pre-delay and light ducking keep the words upfront (D15) |
| 2 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Low Cut 400 Hz on Side only · High Shelf 9 kHz, −3 dB · Zero Latency | A silky, clean tail with mono lows. Vampire Haze gets the dirty one |

**Level:** fader at −10 dB.

## Buses

| Track | Slot | Plugin | Settings | Why |
|---|---|---|---|---|
| VOX BUS | 1 | Pro-C | Opto style · Ratio 2:1 · Attack 30 ms · Release Auto · Knee 18 dB · Threshold about −10 dB, for 1–2 dB GR · Gain to level-match | The lead, both harmonies and the doubles sing as one choir |

VOX GROUP stays empty.

## DBL

**DBL IN L / DBL IN R:** the VOX IN chain exactly (same three slots, same settings), faders at 0 dB, panned L80 / R80.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 120 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · Zero Latency | The lead and the octave carry the low mids |
| 2 | Pro-C | Opto style · Ratio 4:1 · Attack 10 ms · Release Auto · Knee 18 dB · Threshold about −20 dB, for 5–6 dB GR · Gain to level-match | Tighter than the lead, so the doubles blend |
| 3 | Saturn 2 | 1 band · Warm Tube · Drive 25% · Mix 40% · HQ on · Level to match | Matches the lead's warmth |
| 4 | Pro-DS | Single Vocal · Split Band · Threshold −30 dB · Range 10 dB · detection 5–11 kHz | S's stack across takes and harmonies |
| 5 | Pro-Q | Bell 3.5 kHz, Q 1.0, −2 dB · High Shelf 10 kHz, −2 dB | Warmer and less present than the lead, so the lead stays in front |
| 6 | Pro-L 2 | Transparent style · Output −3.0 dBFS · Gain about +10 dB, for 1–2 dB GR · Lookahead 3 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · HALL at 50%, like LEAD's.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Harmony ride | PAR · OCT and PAR · 3RD › faders | −8 dB and −6 dB → off (−∞), then back | Off for rap sections, back for sung lines, with 1-beat ramps | Keeps the stack on the melodies. The 3RD line is already empty there, so this also covers anything Pitcher passes through without notes |
| 2 | Hall swell | LEAD › send to FX · HALL | 50% → 100% → 50% | Last line of each hook | The hook exhales into the hall |

## Ear checks

Added in Step 5.

## Translation notes

- **Mono:** this preset's biggest risk, because it's the widest. Chorus and hall narrow in mono, and the harmonies still have to be heard. Step 4 checks it.
- **Small speakers:** the warmth below 300 Hz fades on phones. Presence is only eased by about 1 dB, so the words still read.
- **Loud playback:** the octave's high-pass keeps it clear of the 808.
