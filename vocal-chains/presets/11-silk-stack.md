# 11 · Silk Stack

Lush, wide and choir-like: the lead blooms into harmonies made from itself, with warm mids and a silky top.

**Status:** final. Dialed in (Step 3), stress-tested (Step 4) and cold-read (Step 5).
**Placement:** balanced (D6) · **Tune:** Medium · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. PAR · OCT stays on Chromatic (D20), and Pitcher follows the 3rd line instead of a key.
3. **The 3rd line:** once VOX IN's Auto-Tune is set, see [Making the 3rd line](#making-the-3rd-line-per-song).
4. **Key moves:** after the blend (foundation §4), place the harmony rides and the hall swells (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Warm and silky. Low cut at 75 Hz, body +2–3 dB near 200–250 Hz, presence eased about 1 dB around 3–4 kHz, gentle air |
| Density | 8–10 dB total: the smoothest of the five, led by opto compression |
| Grit | Warm tube, with no audible dirt |
| Space | A lush long hall of about 3 s with 70 ms of pre-delay and light ducking. The harmonies sit further back in it than the lead. Wet 4/5 |
| Width | The widest of the five. Lead mono and solid, harmonies chorused wide and panned apart (3rd L35, octave R35), doubles at L/R 80, hall at full stereo |
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
| PAR · OCT | LEAD | VOX BUS | FX · HALL 100% | −8 dB, panned R35 |
| PAR · 3RD | LEAD, with its pitch set by the 3RD LINE channel | VOX BUS | FX · HALL 100% | −6 dB, panned L35 |
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
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −35 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | Breaths would be copied into both harmonies. Taking them down here fixes all three voices at once. The threshold sits just above typical breaths, so they dip by up to 6 dB while words don't. Lower it if word tails get clipped |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 30 · Humanize 25 · Flex-Tune 25 · Natural Vibrato 0 · Formant off · Classic Mode off | Smooth correction that keeps slides silky. The harmonies inherit it |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 75 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · optional: a narrow dynamic cut on any ringing resonance | Keeps the natural weight a lush sound needs |
| 2 | Pro-C | Vocal style · Ratio 3:1 · Attack 5 ms · Release 80 ms · Knee 12 dB · Threshold about −15 dB, for 3–4 dB GR · Gain to level-match | A slower, gentler grab: silk, not snap |
| 3 | Pro-Q | Bell 220 Hz, Q 0.7, +2.5 dB | Phase 1's rich warm mids start here |
| 4 | Saturn 2 | 1 band · Warm Tube · Drive 25% · Mix 40% · HQ on · Level to match | Phase 1's warmth and density. The harmonies share it because they're fed from here |
| 5 | Pro-C | Opto style · Ratio 2:1 · Attack 15 ms · Release Auto · Knee 24 dB · Threshold about −20 dB, for 2–3 dB GR · Gain to level-match | Phase 1's opto leveling, for a silky, even line |
| 6 | Fresh Air | Mid Air 10% · High Air 25% · Trim to level-match | A touch of top without edge |
| 7 | Pro-DS | Single Vocal · Split Band · Threshold −28 dB, for 3–5 dB on S's · Range 8 dB · detection 5–11 kHz · Lookahead 10 ms | Every S here gets copied into two harmonies, so it's caught before the split. The longer lookahead keeps it smooth |
| 8 | Pro-Q | Bell 3.5 kHz, Q 1.2, dynamic −3 dB | Belted notes stay smooth |
| 9 | Pro-Q | Tilt Shelf 1 kHz, −1.5 dB | A warm tilt that eases presence about 1 dB around 3–4 kHz: clear but embedded |
| 10 | Pro-L 2 | Transparent style · Gain about +10 dB, adjusted until the loudest lines show 1–2 dB GR · Output −3.0 dBFS · Lookahead 3 ms | Protects the harmony feed and the hall from spikes |

**Density check** (slots 2 + 4 + 5 + 10, on the loudest lines): about 3.5 + 1.5 + 2.5 + 1.5 dB, roughly 9 dB total (target 8–10).

**Order notes:** LEAD is also the source for both harmonies, so every stage here shapes three voices. That's why de-essing and peak control come before the split.

## Parallel tracks

**The harmony engine.** Both harmony tracks are fed from LEAD, with the routes at 100%, so they come from the finished lead and share its tone.

### PAR · OCT (octave down)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Auto-Tune Artist | Alto/Tenor · Chromatic · Retune Speed 50 · Humanize 0 · Flex-Tune 100 · Natural Vibrato 0 · Transpose −12 · Formant on · Throat 100 · Classic Mode off | A natural lower voice rather than a monster, the opposite of Phantom Twin's demon. It shifts without re-tuning (D20) |
| 2 | Pro-Q | Low Cut 120 Hz, 18 dB/oct · High Shelf 6 kHz, −3 dB · Output 0 dB | Low-mid weight without sub mud, softer on top |
| 3 | Pro-C | Vocal style · Ratio 3:1 · Attack 10 ms · Release 100 ms · Knee 12 dB · Threshold about −10 dB, for 3–4 dB GR · Gain to level-match | Support layers stay put |
| 4 | Vintage Chorus | Mode I · Mix 50% · H Pass 250 Hz | Phase 1: wide chorus on the harmonies only. H Pass keeps the chorus off the low end, which keeps the lows clean and mono-safe |

**Level:** fader at −8 dB. The 120 Hz high-pass trims about 3 dB first, so that lands about 11 dB under LEAD (target 10–12). Panned R35, opposite the 3rd, so the two harmonies spread around the lead instead of stacking on it.

### PAR · 3RD (3rd up)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pitcher | MIDI on, in Octaves mode · Port (bottom left) matching 3RD LINE · Speed about halfway · Formant on · Gender nudged slightly toward male · low-frequency setting 80 Hz | Moves the lead to the exact note in the 3rd line, octave included. Plain MIDI mode keeps only the note name, so a 3rd that crosses into the next octave could land a 6th below. Halfway speed glides between notes the way Medium tuning does, where fully up jumps in steps. Gender toward male offsets the upward shift, so the harmony doesn't sound smaller than you |
| 2 | Pro-Q | Low Cut 200 Hz, 18 dB/oct · Bell 3.5 kHz, Q 1.0, −2 dB · Output 0 dB | Sits behind the lead |
| 3 | Pro-C | Vocal style · Ratio 3:1 · Attack 10 ms · Release 100 ms · Knee 12 dB · Threshold about −10 dB, for 3–4 dB GR · Gain to level-match | Support layers stay put |
| 4 | Vintage Chorus | Mode II · Mix 50% · H Pass 250 Hz | A different mode from PAR · OCT, so the two harmonies spread instead of stacking |

**Level:** fader at −6 dB. The 200 Hz high-pass trims about 3 dB first, so that lands about 9 dB under LEAD (target 8–10). Panned L35.

### Making the 3rd line (per song)

1. Add a MIDI Out channel named 3RD LINE. On PAR · 3RD's Pitcher, turn MIDI on and set the Port display (bottom left) to the same number as MIDI Out's port (port 10, for example).
2. Render the tuned lead as a stem that starts at bar 1. First clear any Playlist time selection (your 8-bar loop), because a selection renders only that range. Then File › Export › WAV file, check that it renders the full song, tick **Split mixer tracks**, and keep the VOX IN file. Its notes are the ones Auto-Tune actually sang, and its timing lines up with the song.
3. Load the stem into NewTone. In the Channel Rack, select 3RD LINE and pick an empty pattern, then send NewTone's notes to the piano roll as a score. Place that pattern in the Playlist at bar 1.
4. In the piano roll, delete detection blips (anything shorter than about a 1/16 note) and fix any note that doesn't match what you hear. The harmony copies every mistake left here.
5. Select all notes and move them up 4 semitones. With the song's scale highlighted (the piano roll's scale helper), move any note that lands outside the key down 1 semitone. That leaves a true in-key 3rd above every note. Run Tools › Quick legato, so each note runs into the next with no gaps inside a phrase. Then, with snap off (hold Alt while dragging), move all notes about 10–20 ms earlier, so Pitcher catches the start of each note.
6. Delete the notes on rap sections, and trim any sung note that Quick legato stretched into a rap.

