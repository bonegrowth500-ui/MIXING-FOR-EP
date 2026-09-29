# Foundation

Shared ground rules for all five presets. Each preset sheet builds on the template here and spells out every one of its own settings. Decision numbers (D#) point to the [build plan](../phase-3-build-plan.md#decisions).

---

## 1 · Toolkit reference

The controls the sheets can use, with how sure each one is:
- **Confirmed:** checked against a published source during this step.
- **Known:** a long-standing control that wasn't re-sourced.
- **Check:** the exact label or range couldn't be confirmed. Glance at your screen the first time you use it.

This environment's network policy blocked the manufacturers' sites, so confirmation came through web search. Sources are at the bottom.

**Versions (D1):** Pro-C and Pro-Q both had recent major releases. Core settings stick to what Pro-C 2 and Pro-Q 3 share with the new versions, and anything newer is marked optional. Every other plugin targets its current version.

### Auto-Tune Artist

| Control | Notes | Status |
|---|---|---|
| Input Type | Soprano · Alto/Tenor · Low Male · Instrument · Bass Instrument | Confirmed |
| Key / Scale | Set per song | Known |
| Retune Speed | In ms, 0–400. 0 = instant, robotic snap | Confirmed |
| Humanize | Applies a slower retune only to sustained notes | Confirmed |
| Flex-Tune | 0 pulls every note to target. Higher values let more natural movement through. Modern algorithm only | Confirmed |
| Natural Vibrato | Scales the singer's own vibrato | Known |
| Formant | Keeps the natural vocal character when pitch shifts | Confirmed |
| Throat | Only active with Formant on. 100 = neutral, higher = longer throat (deeper), lower = shorter (younger) | Confirmed (range ends: Check; sheets stay within 80–140) |
| Transpose | ±12 semitones, in semitone steps | Confirmed |
| Classic Mode | The Auto-Tune 5 sound. Turns off Formant, Throat, Transpose and Flex-Tune | Confirmed |
| Tracking | Pitch-detection sensitivity | Known |

### Fresh Air

| Control | Notes | Status |
|---|---|---|
| Mid Air | Presence, roughly 2–5 kHz | Confirmed (band is approximate) |
| High Air | Top-end sheen, roughly 10 kHz and up | Confirmed (band is approximate) |
| Link | Locks both knobs together | Confirmed |
| Trim | Output level match | Confirmed |
| Scale | 0–100% on both knobs | Confirmed |

### FabFilter

| Plugin | Controls the sheets use | Status |
|---|---|---|
| **Pro-Q 3/4** | Shapes: Bell, Low/High Shelf, Low/High Cut, Notch, Band Pass, Tilt Shelf, Flat Tilt. Cut slopes 6–96 dB/oct. Per-band Stereo/Left/Right/Mid/Side. Zero Latency / Natural Phase / Linear Phase. Output gain | Known |
| | Dynamic EQ per band: range, plus a threshold that can run on Auto (Pro-Q 3 and 4) | Confirmed |
| | Per-band dynamic attack/release is Pro-Q 4 only (50% = auto): optional | Confirmed |
| **Pro-C 2/3** | Styles in both versions: Clean, Classic, Opto, Vocal, Mastering, Bus, Punch, Pumping | Confirmed |
| | Pro-C 3-only styles (Versatile, Smooth, Vari-Mu, Op-El, Upward, TTM): optional | Confirmed |
| | Knee 0–72 dB · Attack 0.005–250 ms · Lookahead 0–20 ms · Hold 0–500 ms · Range · Dry gain · external side chain and side-chain EQ (Expert mode) | Confirmed |
| | Threshold, Ratio, Release (+ Auto), makeup Gain | Known |
| **Pro-DS** | Single Vocal / Allround. Wide Band / Split Band (linear phase). Threshold (down to −INF in Single Vocal), Range, detection HP/LP filters, Lookahead up to 15 ms, stereo link with mid/side | Confirmed |
| **Pro-L 2** | Styles: Transparent, Punchy, Dynamic, Allround, Aggressive, Modern, Safe, Bus | Confirmed |
| | Gain, Output Level (ceiling), Lookahead, Attack, Release, True Peak | Known |
| **Pro-G** | Styles: Classic, Clean, Vocal, Guitar, Upward, plus Ducking. Threshold, Ratio (1:1 to ∞:1, acting as a gate above about 5:1), Range (the maximum attenuation), Attack, Hold, Release, Knee, Lookahead | Confirmed |
| **Pro-MB** | Up to 6 bands. Downward and upward compression and expansion | Confirmed |
| | Range sign: in Compress mode, a negative Range compresses downward (normal) and a positive Range compresses upward. Sheets only use negative Range | Confirmed |
| | Attack and Release read 0–100% (program-dependent), not ms | Confirmed |
| **Saturn 2** | 28 styles. Names confirmed: Warm Tape, Clean Tube, Warm Tube · "Subtle" versions of Tape, Tube and Saturation · Transformer: Subtle, Gentle, Warm · Amp: British Rock, British Pop, American Tweed, American Plexi · FX: Foldback, Breakdown | Confirmed |
| | Per band: Drive in % (output compensates automatically as Drive rises), Feedback, Dynamics (left = gate/expand, right = compress), Tone (bass/mid/treble/presence), Mix in %, Level (−inf to +36 dB). Up to 6 bands | Confirmed |
| **Timeless 3** | One Delay Time knob (5 ms–5 s) sets both sides. With Delay Sync on, it becomes Delay Offset, 50–200% of the synced value. The Delay Time Pan ring lengthens the left or the right side, up to 400%. Tape / Stretch time modes. Ping Pong (start L or R). Feedback, Cross Feedback Mix, feedback invert. Filters in the delay path, which shape the first repeat too. Feedback FX: Drive, Lo-Fi, Diffuse, Dynamics, Pitch. Output: a Mix slider (100% on a return, since there is no Dry control), a Wet Level knob and a Stereo Width slider. Modulation, including an envelope follower whose attack and release you set by dragging its envelope dots. Ducking = the envelope follower pulling the Wet Level down | Confirmed |
| **Pro-R 2** | Space (stepless room model + decay time, from about 0.2 s up to about 10 s). Decay Rate 25–400% of the Space's decay. Style: Modern, Vintage or Plate. Predelay 0–500 ms with sync. Character, Distance, Thickness and Mix in %, Brightness in ±%. Stereo Width runs from 0% (mono) through 50% (true stereo, full width) and 100% (dual mono) to 120% (sides boosted). The sheets stay at 50% or below. Ducking (a range knob that triggers on the plugin's own input), Auto Gate, Freeze | Confirmed |
| | Ducking's unit. Whether every version reaches 400% Decay Rate (one source says 50–200%). Sheets note a 200% fallback | Check |
| | Decay-rate EQ, post EQ | Known |

