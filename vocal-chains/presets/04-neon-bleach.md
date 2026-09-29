# 04 · Neon Bleach

Glossy, very bright and expensive: a hard-tuned lead right in your face, with crystalline air on top.

**Status:** final. Dialed in (Step 3), stress-tested (Step 4) and cold-read (Step 5).
**Placement:** on top, the most upfront of the five (D6) · **Tune:** Hard · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R. PAR · OCT UP stays on Chromatic (D20).
3. **Key moves:** after the blend (foundation §4), place the ghost opens, the air lift and the bed dips (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Very bright (Q19). Low cut at 80 Hz. Body +2 dB near 200 Hz, because bright chains make a thin voice thinner. Presence mostly from the mic. Strong air from Fresh Air plus a gentle 12 kHz shelf, about +4–6 dB of top end beyond the mic's own. S's held by a de-esser after all the brightness |
| Density | 11–13 dB total: a fast FET-style grab, then smooth opto leveling |
| Grit | Hidden. Saturn is blended in parallel inside the plugin, adding density with no audible dirt |
| Space | A soft 1/8 ping-pong bed that ducks while you sing and blooms in the gaps (Q20), 16–20 dB under the lead. A short bright plate of about 1 s, kept low. Wet 2/5 |
| Width | Lead mono. The widest doubles of the five (L/R 90), the ping-pong's motion, and an octave-up ghost layer chorused wide, 14–18 dB under the lead |
| Placement | On top, most upfront: the most presence of the five |
| Tune | Hard: retune 0, the fastest of the five, with humanize and Flex-Tune at the bottom of the foundation's base range |

## Upgrades (Q27)

- **Dynamic air.** Phase 1's single big air shelf becomes Fresh Air, which rises and falls with the voice, followed by a gentle static shelf. That gives more sparkle with less sibilance.
- **Harsh-zone clamp.** A dynamic band on 3–5 kHz after the de-esser catches loud notes that go glassy under hard tune.
- **Ghost layer built as an octave up.** Phase 1's ghost harmony becomes an octave-up layer. It always lands in key and needs no per-song setup (D11).

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD | — | 0 dB |
| LEAD | VOX IN | VOX BUS, and PAR · OCT UP at 100% | FX · DELAY 100%, FX · PLATE 100% | 0 dB |
| PAR · OCT UP | LEAD | VOX BUS | FX · PLATE 100% | −14 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L90 / R90 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · DELAY 100%, FX · PLATE 100% | −8 dB |
| FX · DELAY | Sends | VOX GROUP | — | −12 dB |
| FX · PLATE | Sends | VOX GROUP | — | −20 dB |
| VOX BUS | LEAD, PAR · OCT UP, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX tracks | Master | — | Set against the beat, with peaks at or below −6 dBFS |

Sends are post-fader, so tracks that sit lower (DBL, PAR) automatically feed the returns less.

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct | Rumble only. Nothing vocal lives below 60 Hz |
| 2 | Pro-G | Vocal style · Threshold −35 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | A bright chain makes breaths bright too. The threshold sits just above typical breaths, so they dip by up to 6 dB while words don't. Lower it if word tails get clipped |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 0 · Humanize 10 · Flex-Tune 10 · Natural Vibrato 0 · Formant off · Classic Mode off | Instant snap for the gloss. Humanize and Flex-Tune at the bottom of the base range keep even rapped lines locked. Some stepping on spoken glides is part of the hard-tune sound |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 80 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · optional: a narrow dynamic cut on any ringing resonance | A very bright chain exaggerates box and resonances, so they're handled first |
| 2 | Pro-C | Punch style · Ratio 6:1 · Attack 0.5 ms · Release 50 ms · Knee 6 dB · Threshold about −16 dB, for 4–6 dB GR · Gain to level-match | Phase 1's fast FET-style grab |
| 3 | Pro-Q | Bell 200 Hz, Q 0.8, +2 dB | Body before brightness, so the gloss doesn't thin a thin voice further |
| 4 | Saturn 2 | 1 band · Clean Tube · Drive 20% · Mix 25% · HQ on · Level to match | Hidden parallel density: fuller at the same level, never audibly dirty. Clean Tube leans bright, which suits this preset |
| 5 | Pro-C | Opto style · Ratio 3:1 · Attack 10 ms · Release Auto · Knee 18 dB · Threshold about −20 dB, for 3–4 dB steady GR · Gain to level-match | Phase 1's smooth opto leveling, for an even, expensive line |
| 6 | Fresh Air | Mid Air 25% · High Air 55% · Trim to level-match | The dynamic air: a strong top (Q19) and modest presence, since the mic already has presence |
| 7 | Pro-Q | High Shelf 12 kHz, Q 0.7, +2 dB | Finishes the air. With Fresh Air, that's about +4–6 dB of top end beyond the mic's own |
| 8 | Pro-DS | Single Vocal · Split Band · Threshold −30 dB, for 3–6 dB on S's · Range 10 dB · detection 5–12 kHz · Lookahead 5 ms | Catches the S's both air stages lifted |
| 9 | Pro-Q | Bell 3.8 kHz, Q 1.5, dynamic −3 dB | Clamps loud notes that turn glassy under hard tune, only when they spike |
| 10 | Pro-L 2 | Modern style · Gain about +10 dB, adjusted until the loudest lines show 1–3 dB GR · Output −3.0 dBFS · Lookahead 2 ms | Holds the most upfront lead of the five flat |

**Density check** (slots 2 + 4 + 5 + 10, on the loudest lines): about 5 + 1.5 + 3.5 + 2 dB, roughly 12 dB total (target 11–13).

**Order notes:** both brightness stages (6, 7) sit before the de-esser (8), so it sees the final top end. The harsh-zone clamp (9) comes after the de-esser, so it only deals with glassy notes, not S's. This moves de-essing and dynamic control one slot later than the foundation template, to make room for the second air stage.

## Parallel tracks

### PAR · OCT UP (the ghost layer)

**Feed:** LEAD, with the route at 100%. The layer inherits the finished gloss, compression and de-essing before it's shifted, so it arrives as a bright, controlled voice.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Auto-Tune Artist | Alto/Tenor · Chromatic · Retune Speed 50 · Humanize 0 · Flex-Tune 100 · Natural Vibrato 0 · Transpose +12 · Formant on · Throat 100 · Classic Mode off | Shifts up an octave without re-tuning. Formant keeps it a voice, not a chipmunk (D20) |
| 2 | Pro-Q | Low Cut 400 Hz, 24 dB/oct · High Shelf 9 kHz, −3 dB · Output 0 dB | Shimmer only: no low-mid clutter, no hiss |
| 3 | Pro-C | Clean style · Ratio 4:1 · Attack 5 ms · Release 80 ms · Knee 12 dB · Threshold about −12 dB, for 4–6 dB GR · Gain to level-match | A ghost has to stay constant |
| 4 | Vintage Chorus | Mode I · Mix 50% | Phase 1's "tucked wide". Mode I is the gentlest, widest Juno setting |

**Level:** fader at −14 dB, its verse level. The 400 Hz high-pass trims about 4 dB first, so that lands about 18 dB under LEAD. The key move lifts it to −10 dB on hooks, about 14 dB under. Fine-tune with the ghost test (foundation §4).

**Buildable:** yes. Transpose +12 is within Auto-Tune's ±12, Formant needs the Modern algorithm (D16), and Vintage Chorus is FL stock (foundation §1).

## FX returns

### FX · DELAY (the soft bed)

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Timeless 3 | Delay Sync on, 1/8 · Delay Offset 100% · Delay Time Pan centered, so both sides match · Ping Pong on, starting left · Feedback 30% · Stretch mode · Filters: High Pass 400 Hz, Low Pass 7 kHz (default slopes) · Mix 100% · Wet Level 0 dB · ducking: envelope follower → Wet Level, about −12 dB, attack short, release about 150 ms (foundation §2, "Ducking a return") | Q20: ducks up to 12 dB under the words and blooms in the gaps (D15). The short release lets the first repeat after a line come through, since a 1/8 note is only about 200 ms at trap tempos. The filters keep repeats out of the body and away from S's |
| 2 | Pro-Q | Low Cut 500 Hz, 12 dB/oct, on Side only · Output 0 dB | Mono lows (D7). Timeless's High Pass already keeps the repeats off the body |

**Level:** fader at −12 dB. The 400 Hz high-pass takes about 4 dB off the repeats, so they land 16–20 dB under the lead.

### FX · PLATE

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-DS | Allround · Wide Band · Threshold about −22 dB, for 6–8 dB on S's · Range 12 dB · detection 5–10 kHz · Lookahead 5 ms | A bright plate turns every S into a splash. This cleans what the lead, doubles and ghost send before it reaches the plate |
| 2 | Pro-R 2 | Plate style · Space 1.0 s · Decay Rate 100% · Predelay 20 ms · Brightness +20% · Character 30% · Distance 30% · Thickness 20% · Stereo Width 50% · Mix 100% · Ducking off | Phase 1's short bright plate: sheen, not space. 50% is full stereo |
| 3 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Low Cut 400 Hz, 12 dB/oct, on Side only · Output 0 dB | Keeps the plate off the body, with mono lows |

**Level:** fader at −20 dB. You should feel it more than hear it.

## Buses

| Track | Slot | Plugin | Settings | Why |
|---|---|---|---|---|
| VOX BUS | 1 | Pro-C | Bus style · Ratio 2:1 · Attack 30 ms · Release Auto · Knee 12 dB · Threshold about −10 dB, for 1–2 dB GR · Gain to level-match | Glues the lead, ghost and doubles into one gloss |

VOX GROUP stays empty.

## DBL

**DBL IN L / DBL IN R:** the VOX IN chain exactly (same three slots, same settings), faders at 0 dB, panned L90 / R90.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 120 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB | The lead carries the body |
| 2 | Pro-C | Punch style · Ratio 8:1 · Attack 1 ms · Release 60 ms · Knee 6 dB · Threshold about −18 dB, for 6–8 dB GR · Gain to level-match | Tighter than the lead, so the doubles blend |
| 3 | Saturn 2 | 1 band · Clean Tube · Drive 20% · Mix 25% · HQ on · Level to match | The same density as the lead |
| 4 | Fresh Air | Mid Air 15% · High Air 35% · Trim to level-match | Bright, but just behind the lead |
| 5 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB, for 5–8 dB on S's · Range 12 dB · detection 5–12 kHz · Lookahead 5 ms | Very bright doubles stack S's fastest |
| 6 | Pro-Q | Bell 4 kHz, Q 1.0, −2 dB · High Shelf 10 kHz, −2 dB | Tone offset that keeps the lead in front |
| 7 | Pro-L 2 | Modern style · Gain about +10 dB, for 1–2 dB GR · Output −3.0 dBFS · Lookahead 2 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Sends:** FX · DELAY and FX · PLATE at 100%. Sends are post-fader, so they land 6–10 dB below LEAD's.

## Key moves

No throws here: Q20 chose a soft bed.

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Ghost opens | PAR · OCT UP › fader | −14 dB → −10 dB | Hooks, with 1-beat ramps in and out | More gloss where it counts, cleaner verses |
| 2 | Air lift | LEAD › Fresh Air High Air | 55% → 65% | Hooks, with 1-beat ramps in and out | Extra shine on the hook. It's a control inside the plugin, so automate it through Tools › Last tweaked (foundation §5.3) |
| 3 | Bed dips | FX · DELAY › fader | −12 dB → −18 dB | Dense rap lines, with 1-beat ramps in and out | Keeps fast bars clear. Riding the return also catches the doubles' echoes, and it doesn't weaken the envelope follower's ducking the way a lower send would |

## Ear checks

Build in this order, one stage at a time (foundation §5.7).

| # | Stage | You should hear |
|---|---|---|
| 1 | Template and input (foundation §2, §4, §5.7) | The loudest lines peak around −10 dBFS on VOX IN. With the unbuilt tracks muted, mute LEAD for a moment and the vocal should go silent. If it keeps playing, VOX IN still routes to Master |
| 2 | VOX IN 1–3 | An instant, glossy snap: held notes lock dead-on. Some stepping on spoken glides is part of the sound. Breaths dip a little, words don't |
| 3 | LEAD 1 · Pro-Q | Box and any ringing ease on close words |
| 4 | LEAD 2 · Pro-C | The front edge of every syllable gets caught, so the lead stops jumping |
| 5 | LEAD 3 · Pro-Q | More chest, so the brightness to come won't thin you out |
| 6 | LEAD 4 · Saturn 2 | Denser and fuller at the same level, with no audible dirt |
| 7 | LEAD 5 · Pro-C | The whole line evens out and sounds polished |
| 8 | LEAD 6 · Fresh Air | Much brighter and airier, with air that rises and falls with your level. S's sharpen, which slot 8 handles |
| 9 | LEAD 7 · Pro-Q | A final glassy sheen at the very top |
| 10 | LEAD 8 · Pro-DS | S's back under control, with the sheen intact |
| 11 | LEAD 9 · Pro-Q | Loud notes stop turning glassy. Everything else is untouched |
| 12 | LEAD 10 · Pro-L 2 | The lead comes up about 10 dB and stays dead steady, with no pumping. If Master clips, pull VOX GROUP down for now. The blend sets it properly |
| 13 | PAR · OCT UP 1, fader at 0 dB for the check | An octave-up copy that still sounds like a voice, not a chipmunk |
| 14 | PAR · OCT UP 2–3 | Only shimmer is left, with no low mids and no hiss, at a constant level |
| 15 | PAR · OCT UP 4 | The layer spreads wide around the lead |
| 16 | PAR · OCT UP, back at −14 dB | Unmuted, the lead sounds glossier and wider. You don't hear a second voice (the ghost test) |
| 17 | FX · DELAY | 1/8 repeats bounce left and right in the gaps and dip under the words, with no low mids in them. If S's tick in the repeats, lower the Low Pass toward 6 kHz |
| 18 | FX · PLATE | A short, bright sheen you feel more than hear, with no S splashes |
| 19 | DBL IN L / R, with DBL's fader at 0 dB for the check | Each double snaps to the same notes as the lead, far out on its side. Mute DBL for a moment and both doubles should go silent. If they keep playing, a DBL IN track still routes to Master |
| 20 | DBL, fader back at −8 dB | Doubles far out on each side, bright but just behind the lead, 6–10 dB under |
| 21 | VOX BUS | Lead, ghost and doubles glue into one gloss, with no pumping |
| 22 | Blend (foundation §4) | The lead right on top of the beat, with the ghost felt and the bed soft |
| 23 | Key moves | The ghost opens and the air lifts on hooks. The bed pulls back on dense raps |
| 24 | Translation (foundation §5.4) | Every check in [Translation notes](#translation-notes) passes |

## Translation notes

Run the checks in foundation §5.4. A fix on a control with key moves goes into its automation clip (foundation §5.3). What to watch for in this preset:

| Check | Watch for | Fix |
|---|---|---|
| Mono | The ghost's chorus swirling or vanishing. The ping-pong losing its left-right bounce is fine | Lower the ghost's Vintage Chorus Mix toward 30% |
| Quiet | The bed covering words | Lower FX · DELAY's automation clip 2 dB |
| **Small speaker (biggest risk)** | S's or glassy notes piercing, since phones exaggerate 2–5 kHz | Lower LEAD slot 8's threshold 2 dB. If loud notes still sting, deepen slot 9's dynamic range to −4 dB |
| Loud | Ear fatigue from the brightness after a few minutes | Lower both points of LEAD's High Air automation clip by 5 (55 → 50%, 65 → 60%) |
| Headphones | The ghost reading as a separate voice | Lower PAR · OCT UP's automation clip 2 dB |