If the lead's takes change later, render a new stem and redo the line.

**Fallback** (if Pitcher tracks your voice poorly): load the same VOX IN stem into NewTone, raise each note to its in-key 3rd (the step 5 rule), export the result and drop it on the Playlist at bar 1. It lands on its own channel. Point that channel at PAR · 3RD and remove LEAD's route to PAR · 3RD. The stem already carries VOX IN's tuning and expander, but it skips LEAD, so the slots change to:
1. Pro-Q: Low Cut 200 Hz, 18 dB/oct · Bell 3.5 kHz, Q 1.0, −2 dB · Output 0 dB
2. Pro-C: Vocal style · Ratio 4:1 · Attack 10 ms · Release 100 ms · Knee 12 dB · Threshold for about 6 dB GR · Gain to level-match
3. Saturn 2: as LEAD slot 4
4. Pro-DS: as LEAD slot 7, but Threshold −30 dB
5. Pro-L 2: Transparent style · Gain for 1–2 dB GR (roughly +13 dB here) · Output −3.0 dBFS · Lookahead 3 ms
6. Vintage Chorus: Mode II · Mix 50% · H Pass 250 Hz

Here Pro-L 2 comes after the EQ, so it wins back the EQ's 3 dB trim. Start the fader at −9 dB instead of −6, and run key move 1 from −9 dB.

