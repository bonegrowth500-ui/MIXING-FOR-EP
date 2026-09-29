# 13 · Vampire Haze

Dark, gothic and drenched: an empty cathedral at 3 AM, with the top rolled soft and long, heavy tails.

**Status:** final. Dialed in (Step 3), stress-tested (Step 4) and cold-read (Step 5).
**Placement:** leans into the beat (D6) · **Tune:** Fast · **Builds on:** [foundation](00-foundation.md) (see §5.6 for how to read the settings)

## Per-song setup

1. **Input level:** loudest lines peak around −10 dBFS on VOX IN, DBL IN L and DBL IN R (foundation §4).
2. **Key and scale:** set the song's key on the Auto-Tune in VOX IN, DBL IN L and DBL IN R.
3. **Key moves:** after the blend (foundation §4), place the throws and the hall eases, plus the endless ending if you want it (see [Key moves](#key-moves)).

## Sound targets

| Target | Value |
|---|---|
| Tone | Dark and warm (Q24). Low cut at 80 Hz, low-mid warmth +2–3 dB near 220 Hz. The top is rolled off from about 8 kHz and is roughly 9 dB down at 13 kHz, which outweighs the mic's own +5 dB there. 2–4 kHz stays put so rapped words still read: dark, not buried |
| Density | 9–11 dB total, with warm tape saturation |
| Grit | Warm tape on the lead, plus a tape-saturated hall return: the "dirty fog" |
| Space | The wettest of the five. A dark 2–3 s hall (Vintage style) with 50 ms of pre-delay, ducked by the voice. Near-frozen throws on the last word of key lines (Q23). Wet 5/5 |
| Width | Lead mono. Doubles at L/R 70. Hall and throws fully wide |
| Placement | Leans into the beat: the least presence and the most wet of the five |
| Tune | Fast: retune 10–20, humanize and Flex-Tune around 20 |

## Upgrades (Q27)

- **Throws on their own return.** A separate near-frozen return lets the main hall stay a tidy 2–3 s. (Phase 1 put freeze and long throws on the hall itself.)
- **Grainier hall.** Pro-R 2's Vintage style gives the space an older, grainier character before the tape even touches it.
- **Low-mid control on both sides.** A multiband stage on the lead keeps the added warmth from blooming into boom on low notes. The hall's own EQ keeps 300–400 Hz out of the long tails.
- **Throws that step aside.** The near-frozen tail ducks under the next lines (keyed from VOX IN) and swells back in the gaps, so it never buries new words.
- **Band-limited throws.** The frozen tails are filtered to about 300 Hz–5 kHz, so they never cloud the low end or hiss.

## Track map

| Track | Gets audio from | Routes to | Sends | Fader (start) |
|---|---|---|---|---|
| VOX IN | Lead clips | LEAD | Sidechain only to FX · THROW (right-click › Sidechain to this track, no audio): the ducking key | 0 dB |
| LEAD | VOX IN | VOX BUS | FX · HALL 100%, FX · THROW 0% (automated only) | 0 dB |
| DBL IN L / R | Left / right double clips | DBL | — | 0 dB, panned L70 / R70 |
| DBL | DBL IN L, DBL IN R | VOX BUS | FX · HALL 100% | −8 dB |
| FX · HALL | Sends | VOX GROUP | — | −8 dB |
| FX · THROW | Sends | VOX GROUP | — | −10 dB |
| VOX BUS | LEAD, DBL | VOX GROUP | — | 0 dB |
| VOX GROUP | VOX BUS, FX tracks | Master | — | Set against the beat, with peaks at or below −6 dBFS |

## VOX IN

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 60 Hz, 12 dB/oct | Rumble only |
| 2 | Pro-G | Vocal style · Threshold −35 dB · Ratio 2:1 · Range 6 dB · Attack 1 ms · Hold 50 ms · Release 150 ms · Lookahead 2 ms | In a sound this wet, breaths turn into long, ghostly tails. The threshold sits just above typical breaths, so they dip by up to 6 dB before reaching the hall while words don't. Lower it if word tails get clipped |
| 3 | Auto-Tune Artist | Alto/Tenor · song's key and scale · Retune Speed 15 · Humanize 20 · Flex-Tune 20 · Natural Vibrato 0 · Formant off · Classic Mode off | Quick correction that still lets the melancholy slides through |

## LEAD

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 80 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −4 dB · optional: a narrow dynamic cut on any ringing resonance | Box control matters more here, because a long reverb exaggerates boxiness |
| 2 | Pro-C | Classic style · Ratio 4:1 · Attack 3 ms · Release 80 ms · Knee 9 dB · Threshold about −15 dB, for 3–5 dB GR · Gain to level-match | Peaks would splash the hall and the throws |
| 3 | Pro-Q | Bell 220 Hz, Q 0.7, +2.5 dB | Warm body for the gothic weight |
| 4 | Saturn 2 | 1 band · Warm Tape · Drive 25% · Mix 60% · HQ on · Level to match | Thickens the darkness (Phase 1). Warm Tape adds lows and gently softens the very top |
| 5 | Pro-C | Opto style · Ratio 3:1 · Attack 10 ms · Release Auto · Knee 18 dB · Threshold about −19 dB, for 2–3 dB GR · Gain to level-match | A steady level into the hall means steady tails |
| 6 | Pro-Q | High Shelf 8 kHz, Q 0.7, −5 dB · High Cut 10 kHz, 12 dB/oct | The dark half of the tone curve (Q24). About −9 dB at 13 kHz, but only about −0.5 dB at 4 kHz, so the words stay clear |
| 7 | Pro-DS | Single Vocal · Split Band · Threshold −32 dB, for 3–5 dB on S's · Range 10 dB · detection 4.5–10 kHz · Lookahead 5 ms | S's in a long hall and in the throws turn into splashes, so they're caught before the sends. The detection sits a little lower to match the darker tone |
| 8 | Pro-MB | Band 1: 150–450 Hz · Compress mode · Range −4 dB · Ratio 3:1 · Attack 40% · Release 50%. Band 2: 2.5–5 kHz · Compress mode · Range −3 dB · Ratio 3:1 · Attack 20% · Release 30%. Negative Range = downward. Pro-MB's times are percentages: slower on the low band, faster on the upper one. Each threshold set so the band only acts when it builds | Keeps the added warmth and room box from blooming into boom on low notes, before any of it reaches the hall (band 1). Band 2 catches upper-mid spikes |
| 9 | Pro-Q | Bell 1.2 kHz, Q 1.0, −1 dB | Takes a little forwardness out of the mids, so the lead leans back into the beat without losing the 2–4 kHz words |
| 10 | Pro-L 2 | Transparent style · Gain about +10 dB, adjusted until the loudest lines show 1–2 dB GR · Output −3.0 dBFS · Lookahead 3 ms | Keeps what goes into the hall and throws consistent |

**Density check** (slots 2 + 4 + 5 + 10, on the loudest lines): about 4 + 1.5 + 2.5 + 1.5 dB, roughly 9.5 dB total (target 9–11). Pro-MB only adds when a band builds.

**Order notes:** the darkening EQ (6) comes before the de-esser (7), so it de-esses the final tone. Everything that feeds the hall and the throws is under control before the sends.

## Parallel tracks

None. This preset's character lives in the space, so it doesn't need a parallel layer.

## FX returns

**The throw and dark-return engine.**

### FX · HALL

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Vintage style · Space 2.5 s · Decay Rate 100% · Predelay 50 ms · Brightness −50% · Character 40% · Distance 50% · Thickness 50% · Stereo Width 50% · Mix 100% · Ducking about 8 dB | The long dark hall (Q23). Heavy ducking keeps the words clear through a 5/5-wet sound (D15). 50% is full stereo |
| 2 | Saturn 2 | 1 band · Warm Tape · Drive 35% · Mix 100% · HQ on · Level to match | Turns the tail into Phase 1's dirty fog |
| 3 | Pro-Q | Low Cut 250 Hz, 12 dB/oct · Bell 350 Hz, Q 1.0, −3 dB · Low Cut 400 Hz, 12 dB/oct, on Side only · High Cut 6 kHz, 12 dB/oct · Output 0 dB | Dark, with mono lows (D7). The 350 Hz dip keeps the wettest hall of the five from turning to mud, since it's fed a warm, boosted lead and then saturated |

**Level:** fader at −8 dB.

### FX · THROW

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-R 2 | Vintage style · Space at maximum (about 10 s) · Decay Rate 200% · Predelay 0 ms · Brightness −60% · Character 30% · Distance 60% · Thickness 40% · Stereo Width 50% · Mix 100% · Ducking off · Freeze off | A tail of around 20 s, long enough to feel frozen, on key line endings only (Q23). Freeze is there for an endless ending |
| 2 | Pro-Q | Low Cut 300 Hz, 24 dB/oct · High Cut 5 kHz, 24 dB/oct · Output 0 dB | Frozen tails stay out of the low end and don't hiss |
| 3 | Pro-C | Clean style · Ratio 4:1 · Attack 5 ms · Release 400 ms · Knee 12 dB · Threshold about −25 dB, for 6–8 dB GR while the vocal plays · Auto Gain off · Gain 0 dB · side chain External, keyed from VOX IN (foundation §2, "Ducking a return") | The frozen tail steps under the next lines and swells back in the gaps. Pro-R 2's own Ducking can't do this, because the throw's input is silent once the word has passed (D15) |

**Level:** fader at −10 dB. LEAD's send to this track sits at 0% except during throws, and VOX IN feeds it a sidechain-only key for slot 3.

**Buildable:** yes. Pro-R 2's Space, Decay Rate, Vintage style, Brightness, Thickness, Ducking and Freeze, Saturn 2's Warm Tape and Pro-C's external side chain are confirmed (foundation §1). Ducking's unit is a Check item: if your knob reads in %, see §5.6.

## Buses

| Track | Slot | Plugin | Settings | Why |
|---|---|---|---|---|
| VOX BUS | 1 | Pro-C | Opto style · Ratio 2:1 · Attack 30 ms · Release Auto · Knee 18 dB · Threshold about −10 dB, for 1–2 dB GR · Gain to level-match | Glues the lead and doubles before the space takes over |

VOX GROUP stays empty.

## DBL

**DBL IN L / DBL IN R:** the VOX IN chain exactly (same three slots, same settings), faders at 0 dB, panned L70 / R70.

| Slot | Plugin | Settings | Why |
|---|---|---|---|
| 1 | Pro-Q | Low Cut 120 Hz, 12 dB/oct · Bell 400 Hz, Q 1.4, dynamic −4 dB | The lead carries the body |
| 2 | Pro-C | Classic style · Ratio 6:1 · Attack 3 ms · Release 80 ms · Knee 9 dB · Threshold about −17 dB, for 5–7 dB GR · Gain to level-match | Tighter than the lead, so the doubles blend |
| 3 | Saturn 2 | 1 band · Warm Tape · Drive 25% · Mix 60% · HQ on · Level to match | Matches the lead's grain |
| 4 | Pro-Q | Bell 3 kHz, Q 1.0, −1.5 dB · High Shelf 7 kHz, −6 dB · High Cut 8 kHz, 12 dB/oct | Darker than the lead at every frequency, so the lead stays in front |
| 5 | Pro-DS | Single Vocal · Split Band · Threshold about −36 dB, for 5–8 dB on S's · Range 12 dB · detection 4.5–10 kHz · Lookahead 5 ms | S's stack up across takes, and the hall exaggerates them. The threshold sits lower than the lead's because slot 4 already darkened the doubles |
| 6 | Pro-L 2 | Transparent style · Gain about +10 dB, for 1–2 dB GR · Output −3.0 dBFS · Lookahead 3 ms | Brings the doubles up to the lead's level, so the −8 dB fader really puts them 6–10 dB under (D23) |

**Level:** fader at −8 dB (6–10 dB under LEAD). **Send:** FX · HALL at 100%. Sends are post-fader, so it lands 6–10 dB below LEAD's. No throw send: throws stay a solo-voice moment.

## Key moves

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| 1 | Cathedral throw | LEAD › send to FX · THROW | 0% → 100% → 0% | The last word of key lines: open just before the word, close right after it | The signature moment (Q23). Only that word feeds the frozen tail, which then ducks under the next lines on its own |
| 2 | Hall eases | LEAD › send to FX · HALL | 100% → 60% → 100% | Dense rap lines | Keeps words readable in the fastest bars |
| 3 | Endless ending (optional) | FX · THROW › Pro-R 2 Freeze, then FX · THROW › fader | Freeze off → on, then the fader from −10 dB (or your blended level) down to −∞ over the last 2–4 bars | Throw the song's final word with move 1, turn Freeze on right after it, then fade | The last tail hangs, then fades before the song ends. Freeze sits inside the plugin, so automate it through Tools › Last tweaked (foundation §5.3) |

## Ear checks

Build in this order, one stage at a time (foundation §5.7).

| # | Stage | You should hear |
|---|---|---|
| 1 | Template and input (foundation §2, §4, §5.7) | The loudest lines peak around −10 dBFS on VOX IN. With the unbuilt tracks muted, mute LEAD for a moment and the vocal should go silent. If it keeps playing, VOX IN still routes to Master |
| 2 | VOX IN 1–3 | Quick correction that still lets slides bend. Breaths dip a little, words don't |
| 3 | LEAD 1 · Pro-Q | Boxiness eases on close and low words |
| 4 | LEAD 2 · Pro-C | Peaks stop spiking |
| 5 | LEAD 3 · Pro-Q | A warm, heavy body |
| 6 | LEAD 4 · Saturn 2 | Thicker and warmer, with the very top softened slightly |
| 7 | LEAD 5 · Pro-C | A steady level from line to line |
| 8 | LEAD 6 · Pro-Q | The top rolls off: darker and softer, but the words stay clear |
| 9 | LEAD 7 · Pro-DS | S's tamed, with no lisp |
| 10 | LEAD 8 · Pro-MB | Low notes stop blooming into boom, and upper-mid spikes get caught |
| 11 | LEAD 9 · Pro-Q | The lead leans back a little, with the words still clear |
| 12 | LEAD 10 · Pro-L 2 | The lead comes up about 10 dB and holds steady. If Master clips, pull VOX GROUP down for now. The blend sets it properly |
| 13 | FX · HALL 1 · Pro-R 2 | A long, dark, grainy hall that dips under the words and swells in the gaps |
| 14 | FX · HALL 2–3 | The tail turns into a dirty fog, dark and free of mud |
| 15 | FX · THROW 1–2: by hand, turn LEAD's send to it up to 100% just before one line's last word, then back to 0% | That word hangs as a near-frozen tail, with no lows and no hiss. Leave the send at 0% afterward |
| 16 | FX · THROW 3, after wiring the key (foundation §2, Ducking a return) | With LEAD's send at 0%, FX · THROW stays silent (if it echoes every word, the VOX IN connection is a normal route). Throw one word again: the tail steps under the next line and swells back in the gap |
| 17 | DBL IN L / R, with DBL's fader at 0 dB for the check | Each double snaps to the same notes as the lead, on its own side. Mute DBL for a moment and both doubles should go silent. If they keep playing, a DBL IN track still routes to Master |
| 18 | DBL, fader back at −8 dB | Darker doubles just behind the lead, 6–10 dB under |
| 19 | VOX BUS | The lead and doubles glued and steady before the space takes over |
| 20 | Blend (foundation §4) | The lead leaning into the beat, drenched but readable |
| 21 | Key moves | Key line endings hang in the frozen throw, and dense raps get drier. The optional ending holds, then fades |
| 22 | Translation (foundation §5.4) | Every check in [Translation notes](#translation-notes) passes |

## Translation notes

Run the checks in foundation §5.4. A fix on a control with key moves goes into its automation clip (foundation §5.3). What to watch for in this preset:

| Check | Watch for | Fix |
|---|---|---|
| Mono | Hollow tails from the hall or the throws | Lower Stereo Width on the Pro-R 2 of whichever return goes hollow to about 40%. Only settings below 50% narrow it |
| **Quiet (biggest risk)** | Words blurring, since this is the wettest of the five | Lower FX · HALL's fader 2 dB |
| Small speaker | Words sinking into the fog: a phone loses the lead's 220 Hz body but still plays the whole hall. 2–4 kHz is already protected | Bypass LEAD slot 9's dip. If words still sink, lower FX · HALL's fader 2 dB |
| Loud | Boom on low notes as the warmth and the hall build | Lower Pro-MB band 1's threshold until low notes show 2–4 dB |
| Headphones | Throw tails crowding the next lines | Lower FX · THROW's Pro-C threshold until the tails duck 8–10 dB under the lines |