### FL Studio

| Feature | Notes | Status |
|---|---|---|
| Mixer slots | 10 effect slots per track | Known |
| Routes | Post-fader. The send knob appears above a route's switch once it's on, and reads 0–100%. Its dB mapping wasn't confirmed, so the sheets set return levels with faders, which read in dB (D21) | Confirmed |
| Fruity Send | A pre-fader tap from inside a track's effect stack | Confirmed |
| Sidechain to this track | Makes a connection with its audio send at zero, so it only carries a sidechain key | Confirmed |
| Sidechain into VST plugins | Plugin wrapper settings (cog, top-left) → map the sidechain input. In the FabFilter plugin, set the side chain to External | Confirmed (panel wording: Check) |
| Stereo separation knob | Center = off. Turn right to merge to mono | Confirmed |
| Plugin delay compensation | Automatic mode in the mixer menu. Covers sends and wet/dry paths | Confirmed (menu wording: Check) |
| Audio clips | Channel Settings → Precomputed effects → Normalize (peaks to 0 dB). Channel volume knob in the Channel Rack | Confirmed |
| Pitcher | MIDI modes: MIDI (the note name sets the pitch, kept in the voice's own octave), Octaves (the note and its octave both come from the MIDI note) and Harmonize (up to 4 notes). The Port display appears at the bottom left once MIDI is on. Speed, a Formant switch and Gender knob, key/scale, and a low-frequency detection setting (about 80 Hz for lower voices, 110 Hz for higher) | Confirmed |
| NewTone | Detects and edits notes, and exports them as a MIDI score to a channel | Confirmed |
| Vintage Chorus | Juno-6 chorus. Modes I / II (Shift+click for I+II), Mix (wet/dry), Time 1 / Time 2, Feedback, H Pass on the wet signal, LR Phase, Invert Wet | Confirmed |
| Automation clips | Mixer controls: right-click → Create automation clip. Plugin controls: move the control, then Tools › Last tweaked › Create automation clip | Confirmed |

### To confirm on screen

Step 4 re-checked this list and confirmed six items: Saturn 2's style labels, Auto-Tune's Retune Speed range, Pro-MB's Range sign and time units, Pro-R 2's style names and Vintage Chorus's Mix control. These are still open:
- The ends of Auto-Tune Artist's Throat range (the sheets only use 100 and 120)
- FL's wording for the sidechain wrapper panel and the PDC menu
- Pro-R 2's Ducking unit and its maximum Decay Rate (the sheets note a fallback)
- The scales on Pitcher's Speed and Gender knobs (the sheets describe positions, not numbers)

---

## 2 · FL routing template

Every preset is built on this map. A preset only adds the parallel tracks and returns it needs.

```
lead clips ─► VOX IN ─► LEAD ─────────► VOX BUS ─► VOX GROUP ─► Master
                │        │                 ▲           ▲
                └────────┴─► PAR tracks ───┤           │
double L ─► DBL IN L ─┐                    │           │
double R ─► DBL IN R ─┴─► DBL ─────────────┘           │
LEAD / DBL sends ─► FX returns ────────────────────────┘
```

| Track | Job | Gets audio from | Routes to | Slots |
|---|---|---|---|---|
| VOX IN | Tune and split. Every layer made from the lead starts here | Lead audio clips | LEAD and any PAR track fed before the character chain. Never Master | 3, fixed (D13) |
| LEAD | The character chain | VOX IN | VOX BUS, any PAR track fed after the character chain, and post-fader sends to FX | All 10 |
| DBL IN L / DBL IN R | Tune each double on its own and pan it | One side's double clips | DBL | 3 each, fixed (D19) |
| DBL | The doubles' character chain | DBL IN L and DBL IN R | VOX BUS, plus sends to FX | Up to 10 |
| PAR · *name* | Parallel layers (demon, harmonies, crunch) | VOX IN or LEAD, per sheet | VOX BUS | As needed |
| FX · *name* | Delay, reverb and throw returns | Sends from LEAD (and DBL where a sheet says) | VOX GROUP (D14) | As needed |
| VOX BUS | Glue for the dry layers | LEAD, DBL, PAR | VOX GROUP | 1–3 |
| VOX GROUP | One fader for the whole vocal | VOX BUS and FX | Master | 0–1 |

### Wiring it

1. Put the vocal block on consecutive free inserts, in the table's order, with these names.
2. In the Channel Rack, point every lead audio clip channel to VOX IN, left doubles to DBL IN L and right doubles to DBL IN R. With a single double, use DBL IN L only.
3. Select VOX IN, right-click the route switch under LEAD, and choose **Route to this track only**. That removes its Master route. Then left-click the switch under each PAR track it feeds.
4. Route LEAD to VOX BUS with **Route to this track only**, then left-click the switch under each PAR track fed from LEAD.
5. Select DBL IN L, right-click the switch under DBL and choose **Route to this track only**. Repeat for DBL IN R. Pan them with their own mixer pan knobs. A single double stays centered.
6. Use **Route to this track only** for DBL and PAR → VOX BUS, FX → VOX GROUP, and VOX BUS → VOX GROUP. VOX GROUP keeps its Master route.
7. Add sends last, because **Route to this track only** clears a track's other routes. Select LEAD and left-click the switch under each FX track, then set the level on the knob above it. Do the same for DBL and for any PAR track whose Track map lists sends. Routes are post-fader, so moving a track's fader moves its sends too. Sidechain-only keys also go in now (see Ducking a return).
8. Leave VOX IN's fader at its default. Everything downstream follows it.

### Ducking a return

Most returns duck themselves (D15). Pro-R 2 has a Ducking knob, and Timeless 3 can pull its own Wet Level down with its envelope follower. Both react to the signal arriving at the return, so they need no extra routing.

To set up Timeless 3's ducking:
1. In the modulation section, add an Envelope Follower source.
2. Drag the source's drag button onto the Wet Level knob. That creates a modulation slot.
3. In the slot, click the +/- button so the follower pulls the Wet Level down. Then, while the vocal plays, raise the slot's Level slider until the Wet Level knob dips by about the sheet's depth (for example −12 dB).
4. Drag the dots in the follower's envelope display to set attack short and release to the sheet's value.

When a sheet uses Pro-C ducking instead (after Wiring it, step 7):
1. Select VOX IN, right-click the switch under the FX track, and choose **Sidechain to this track**.
2. On that FX track, open Pro-C, click the wrapper cog (top-left) and map the sidechain input to VOX IN.
3. In Pro-C's Expert mode, set the side chain to External.
4. Turn Pro-C's Auto Gain off and leave Gain at 0 dB. A ducker gets no makeup.

The key comes from VOX IN because LEAD already sends audio to the return, and "Sidechain to this track" works by zeroing a connection's audio send.

### Delay compensation

- Keep FL's plugin delay compensation on **Automatic** (mixer menu). Never add manual PDC to a vocal track, or the delay doubles up.
- Parallel layers only meet at VOX BUS, and nothing latency-heavy goes straight to Master. This follows Image-Line's own advice for parallel paths.
- Parallel copies at the same pitch as the lead connect through mixer routes only, never Fruity Send. Its tap sits mid-chain, ahead of the source track's later plugins, which makes the two paths harder to keep locked.
- Where a plugin offers a latency choice on a parallel track, pick zero latency (D18).

### Slot budget

- **VOX IN:** three fixed slots: rumble cut → gentle expander → Auto-Tune Artist (D13).
- **LEAD:** all 10 slots. The default order of jobs is below. A sheet can move a job, and says why when it does.

| Slot | Job | Typical tool |
|---|---|---|
| 1 | Corrective EQ: low cut, box, resonances | Pro-Q (dynamic bands) |
| 2 | Compressor 1: peak catcher | Pro-C |
| 3 | Tone EQ: body support, shape | Pro-Q |
| 4 | Saturation: density and harmonics | Saturn 2 |
| 5 | Compressor 2: leveler | Pro-C |
| 6 | Presence and air (or darkening) | Fresh Air / Pro-Q |
| 7 | De-esser, after the brightness | Pro-DS |
| 8 | Dynamic control: harshness, yells | Pro-Q dynamic / Pro-MB |
| 9 | Polish EQ: final tilt, placement | Pro-Q |
| 10 | Peak control | Pro-L 2 |

- **DBL IN L / DBL IN R:** three fixed slots each: rumble cut → gentle expander → Auto-Tune Artist with the lead's key, scale and retune (D19).
- **DBL:** the doubles' character chain. Up to 10 slots, using only what it needs (see 5.2).
- **PAR and FX:** as many slots as each needs. A return that ducks with Pro-C puts it last (see Ducking a return).
- **VOX BUS:** 1–3 slots of glue. **VOX GROUP:** empty unless a sheet needs one slot.

### Names and colors

- **Names:** VOX IN · LEAD · DBL IN L / DBL IN R · DBL · PAR · DEMON / OCT / OCT UP / 3RD / CRUNCH · FX · DELAY / PLATE / HALL / VERB / ROOM / SLAP / THROW · VOX BUS · VOX GROUP
- **Colors:** VOX IN grey. LEAD, DBL and PAR in one color you pick per preset (DBL lighter, PAR darker). FX teal. Buses white.

---

## 3 · Source profile

**The voice:** between mid and high, leans thin (Q6, Q8).
**The mic:** the LCT 440 PURE is flat through the lows and mids, then rises gently from about 1.25 kHz, with a 3.5 dB peak at 4 kHz and a 5 dB peak at 13 kHz.
**The room:** DIY-treated bedroom (Q7).

What that means for every chain:
1. **The mic already supplies presence and air.** Brightness moves mostly shape and control rather than boost.
2. **The real need is body and density.** That comes from three things working together: EQ support in the body zone, harmonic saturation, and compression. The low cut stays conservative.
3. **The room adds some low-mid boxiness and short reflections, not long tails.** Box gets a dynamic cut. Breaths and room between phrases get tamed gently.

### Zone map

| Zone | Range | Policy |
|---|---|---|
| Rumble | Below 60 Hz | Cut on VOX IN at 60 Hz, 12 dB/oct. Nothing vocal lives here |
| Low cut | 70–100 Hz | Lead low cut at 75–90 Hz, 12–18 dB/oct. Never above 100 Hz on the lead |
| Body | 150–300 Hz | Broad support of +1.5 to +3 dB where the voice's weight peaks, usually 180–250 Hz, plus saturation. To find it, sweep a narrow boost through 150–300 Hz and stop where it gains chest without boom |
| Box | 300–500 Hz | Dynamic cut of −2 to −4 dB, only when it builds (close takes, low notes) |
| Honk | 800 Hz–1.5 kHz | Leave it, because a nasal edge suits this lane. Dynamic −1 to −2 dB only if a note pokes out |
| Presence | 2–5 kHz | The mic already adds about 3.5 dB at 4 kHz. Add sparingly, and control 3–5 kHz dynamically on yells |
| Sibilance | 5–10 kHz | Pro-DS detection lives here. Mid-high voices usually center around 6–8 kHz. Find the exact spot with Pro-DS's audition |
| Air | 10–16 kHz | The mic already adds about 5 dB at 13 kHz. Use Fresh Air or a high shelf in moderation, with the de-esser after it |

**Auto-Tune input type:** Alto/Tenor.

**Breath and room:** a gentle expander on VOX IN, with no more than 6 dB of reduction and never a hard gate. Breaths get reduced, not removed, because some of that energy belongs in this style. Obvious noises like chair creaks get cut by hand.

---

## 4 · Gain and dynamics standard

### Input level

- **Target:** the loudest lines peak around **−10 dBFS** on VOX IN's meter, which puts the average near −18 dBFS. Every threshold and drive amount in the sheets assumes this, so the presets behave the same from song to song.
- **How:** use the volume knobs on the audio clip channels in the Channel Rack. Normalize (Channel Settings → Precomputed effects) only on clips that hold a whole section. Never normalize short phrase clips one by one, because that flattens the contrast between quiet and loud lines (D17).

### Between stages

- Level-match each plugin so its output lands where its input was, using the plugin's own output control: Pro-Q Output, Pro-C Gain, Saturn Level, Fresh Air Trim, Pro-L 2 Gain. The exception is when a sheet says otherwise.
- Keep peaks between stages around −12 to −6 dBFS. Only the LEAD's final limiter works up to its ceiling.

### Compression budget (LEAD, on the loudest lines)

| Stage | Job | Gain reduction |
|---|---|---|
| Compressor 1 | Peak catcher, fast | 3–6 dB on peaks |
| Saturation | Density, soft peak rounding | About 1–2 dB, effective |
| Compressor 2 | Leveler, slower | 2–4 dB, steady |
| Pro-L 2 | Peak control | 1–3 dB, peaks only |
| **Total** | | **About 8–14 dB, with no single stage over 6 dB** |

Each sheet sets its own total within this range. Smoother presets sit low and grittier ones sit high.

### Blend references

Levels here are measured against LEAD at VOX BUS, on the peak meters and by ear. Heavily compressed layers (the demon, the ghost, the crunch) sound closer than their peaks suggest, so when the meter and the test disagree, the test wins.

| Layer | Level vs. LEAD | Test |
|---|---|---|
| Ghost | −18 to −12 dB | Muting it makes the lead feel smaller. Unmuted, you don't hear a second voice |
| Support (harmonies, crunch) | −12 to −6 dB | It adds size or edge without pulling focus |
| Doubles (DBL) | −10 to −6 dB | The lead still owns the center |

### Ceilings and headroom

- **Pro-L 2 at the end of LEAD:** output ceiling −3 dBFS. Raise its Gain until the loudest lines show 1–3 dB of reduction. Expect about +8 to +13 dB: every stage before it is level-matched by loudness, which leaves peaks around −14 to −12 dBFS by the time they arrive. The doubles end with the same stage (D23), so their fader offsets hold.
- **VOX BUS:** glue only, no limiter.
- **VOX GROUP:** with the beat at its usual level, set the fader where the vocal sits right. Its peaks should stay at or below −6 dBFS so the master has room.

---

## 5 · Shared conventions

### 5.1 · Auto-Tune base

Every preset's VOX IN starts from this and changes only what its sheet lists.

| Control | Base | Why |
|---|---|---|
| Input Type | Alto/Tenor | Fits a mid-high voice |
| Key / Scale | The song's key, on VOX IN and both DBL IN tracks | Per-song setup |
| Algorithm | Modern (Classic Mode off) | Classic turns off Flex-Tune, Formant, Throat and Transpose (D16) |
| Retune Speed | Hard 0–5 · Fast 10–20 · Medium 25–40 | Set by each preset's tune style |
| Humanize | 10–30 | Held notes breathe instead of freezing |
| Flex-Tune | 10–30 | Rapped syllables pass more naturally while sung notes still snap. Hard presets sit at the low end |
| Natural Vibrato | 0 | Leaves the voice's own vibrato alone |
| Formant | Off on VOX IN | Only transposing tracks turn it on |
| Throat | 100 | Neutral unless a sheet says otherwise |
| Transpose | 0 on VOX IN | Only transposing tracks use it |
| Tracking | Default | Adjust only if detection glitches on raspy or breathy parts |

**Transposing tracks** (the demon and the octave layers) are different. They run on Chromatic with minimal correction (high Flex-Tune) and Formant on. Their input is already tuned, so they only shift pitch, and they never need the song's key (D20).

### 5.2 · Doubles baseline

DBL mirrors the lead's job at lower focus:
- **Front end (DBL IN L / DBL IN R):** the same three jobs as VOX IN, one track per double: rumble cut, gentle expander, then Auto-Tune with the lead's exact key, scale and retune. Each double gets its own Auto-Tune because it only follows one voice at a time (D19). Panning happens on these tracks.
- **Low cut:** 100–140 Hz, higher than the lead. The lead carries the body, and stacked low-mids would blur it.
- **Tone:** 1–3 dB less at 3–5 kHz and above 10 kHz than the lead. Fresh Air lower or off.
- **De-essing:** harder than the lead (deeper Pro-DS range), because S's stack up across takes.
- **Compression:** tighter than the lead. A steady level blends better.
- **Peak control:** the last slot is Pro-L 2 at −3 dBFS, like the lead, so the DBL fader's offset means what it says (D23).
- **Pan:** a pair at L/R 60–90, set per sheet. A single double uses DBL IN L, centered, with DBL's fader 2–3 dB lower than the sheet's.
- **Sends:** the levels each sheet lists. DBL's fader puts them 6–10 dB below the lead's, since sends are post-fader. Lead-only effects (a slap, throws, the demon's room) skip the doubles.
- **Level:** 6–10 dB under LEAD.
- Doubles never feed PAR tracks.

### 5.3 · Key-move format

Each sheet lists 2–4 moves in this form (D9). Draw them only after the blend is final (the §4 tests). Once a control has an automation clip, the clip owns it, so later level changes go into the clip, not the fader (D24).
- For mixer faders and send knobs, right-click the control and choose **Create automation clip**.
- For a control inside a plugin (Fresh Air, Pro-R 2, Pro-Q, Pro-L 2), move it once, then use **Tools › Last tweaked › Create automation clip**. If that doesn't catch it, find the plugin under Browser › Current project and right-click the parameter there.
- Keep one clip per control. If two moves touch the same control, draw them in the same clip.
- In fixes, "X's automation clip" means the clip you drew for that control: move every point by the amount given. If you haven't drawn one, move the control itself.
- The From values are the sheet's starting levels. If your blend moved a fader, shift the whole move by the same amount (a fader blended 2 dB lower runs the move 2 dB lower).

| # | Move | Track › Parameter | From → To | When | Why |
|---|---|---|---|---|---|
| e.g. | Throw | LEAD › send to FX · THROW | 0% → 100% → 0% | Last word of bar 8 | Lifts the line ending |

### 5.4 · Mono and translation test

Run it once per preset after dialing in, then once per song.

| Check | How | Pass |
|---|---|---|
| Mono | Turn the master track's stereo separation knob fully right, then back to center afterward | The lead doesn't dip or change tone, doubles and returns don't vanish or go hollow, and nothing swirls |
| Quiet | Monitor very low | Every word still comes through |
| Small speaker | Phone speaker or earbuds | Presence intact, S's not piercing, body still there |
| Loud | Car or monitors at volume | No boom in the low-mids, no harsh edge |
| Headphones | Good headphones | Returns and doubles support the lead without distracting |

### 5.5 · Chain-sheet template

Every preset sheet uses these sections, in this order:
1. **Header:** identity and placement (D6)
2. **Per-song setup** (D11)
3. **Sound targets and upgrades**
4. **Track map:** the template tracks it uses, routes, send levels and starting faders
5. **VOX IN:** the three slots, with this preset's Auto-Tune settings
6. **LEAD:** all 10 slots as Slot · Plugin · Settings · Why
7. **Parallel tracks**
8. **FX returns**
9. **Buses**
10. **DBL:** the DBL IN tracks and the DBL chain
11. **Key moves**
12. **Ear checks:** the build order, with one line per stage on what you should hear change (§5.7)
13. **Translation notes:** the §5.4 checks for this preset, each with what to watch for and the fix. The biggest risk is marked

### 5.6 · Reading the settings

- **GR** means gain reduction on the loudest lines. Each threshold is a starting point for the GR written next to it.
- **Level-match** means setting the plugin's output so bypassing it doesn't change loudness.
- **Pro-Q** runs in Zero Latency, its default mode, on every track (D18). A band with no Q listed keeps the default Q.
- **Dynamic −3 dB** on a Pro-Q band means Gain 0 dB with the band's dynamic range at −3 dB. The band stays flat and cuts up to 3 dB only when the level crosses its threshold.
- **Dynamic EQ bands** use threshold Auto. If your Pro-Q has no Auto, set the threshold so the band only moves on the loudest lines.
- **Pro-C:** Auto Gain stays off everywhere, and makeup comes from the Gain knob. "Release Auto" means the Auto release button on, with the Release knob at its default.
- **Faders** are starting values. The blend tests in §4 fine-tune them for your voice.
- **Sends** sit at 100% unless a sheet says otherwise, and return faders set the wet level (D21).
- **EQ on parallel tracks and returns** stays at Output 0 dB. Its cuts are part of each sheet's level math, so don't level-match it (D24).
- **LEAD's fader stays at 0 dB.** PAR tracks fed from LEAD are post-fader, so moving it would change how they gate, drive and compress. Balance with the other faders, and set the overall vocal level on VOX GROUP (D24).
- **Pro-R 2 Ducking** values are in dB. If your knob reads in %, raise it until the tails drop clearly under the words and bloom in the gaps.
- **Ramps** in key moves are the automation clip's shape: "1-beat ramp" means the move takes one beat to get there.
- **Wet 2/5** and similar scores in Sound targets are the Phase 1 meters (0 = dry, 5 = drenched). They describe the overall space, not a knob.
- **Optional extras** from Pro-Q 4 and Pro-C 3 are never needed (D1).

### 5.7 · Building and ear-checking

Each sheet's Ear checks table is its build order:
1. Set every fader and pan from the sheet's Track map. Then mute every track the table hasn't reached yet (PAR, FX, DBL IN L / R and DBL), and unmute each one at its own stage. Park tracks with mutes, not solo: depending on your settings, un-soloing in FL can unmute every track.
2. Loop 8 bars that hold both rap and melody, with the beat playing quietly underneath.
3. Add one stage and set it from the sheet.
4. Switch it off and on to hear what it adds. Use the slot's green switch for a plugin on LEAD, DBL or a PAR track. For a return's reverb or delay, use the return's mute instead: bypassing a 100%-wet plugin sends the dry vocal through.
5. Listen for the change the table names. If you don't hear it, re-check that stage before adding the next one.

Most stages are level-matched (§4), so the change should be in tone, control or space, not loudness. Three kinds change level on purpose: the Pro-L 2 stages, EQ on parallel tracks and returns (Output 0 dB, D24), and duckers. If any other stage gets louder, fix its output first.

The blend and the key moves come last, in that order (D24).

---

## Sources

**Auto-Tune Artist:**
- [Antares: Introduction to AutoTune Artist](https://www.antarestech.com/blog/tutorial-introduction-to-auto-tune-artist)
- [Antares: AutoTune Best Practices](https://help.antarestech.com/hc/en-us/articles/42858099043092-AutoTune-Best-Practices)
- [Auto-Tune Artist User Guide (PDF)](https://antares-web-frontend.sfo3.cdn.digitaloceanspaces.com/documentation/pdfs/Auto-Tune_Artist_Manual.pdf)
- [Auto-Tune Pro X User Guide 10.0 (PDF)](https://antares-web-frontend.sfo3.cdn.digitaloceanspaces.com/documentation/pdfs/Auto-Tune_Pro_X_User_Guide_10.0.pdf)
- [Antares: Throat](https://www.antarestech.com/product/throat/)
- [Sweetwater: Auto-Tune Quickstart](https://www.sweetwater.com/sweetcare/articles/auto-tune-quickstart-guide/)

**Fresh Air:**
- [Slate Digital Docs: Fresh Air](https://docs.slatedigital.com/FreshAir/Fresh%20Air.html)
- [bchillmix: Fresh Air vs. stock exciter](https://bchillmix.com/blogs/news/fresh-air-vs-stock-exciter-for-brighter-vocals)

**FabFilter:**
- [FabFilter releases Pro-C 3](https://www.fabfilter.com/news/1768435200/fabfilter-releases-pro-c-3-compressor-plug-in)
- [Pro-C 3 Help: Style and character](https://www.fabfilter.com/help/pro-c/using/styleandcharacter)
- [MusicTech: Pro-C 3](https://musictech.com/news/gear/fabfilter-pro-c-3/)
- [Pro-C 2 manual (PDF)](https://www.fabfilter.com/downloads/pdf/help/ffproc2-manual.pdf)
- [Pro-Q 4 Help: Dynamic EQ](https://www.fabfilter.com/help/pro-q/using/dynamic-eq)
- [Pro-DS Help: Basic controls](https://www.fabfilter.com/help/pro-ds/using/basiccontrols)
- [Production Expert: Pro-L 2 styles](https://www.production-expert.com/production-expert-1/fabfilter-pro-l-2-for-music-mastering-in-2026-which-style-and-why-it-matters)
- [Pro-G Help: Time controls, Style and Knee](https://www.fabfilter.com/help/pro-g/using/timecontrols)
- [Pro-MB Help: Basic band controls](https://www.fabfilter.com/help/pro-mb/using/basicbandcontrols)
- [Saturn 2 Help: Band controls](https://www.fabfilter.com/help/saturn/using/bandcontrols)
- [FabFilter releases Saturn 2](https://www.fabfilter.com/press/1589878800/fabfilter-releases-fabfilter-saturn-2-distortion-and-saturation-plug-in)
- [Production Expert: Saturn 2](https://www.production-expert.com/production-expert-1/2020/5/19/saturn-2-from-fabfilter-new-version-offers-everything-for-saturation-and-distortion-from-subtle-to-wild)
- [Sage Audio: How to use Saturn 2](https://www.sageaudio.com/articles/how-to-use-fabfilter-saturn-2)
- [Timeless 3 Help: Delay controls](https://www.fabfilter.com/help/timeless/using/delaycontrols)
- [Timeless 3 Help: Envelope follower](https://www.fabfilter.com/help/timeless/using/ef)
- [Timeless 3 Help: Drag-and-drop modulation slots](https://www.fabfilter.com/help/timeless/using/modulationslots)
- [Music Connection: Timeless 3](https://www.musicconnection.com/new-toys-fabfilter-timeless-3-delay-plugin/)
- [Pro-R 2 Help: Main controls](https://www.fabfilter.com/help/pro-r/using/maincontrols)
- [Production Expert: Pro-R 2 first look](https://www.production-expert.com/production-expert-1/new-features-fabfilter-pro-r-2-first-look)

**FL Studio:**
- [Mixer Explained](https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/mixer.htm)
- [Automation Clips](https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/playlist_automationclip.htm)
- [Fruity Send](https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Fruity%20Send.htm)
- [Ringmod: Sidechain routing guide](https://ringmodsidechain.com/tutorials/sidechain-routing-in-fl-studio-complete-guide)
- [MusicProductionWiki: How to sidechain in FL Studio](https://musicproductionwiki.com/articles/how-to-sidechain-in-fl-studio)
- [Black Ghost Audio: Sidechain with Pro-C 2](https://www.blackghostaudio.com/blog/how-to-apply-sidechain-compression-using-fabfilters-pro-c-2)
- [Image-Line: PDC made simple](https://www.image-line.com/fl-studio-news/plugin-delay-compensation-pdc-made-simple)
- [Image-Line forum: Automatic PDC](https://forum.image-line.com/viewtopic.php?t=9549)
- [Image-Line forum: Stereo separation knob](https://forum.image-line.com/viewtopic.php?t=270585)
- [Pitcher](https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Pitcher.htm)
- [Vintage Chorus](https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Vintage%20Chorus.htm)
- [ask.video: NewTone](https://ask.video/article/audio-software/audio-editing-pitch-correction-using-fl-studios-newtone-)
- [BarrettArtists: Normalizing in FL Studio](https://www.barrettartists.com/fl-studio-how-to-normalize-audio/)

**Lewitt LCT 440 PURE:**
- [RecordingHacks](https://recordinghacks.com/microphones/Lewitt/LCT-440-Pure)
- [Sound On Sound review](https://www.soundonsound.com/reviews/lewitt-lct-440-pure)
- [Recording Magazine review](https://www.recordingmag.com/resources/featured-reviews/lewitt-lct-440-pure/)