**Buildable:** yes. With MIDI on in Octaves mode, Pitcher takes each note and its octave from the MIDI Out notes. NewTone exports notes as a score, and Vintage Chorus and Auto-Tune's transpose are confirmed (foundation §1). The "up 4, then pull out-of-key notes down 1" rule gives exact 3rds in major and natural minor keys. Harmonic minor has one exception: the raised 7th's 3rd comes out 1 semitone high, so move it down (in A minor, G♯ takes B, not C).

## FX returns

### FX · HALL

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Modern style · Space 3.0 s · Decay Rate 100% · Predelay 70 ms · Brightness −10% · Character 30% · Distance 40% · Thickness 20% · Stereo Width 50% · Mix 100% · Ducking about 4 dB | Phase 1's lush hall. Pre-delay and light ducking keep the words upfront (D15). 50% is full stereo |
| 2 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Low Cut 400 Hz, 12 dB/oct, on Side only · High Shelf 9 kHz, −3 dB · Output 0 dB | A silky, clean tail with mono lows. Vampire Haze gets the dirty one |

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
| 1 | Pro-Q | Low Cut 120 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB | The lead and the octave carry the low mids |
| 2 | Pro-C | Opto style · Ratio 4:1 · Attack 10 ms · Release Auto · Knee 18 dB · Threshold about −20 dB, for 5–6 dB GR · Gain to level-match | Tighter than the lead, so the doubles blend |
| 3 | Saturn 2 | 1 band · Warm Tube · Drive 25% · Mix 40% · HQ on · Level to match | Matches the lead's warmth |
| 4 | Pro-DS | Single Vocal · Split Band · Threshold −30 dB, for 5–8 dB on S's · Range 10 dB · detection 5–11 kHz · Lookahead 10 ms | S's stack across takes and harmonies |
| 5 | Pro-Q | Bell 3.5 kHz, Q 1.0, −2 dB · High Shelf 10 kHz, −2 dB | Warmer and less present than the lead, so the lead stays in front |
| 6 | Pro-L 2 | Transparent style · Gain about +10 dB, for 1–2 dB GR · Output −3.0 dBFS · Lookahead 3 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · HALL at 50%, like LEAD's. Sends are post-fader, so it lands 6–10 dB below LEAD's.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Harmony ride | PAR · OCT and PAR · 3RD › faders | −8 dB and −6 dB → off (−∞), then back | Off for rap sections, back for sung lines. Put each 1-beat ramp in the gap between sections, so the faders reach −∞ before the first rap word and are back by the first sung word | Keeps the stack on the melodies. The 3RD line is already empty there, so this also covers anything Pitcher passes through without notes |
| 2 | Hall swell | LEAD › send to FX · HALL | 50% → 100% → 50% | Last line of each hook: a 1-beat ramp up into the line, back to 50% right after its last word | The hook exhales into the hall |

