# 16 · Rockstar Grit

Upfront, gritty and rock-coded: amp-driven snarl, biting mids and a classic slapback, still tuned.

**Status:** final. Dialed in (Step 3), stress-tested (Step 4) and cold-read (Step 5).
**Placement:** on top (D6) · **Tune:** Fast · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R.
3. **Key moves:** after the blend (foundation §4), place the crunch pushes, plus the yell guard if a yell still spikes. Both go in one PAR · CRUNCH fader clip (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Biting mids. Low cut at 90 Hz, body +1.5–2 dB near 200 Hz, snarl around 1–2 kHz. Presence raised carefully, since the mic already adds about 3.5 dB at 4 kHz. Moderate air, led by Mid Air rather than High Air |
| Density | 12–14 dB total including saturation: the most compressed of the five |
| Grit | Crunch (Q25): moderate saturation in the lead, plus a parallel British Rock amp layer 6–10 dB under the lead |
| Space | A ~100 ms slapback plus a small live room of about 0.7 s. Wet 2/5 |
| Width | The narrowest of the five. Lead, crunch and slap centered. Doubles at L/R 60. Room a little narrower than full stereo |
| Placement | On top |
| Tune | Fast: retune 10–15, humanize around 15, Flex-Tune 15–20 so yells and rap pass naturally |

## Upgrades (Q27)

- **Crunch fed from the finished lead.** Yells reach the amp already controlled, so the crunch stays consistent instead of exploding.
- **Gates before the amps.** The crunch and the doubles each get a gate ahead of their distortion, so it never turns breaths into noise.
- **Band-limited snarl.** The crunch is kept between about 250 Hz and 7 kHz, so it bites without fizz or mud.
- **Warm slap.** A touch of Timeless's Drive saturates the repeats for a vintage tape feel. (Tape mode only changes how delay-time moves sound. Drive gives the color.)
- **Crunchier doubles.** The doubles get more amp than the lead, for a gang-vocal edge.

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD | — | 0 dB |
| LEAD | VOX IN | VOX BUS, and PAR · CRUNCH at 100% | FX · SLAP 100%, FX · ROOM 100% | 0 dB |
| PAR · CRUNCH | LEAD | VOX BUS | — | −5 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L60 / R60 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · ROOM 100% | −8 dB |
| FX · SLAP | Sends | VOX GROUP | — | −14 dB |
| FX · ROOM | Sends | VOX GROUP | — | −16 dB |
| VOX BUS | LEAD, PAR · CRUNCH, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX tracks | Master | — | Set against the beat, with peaks at or below −6 dBFS |

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −35 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | Distortion lifts everything quiet, so breaths and room go down before the grit sees them. The threshold sits just above typical breaths, so they dip by up to 6 dB while words don't. Lower it if word tails get clipped |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 12 · Humanize 15 · Flex-Tune 18 · Natural Vibrato 0 · Formant off · Classic Mode off | Still tuned (Phase 1), but loose enough at the edges for yells and rap |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 90 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB · optional: a narrow dynamic cut on any ringing resonance | A tighter low end: rock vocals sit higher |
| 2 | Pro-C | Punch style · Ratio 8:1 · Attack 0.3 ms · Release 40 ms · Knee 3 dB · Threshold about −16 dB, for 5–6 dB GR · Gain to level-match | Phase 1's rock pump, and the first line of yell control (Q26) |
| 3 | Pro-Q | Bell 200 Hz, Q 0.8, +1.5 dB · Bell 1.5 kHz, Q 1.0, +2 dB | Body, plus the snarl zone where the grit will bite |
| 4 | Saturn 2 | 1 band · Warm Tube · Drive 30% · Mix 50% · HQ on · Level to match | The first half of the crunch. A tube here, so the parallel amp layer adds a different color |
| 5 | Pro-C | Classic style · Ratio 4:1 · Attack 5 ms · Release 100 ms · Knee 12 dB · Threshold about −19 dB, for 3–4 dB GR · Gain to level-match | Keeps the saturated line steady |
| 6 | Fresh Air | Mid Air 30% · High Air 20% · Trim to level-match | Upper-mid bite with a little air. Kept at 30% because the mic already peaks at 4 kHz |
| 7 | Pro-Q | Bell 3 kHz, Q 1.2, +1 dB · High Shelf 10 kHz, +1 dB | Final bite, kept small because the mic already lifts 4 kHz |
| 8 | Pro-DS | Single Vocal · Split Band · Threshold −30 dB, for 3–6 dB on S's · Range 10 dB · detection 5–11 kHz · Lookahead 5 ms | Distortion, air and the 10 kHz shelf all sharpen S's |
| 9 | Pro-MB | 1 band, 2–5 kHz · Compress mode · Range −6 dB (negative = downward, so the band's gain dips, never rises) · Ratio 4:1 · Attack 20% · Release 30% · Knee 6 dB · Lookahead 2 ms · Threshold: loop the biggest yell, start at 0 dB and lower it until the yell shows 3–6 dB, then check that a normal loud line shows 0 dB. With no yells in the song, leave it where normal lines show 0 dB | Clamps upper-mid harshness only when a yell spikes (Q26). Pro-MB's times are percentages, and these give a fast grab with a quick recovery |
| 10 | Pro-L 2 | Punchy style · Gain about +10 dB, adjusted until the loudest lines show 2–3 dB GR · Output −3.0 dBFS · Lookahead 1 ms | The last catch for yells (Q26). Punchy suits a single rock vocal |

**Density check** (slots 2 + 4 + 5 + 10, on the loudest lines): about 5.5 + 2 + 3.5 + 2.5 dB, roughly 13.5 dB total (target 12–14). Pro-MB only adds on yells.

**Order notes:** the bite EQ (7) moves ahead of the de-esser (8) and the yell clamp (9), so its boosts can't bring back the S's and harshness those two remove. The clamp sits after the de-esser, so it only handles yell harshness. Compression on both sides of the saturation (2, 5) keeps the grit steady whether you're talking or yelling.

## Parallel tracks

### PAR · CRUNCH (the crunch engine)

**Feed:** LEAD, with the route at 100%. The amp gets the finished, compressed lead, so yells arrive under control.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-G | Classic style · Threshold −24 dB · Ratio ∞:1 · Range 18 dB · Attack 0.5 ms · Hold 90 ms · Release 150 ms · Lookahead 0 ms | The amp only gets voice. The feed is the compressed, limited lead, which lifts breaths to roughly −33 to −23 dBFS, so the threshold starts near the top of that range. The partial range and the longer hold and release let word tails fade instead of chopping. Loop a breathy phrase and move the threshold until Pro-G's meter shows the full range on breaths and none on words |
| 2 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Output 0 dB | Tight distortion: the low end stays out of the amp. The gentle slope keeps a little chest in the snarl |
| 3 | Saturn 2 | 1 band · British Rock (Amp) · Drive 45% · Mix 100% · HQ on · Level to match | The crunch (Q25) |
| 4 | Pro-Q | Bell 5 kHz, Q 3, −3 dB (slide it to wherever fizz sits) · High Cut 7 kHz, 24 dB/oct · Output 0 dB | Snarl without fizz |
| 5 | Pro-C | Classic style · Ratio 4:1 · Attack 5 ms · Release 80 ms · Knee 12 dB · Threshold about −10 dB, for 3–4 dB GR · Gain to level-match | Keeps the snarl a constant support layer |

**Level:** fader at −5 dB. The 250 Hz high-pass trims about 3 dB first, so that lands about 8 dB under LEAD. Adjust until it adds edge without pulling focus: 6–10 dB under. Mono (D7). It's at the same pitch as the lead, so it connects through mixer routes only and relies on FL's automatic delay compensation (D5, D18).

**Buildable:** yes. Saturn 2's British Rock style, Pro-G, Pro-Q and Pro-C are all confirmed (foundation §1).

### Yell control inside the chain (Q26)

Four layers, no second chain:
1. LEAD slot 2: the fast compressor grabs the yell's front edge.
2. LEAD slot 9: Pro-MB clamps upper-mid harshness only when it spikes.
3. LEAD slot 10: Pro-L 2 catches whatever is left.
4. PAR · CRUNCH is fed after all of that, so the amp never gets an uncontrolled yell.

## FX returns

### FX · SLAP

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Timeless 3 | Delay Sync off · Delay Time 100 ms · Delay Time Pan centered, so both sides match · Ping Pong off · Feedback 5% · Tape mode · Drive 20% · Filters: High Pass 300 Hz, Low Pass 5 kHz (default slopes) · Mix 100% · Wet Level 0 dB · no ducking | Phase 1's classic slapback. It's part of the sound, so it doesn't duck. Drive gives the tape color, and the High Pass keeps the slap off the body. Both sides share one time, so the slap is centered and needs no mono fix |

**Level:** fader at −14 dB.

### FX · ROOM

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Modern style · Space 0.7 s · Decay Rate 100% · Predelay 10 ms · Brightness 0% · Character 60% · Distance 40% · Thickness 30% · Stereo Width 35% · Mix 100% · Ducking off | Phase 1's small live room. The high Character makes it lively, and 35% keeps it a little narrower than full stereo (50%) |
| 2 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Low Cut 400 Hz, 12 dB/oct, on Side only · Output 0 dB | Keeps the room off the body, with mono lows (D7) |

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
| 1 | Pro-Q | Low Cut 130 Hz, 18 dB/oct · Bell 400 Hz, Q 1.4, dynamic −3 dB | The lead carries the body |
| 2 | Pro-G | Classic style · Threshold about −35 dB · Ratio ∞:1 · Range 18 dB · Attack 0.5 ms · Hold 90 ms · Release 150 ms · Lookahead 0 ms | The 10:1 compressor and the amp after it lift everything quiet, so breaths go down first. Loop a breathy phrase and move the threshold until Pro-G's meter shows the full range on breaths and none on words |
| 3 | Pro-C | Punch style · Ratio 10:1 · Attack 0.5 ms · Release 40 ms · Knee 3 dB · Threshold about −19 dB, for 7–9 dB GR · Gain to level-match | Rock doubles sit flat and dense |
| 4 | Saturn 2 | 1 band · British Rock (Amp) · Drive 35% · Mix 60% · HQ on · Level to match | More amp than the lead, for a gang-vocal edge (upgrade) |
| 5 | Pro-Q | Bell 3.5 kHz, Q 1.0, −2 dB · High Cut 8 kHz, 12 dB/oct | Less presence than the lead, so the lead stays in front |
| 6 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB, for 5–8 dB on S's · Range 12 dB · detection 5–11 kHz · Lookahead 5 ms | Crunch sharpens S's, and they stack across takes |
| 7 | Pro-L 2 | Punchy style · Gain about +10 dB, for 1–2 dB GR · Output −3.0 dBFS · Lookahead 1 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · ROOM at 100%. Sends are post-fader, so it lands 6–10 dB below LEAD's. No slap send: the slap is a centered, lead-only echo, and on panned doubles it would add off-center repeats that blur the timing.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Crunch push | PAR · CRUNCH › fader | −5 dB → −3 dB | Hooks, with 1-beat ramps | More snarl where the energy peaks |
| 2 | Yell guard | PAR · CRUNCH › fader | −5 dB → −9 dB (or −3 → −7 inside a hook) | The biggest yell of the song, only if needed, with 1/16-note ramps. Draw it in the same clip as the pushes (foundation §5.3) | The chain already handles yells (Q26). This is the safety for one that still spikes |

## Ear checks

Build in this order, one stage at a time (foundation §5.7).
Include the song's biggest yell in the loop, or loop it separately for stages 4, 11 and 12.

| # | Stage | You should hear |
|---|---|---|
| 1 | Template and input (foundation §2, §4, §5.7) | The loudest lines peak around −10 dBFS on VOX IN. With the unbuilt tracks muted, mute LEAD for a moment and the vocal should go silent. If it keeps playing, VOX IN still routes to Master |
| 2 | VOX IN 1–3 | Tuned, but yells and rap lines still bend naturally. Breaths dip a little, words don't |
| 3 | LEAD 1 · Pro-Q | A tighter low end, and box eases on close words |
| 4 | LEAD 2 · Pro-C | Rock pump: the front edge of every syllable and yell gets grabbed |
| 5 | LEAD 3 · Pro-Q | More body, plus a nasal snarl around 1.5 kHz |
| 6 | LEAD 4 · Saturn 2 | Warm tube density with a first touch of grit |
| 7 | LEAD 5 · Pro-C | The gritty line holds steady, talking or yelling |
| 8 | LEAD 6 · Fresh Air | Upper-mid bite with a little air |
| 9 | LEAD 7 · Pro-Q | A final small bite |
| 10 | LEAD 8 · Pro-DS | S's back under control after all that bite |
| 11 | LEAD 9 · Pro-MB | Yells lose their harsh edge, and normal lines are untouched |
| 12 | LEAD 10 · Pro-L 2 | The lead comes up about 10 dB, and even the biggest yells stay under the ceiling. If Master clips, pull VOX GROUP down for now. The blend sets it properly |
| 13 | PAR · CRUNCH 1 · Pro-G | On a breathy phrase, Pro-G's meter shows the full range on breaths and none on words |
| 14 | PAR · CRUNCH 2–3, fader at 0 dB for the check | An amp-driven snarl on top of the lead, with no low-end mud |
| 15 | PAR · CRUNCH 4–5 | The fizz disappears and the snarl stays even |
| 16 | PAR · CRUNCH, back at −5 dB | Edge and attitude without pulling focus (the support test) |
| 17 | FX · SLAP | One tight, warm 100 ms slap, centered |
| 18 | FX · ROOM | A small, lively room around the voice |
| 19 | DBL IN L / R, with DBL's fader at 0 dB for the check | Each double snaps to the same notes as the lead, on its own side. Mute DBL for a moment and both doubles should go silent. If they keep playing, a DBL IN track still routes to Master |
| 20 | DBL, fader back at −8 dB | Dense, amped doubles with no breath noise, just behind the lead, 6–10 dB under |
| 21 | VOX BUS | Lead, crunch and doubles hit together |
| 22 | Blend (foundation §4) | The lead on top, gritty and upfront: lead, crunch and slap dead center, doubles at L/R 60, the room only a little wider |
| 23 | Key moves | More snarl on hooks. The yell guard pulls the crunch back on the biggest yell |
| 24 | Translation (foundation §5.4) | Every check in [Translation notes](#translation-notes) passes |

## Translation notes

Run the checks in foundation §5.4. A fix on a control with key moves goes into its automation clip (foundation §5.3). What to watch for in this preset:

| Check | Watch for | Fix |
|---|---|---|
| Mono | The room going hollow. Lead, crunch and slap are centered, and the doubles fold down cleanly | Lower the room's Stereo Width to 25% |
| Quiet | The crunch covering words | Lower PAR · CRUNCH's automation clip 1–2 dB |
| Small speaker | Crunch fizz, which phones show first | Slide the crunch's 5 kHz bell (PAR · CRUNCH slot 4) onto it, or lower its High Cut to 6 kHz |
| **Loud (biggest risk)** | Harshness at volume from grit plus bite | Lower LEAD slot 9's threshold 2–3 dB more, so yells use the full 6 dB Range. If the crunch is the harsh part, add a second bell in PAR · CRUNCH slot 4 (Q 3, −2 dB) on that spot and leave the 5 kHz bell on the fizz. If normal lines are harsh too, set LEAD slot 7's 3 kHz bell to 0 dB |
| Headphones | The slap reading as a separate echo instead of part of the voice | Lower FX · SLAP 2 dB |