## Ear checks

Build in this order, one stage at a time (foundation §5.7).

| # | Stage | You should hear |
|---|---|---|
| 1 | Template and input (foundation §2, §4, §5.7) | The loudest lines peak around −10 dBFS on VOX IN. With the unbuilt tracks muted, mute LEAD for a moment and the vocal should go silent. If it keeps playing, VOX IN still routes to Master |
| 2 | VOX IN 1–3 | Notes land in tune, but slides stay smooth and silky. Breaths dip a little, words don't |
| 3 | LEAD 1 · Pro-Q | Box eases on close words, and the natural weight stays |
| 4 | LEAD 2 · Pro-C | A gentle hold on peaks. Still soft, no snap |
| 5 | LEAD 3 · Pro-Q | Rich, warm mids: fuller and rounder |
| 6 | LEAD 4 · Saturn 2 | Warmer and denser, with no audible dirt |
| 7 | LEAD 5 · Pro-C | A silky, even line |
| 8 | LEAD 6 · Fresh Air | A touch of top without edge |
| 9 | LEAD 7 · Pro-DS | S's soften smoothly, with no lisp |
| 10 | LEAD 8 · Pro-Q | Belted notes stay smooth |
| 11 | LEAD 9 · Pro-Q | A little warmer and more embedded, with the words still clear |
| 12 | LEAD 10 · Pro-L 2 | The lead comes up about 10 dB, with no audible limiting. If Master clips, pull VOX GROUP down for now. The blend sets it properly |
| 13 | PAR · OCT 1, fader at 0 dB for the check | A natural lower voice an octave down, not a monster |
| 14 | PAR · OCT 2–4 | Low-mid weight with no sub mud, soft on top and steady, spreading wide to the right |
| 15 | PAR · 3RD 1: load Pitcher, make the 3rd line (see Making the 3rd line), fader at 0 dB for the check | An in-key 3rd above every sung note, gliding between notes like the lead. A wrong note means the 3RD LINE needs a fix |
| 16 | PAR · 3RD 2–4 | It sits behind the lead, steady, spreading wide to the left |
| 17 | Both harmonies, back at −8 / −6 dB | On the sung bars, the stack adds size and color without pulling focus, and the lead stays clear (the support test). The harmonies leave the raps at the key moves |
| 18 | FX · HALL | A lush 3 s hall that blooms about 70 ms behind the start of each word and dips slightly while you sing. The harmonies sit deeper in it than the lead |
| 19 | DBL IN L / R, with DBL's fader at 0 dB for the check | Each double snaps to the same notes as the lead, wide on its side. Mute DBL for a moment and both doubles should go silent. If they keep playing, a DBL IN track still routes to Master |
| 20 | DBL, fader back at −8 dB | Warm, wide doubles just behind the lead, 6–10 dB under |
| 21 | VOX BUS | Lead, harmonies and doubles sing as one choir |
| 22 | Blend (foundation §4) | Judged on the sung bars: the lead clear but embedded in the harmonies and the hall |
| 23 | Key moves | The harmonies drop out on raps and return on melodies. The last hook line exhales into the hall |
| 24 | Translation (foundation §5.4) | Every check in [Translation notes](#translation-notes) passes |

## Translation notes

Run the checks in foundation §5.4. A fix on a control with key moves goes into its automation clip (foundation §5.3). What to watch for in this preset:

| Check | Watch for | Fix |
|---|---|---|
| **Mono (biggest risk)** | The harmonies thinning or swirling as the choruses fold. The hall narrowing is fine | Lower both choruses' Mix toward 30% |
| Quiet | The hall washing over words | Lower FX · HALL's fader 2 dB |
| Small speaker | A dull lead once the warmth below 300 Hz fades | Ease LEAD slot 9's tilt to −1 dB |
| Loud | Low-mid build-up from the lead and the octave. The octave's high-pass already keeps it off the 808 | Lower PAR · OCT's automation clip 1–2 dB on the sung sections |
| Headphones | A 3rd that lands on a wrong note, changes note late or smears | Fix wrong notes in 3RD LINE, and nudge late ones a little earlier. If it still smears, turn Pitcher's Speed up a little |
