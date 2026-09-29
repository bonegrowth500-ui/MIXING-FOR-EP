# Phase 3: Build Plan

Builds the five presets locked in the [Phase 2 spec](phase-2-spec.md). Every step stays inside that spec. Anything the spec leaves open gets resolved by judgment and logged under [Decisions](#decisions). Q-numbers point to the spec's interview answers.

**Rhythm:** each step ends with a commit and a short report, then waits for the next cue.

**Done means:**
- every slot has a starting value and a reason
- every routing move is something FL can actually do
- every spec answer traces to where it's implemented (4A)
- an intermediate FL user can build each preset from its sheet alone (5C)

## Deliverables

All in `vocal-chains/presets/`:

| File | Contents | Written in |
|---|---|---|
| `00-foundation.md` | Routing template, source profile, gain standard, shared conventions | Step 1 |
| `02-phantom-twin.md` | Full chain sheet | Steps 2–3 |
| `04-neon-bleach.md` | Full chain sheet | Steps 2–3 |
| `11-silk-stack.md` | Full chain sheet | Steps 2–3 |
| `13-vampire-haze.md` | Full chain sheet | Steps 2–3 |
| `16-rockstar-grit.md` | Full chain sheet | Steps 2–3 |

---

## Step 1 · Ground Truth ✅

*Verify the toolkit and lock the shared foundation before any preset gets a setting.*

**1A · Manual check.** Pull the official documentation for every tool the sheets can use and record exact parameter names, ranges and modes:
- Auto-Tune Artist: input types, retune, humanize, flex-tune, formant, throat, transpose
- Fresh Air
- FabFilter: Pro-Q, Pro-C, Pro-DS, Pro-L, Pro-MB, Pro-G, Saturn, Timeless, Pro-R, Volcano
- FL stock: Pitcher, NewTone, Edison, chorus and stereo tools, send and sidechain routing, stereo separation

If a manual can't be reached, the sheets use only controls I'm certain exist, and the gap gets flagged.

**1B · FL routing template.** Design the track map all five presets build on: source track, lead, doubles, parallel tracks, returns and vocal buses. Set conventions for sends, sidechain ducking, naming, colors and slot budgets. Confirm how FL's automatic delay compensation handles split paths, so parallel layers stay phase-locked.

**1C · Source profile.** Turn Q6–8 into numeric targets:
- the low-cut, body, mud, honk, presence, sibilance and air zones
- the Auto-Tune input type
- how room tail and breaths get handled

**1D · Gain and dynamics standard.** Set:
- the input level into each chain and level targets between stages
- how total compression splits across serial stages
- reference blend levels for parallel paths
- limiter ceilings and headroom at the vocal group

**1E · Shared conventions.**
- an Auto-Tune base that holds up on both deliveries in Q13
- the doubles baseline
- the key-move format
- the mono and translation test
- the chain-sheet template

**Done when:** `00-foundation.md` is committed, and every EQ, dynamics and level decision in later steps can point back to it.

---

## Step 2 · Blueprints ✅

*Design all five signal flows on paper before dialing any numbers.*

**2A · Sound targets.** Turn each Phase 1 concept, plus its spec answers, into measurable targets: tone curve, density, space (decay and wet level), width, grit and placement. Mark exactly where a small upgrade (Q27) applies and why.

**2B · Signal flow.** For each preset, lay out the track list and a slot map for the lead (all 10 slots with a purpose). Then the doubles track, parallel tracks, returns and buses, with the reason each stage sits where it does.

**2C · Special engines.** Design each preset's hard part and check it's buildable against the 1A notes:
- Phantom Twin: the demon engine (Q17–18). Covers the feed point, transpose, formant, a gate before the distortion, and band-limiting.
- Neon Bleach: the echo bed (Q20).
- Silk Stack: the harmony engine (Q21–22), including its per-song setup.
- Vampire Haze: the throws and dark returns (Q23–24).
- Rockstar Grit: the crunch, with yell control inside the chain (Q25–26).

**2D · Cross-check matrix.** Line the five blueprints up side by side and confirm:
- no two presets drift toward the same sound
- every spec answer maps to a component
- only toolkit plugins are used
- slot counts fit
- CPU load is reasonable

**Done when:** the signal-flow section of all five sheets is committed.

---

## Step 3 · Dial-In ✅

*Write every setting, in an order where each preset builds on the last.*

**Build order:**
1. Neon Bleach: the clean reference
2. Phantom Twin: adds the parallel engine
3. Rockstar Grit: adds grit
4. Silk Stack: adds the harmony engine
5. Vampire Haze: adds the dark space

**3A · Lead chains.** Slot by slot: plugin, mode, exact starting values and a one-line reason.

**3B · Parallel, return and bus tracks.** Every engine and FX return fully specified, including sidechain ducking, return EQ and bus glue.

**3C · Doubles chains.** Tuning matched to the lead, a tone offset, tighter dynamics, pan and width, and send levels.

**3D · Key moves.** 2–4 per preset, each in the format from D9.

**3E · Per-song setup.** The short list of what changes from song to song (D11), at the top of each sheet.

**Done when:** all five sheets are complete and committed.

---

## Step 4 · Stress Test ✅

*Prove the build without ears.*

**4A · Spec trace.** Trace every answer from Q1 to Q28 to where it's implemented, then sweep for anything out of scope.

**4B · Technical audit.** Check:
- every parameter against the 1A notes
- slot counts
- sends and sidechains
- delay compensation
- version safety (D1)
- CPU load

**4C · Signal math.** Walk the gain through every path: stage levels, compression totals, parallel blend levels, limiter behavior and headroom.

**4D · Sonic logic and translation.** Check:
- rap vs. melody behavior in each preset
- enough body on a thin voice
- sibilance stacking across lead, doubles and air
- every stereo element folded to mono
- phone, car, headphone and club risks

**4E · Fidelity and distinctness.** Each preset still reads as its Phase 1 identity, the upgrades stay small, and the five stay clearly different.

**4F · Fresh-eyes review.** A separate reviewer agent checks each sheet against the spec and the 1A notes. Every confirmed issue gets fixed and re-checked.

**Done when:** every finding is resolved and a short verification log is added to this plan.

---

## Step 5 · Final Cut ✅

*Polish and ship.*

**5A · Consistency pass.** The same structure, terms, units and formatting across all sheets and the foundation.

**5B · Setup order and ear checks.** A build-order checklist per preset, with one line per stage on what you should hear change.

**5C · Cold read.** Build each preset from its sheet alone, as an intermediate FL user. Fix anything unclear or missing.

**5D · Ship.** Update the README tracker, commit, push and send the delivery summary.

**Done when:** the five presets are delivered.

---

## Decisions

Judgment calls made inside the spec where it leaves room. New ones get added as they come up.

| # | Call | Why |
|---|---|---|
| D1 | *(Refined in Step 1.)* Pro-C and Pro-Q both had recent major releases (Pro-C 3 in January 2026, Pro-Q 4 in December 2024). Their core settings only use features shared with Pro-C 2 and Pro-Q 3, and newer extras are marked optional. Every other plugin targets its current version, since none has had a new major version in over two years. | Works on whichever versions are installed, without giving up features that have been stable for years. |
| D2 | Tune once, upstream. Each preset gets a source track (VOX IN) with Auto-Tune and shared cleanup, feeding the lead and every parallel path. The lead's 10 slots hold the character chain. | Every layer carries the same tuned audio, so tuned and untuned copies can never clash. |
| D3 | Vocal buses count as part of the chain. Dry layers glue on a vocal bus, and returns join them at a vocal group. The master and mix bus stay untouched. | Parallel paths need a shared glue point. Mastering stays out of scope. |
| D4 | Doubles are built for a stereo pair (L/R), with a single-double fallback. | Covers both common ways of tracking doubles. |
| D5 | Same-pitch parallel paths avoid latency mismatches, and FL's delay compensation gets verified in 1B. | Prevents comb filtering between parallel copies of the lead. |
| D6 | Placement: Phantom Twin on top · Neon Bleach on top, most upfront · Silk Stack balanced · Vampire Haze leans into the beat · Rockstar Grit on top. | Resolves "varies per preset" from each Phase 1 concept. |
| D7 | Lead, demon and crunch paths stay mono. Width comes from doubles, harmonies and returns. Every return gets a low cut and a mono check. | Mono safety without losing width. |
| D8 | The octave down comes from Auto-Tune Artist's transpose. The 3rd up comes from Pitcher, driven by a per-song MIDI line, with NewTone as fallback. Both run as Silk Stack parallel tracks. | The most reliable way to make harmonies from the lead with this toolkit. |
| D9 | Each key move is written as track/parameter, from→to values, timing and purpose, done with FL automation clips. | Makes every move exact and repeatable. |
| D10 | Input level is set with clip gain on the audio. | Consistent levels into every chain, without using a slot. |
| D11 | Per-song setup is limited to: an input level check, the Auto-Tune key and scale, Silk Stack's harmony line, and placing the key moves. | Keeps the presets set-and-go. |
| D12 | Each sheet is complete for its song. The foundation holds only shared procedures. | One preset per song means one sheet per song. |
| D13 | VOX IN always holds exactly three slots: rumble cut → gentle expander → Auto-Tune Artist. | Covers what every branch needs and nothing more, so all branches stay pitch- and phase-locked. |
| D14 | FX returns route to VOX GROUP, not VOX BUS. | Keeps the bus glue from pumping reverb and delay tails. |
| D15 | *(Refined in Step 2.)* Returns duck themselves where the plugin can: Pro-R 2's Ducking knob, or Timeless 3's envelope follower on its Wet level. When a sheet uses Pro-C ducking instead, the key comes from VOX IN over a sidechain-only connection. | No extra routing in the common case. The VOX IN key avoids zeroing LEAD's audio send. |
| D16 | Auto-Tune runs in the Modern algorithm (Classic Mode off) unless a sheet says otherwise. | Classic turns off Flex-Tune, Formant, Throat and Transpose. |
| D17 | Levels are set with the audio clip channels' volume knobs. Only whole-section clips get normalized, never short phrase clips one by one. *(Refines D10.)* | Keeps the contrast between quiet and loud lines. |
| D18 | *(Refined in Step 2. Refines D5.)* Parallel tracks pick zero latency wherever it costs nothing audible: Pro-Q on Zero Latency, lookahead at 0. Distortion stages keep Saturn's HQ oversampling on, and FL's automatic PDC handles that latency. | Keeps parallel layers locked without making the distortion grainy. |
| D19 | Each double gets its own front-end track (DBL IN L / DBL IN R: rumble cut, expander, Auto-Tune) and is panned there. Both then feed DBL for the shared character chain. A single double uses DBL IN L, centered. | Auto-Tune follows one voice at a time. Two takes summed on one track can't each lock to the lead's notes. |
| D20 | Transposing tracks (the demon and the octave layers) run Auto-Tune on Chromatic with minimal correction and Formant on. Only VOX IN and the DBL IN tracks need the song's key. | Their input is already tuned, so they only shift pitch. Fewer places to set a key means fewer per-song mistakes. |
| D21 | Sends sit at 100% unless a sheet sets another percentage, and return faders set the wet level. Routes are post-fader, so doubles and parallel layers feed the returns less on their own. | FL's send knob reads in percent and its dB mapping isn't confirmed. Faders read in dB, so they're exact. |
| D22 | When a return's send already sits at 100%, a throw rides that return's fader instead (Phantom Twin). A return built only for throws rides its send up from 0% (Vampire Haze). | A send can't go past 100%, and a dedicated throw return stays silent until it's needed. |
| D23 | Every DBL chain ends with the same Pro-L 2 peak stage as its lead (−3 dBFS ceiling, 1–2 dB GR). | The lead's limiter lifts it about 10 dB. Without a matching stage, the doubles would sit about 18 dB under instead of 6–10. |
| D24 | Level rules that protect each sheet's math. EQ on parallel tracks and returns stays at Output 0 dB. LEAD's fader stays at 0 dB. Key moves get drawn after the blend is final, and a control with an automation clip gets changed in its clip. | The EQ cuts are counted in the fader values. PAR tracks fed from LEAD are post-fader, so LEAD's fader changes what they gate, drive and compress. An automation clip overrides its control, so blend changes made on the control afterward get lost. |

---

## Logs

### Step 2 · Blueprint cross-check (2D)

**Distinctness.** Where each preset sits:

| | Phantom Twin | Neon Bleach | Silk Stack | Vampire Haze | Rockstar Grit |
|---|---|---|---|---|---|
| Top end | Bright | Very bright (brightest) | Warm, silky | Dark (darkest) | Mid-forward bite |
| Density (total GR) | 10–12 dB | 11–13 dB | 8–10 dB (smoothest) | 9–11 dB | 12–14 dB (densest) |
| Grit | Demon only | Hidden | Warm tube | Tape and a dirty hall | Crunch (grittiest) |
| Space | Bright delay + dark room | Ducked ping-pong + plate | Lush hall | Dark hall + throws (wettest) | Slap + small room |
| Width | Medium | Wide doubles + ghost | Widest | Wide tails | Narrowest |
| Placement | On top | Most upfront | Balanced | Leans in | On top |
| Parallel layer | Octave-down demon: dark, distorted, ghost | Octave-up ghost: clean, airy, wide | 3rd up + octave down: support, chorused | None | Same-pitch amp crunch |
| Tune | Hard | Hard | Medium | Fast | Fast |

The closest pairs, and what keeps them apart:
- **Phantom Twin vs. Neon Bleach** (both hard-tuned and bright): different brightness levels, opposite ghost layers (dark distorted octave down vs. clean airy octave up), and different spaces (a 1/4 stereo delay plus a dark room vs. a ducked 1/8 ping-pong plus a plate).
- **Silk Stack vs. Vampire Haze** (both hall-driven): warm and silky vs. dark, a clean hall vs. saturated fog, harmonies vs. throws, balanced vs. leaning in.
- **Rockstar Grit vs. Phantom Twin** (both have a distorted parallel layer): same-pitch snarl vs. an octave-down ghost, narrowest vs. medium width, slap and room vs. delay and dark room.

**Spec coverage:**

| Spec | Where it lands |
|---|---|
| Q1–Q5 toolkit | Every slot uses FL stock, Auto-Tune Artist, Fresh Air or FabFilter (audited: nothing else) |
| Q6–Q8 source | Foundation §3. Every LEAD has body support (slot 3) and saturation (slot 4) |
| Q9 lead + doubles | Every sheet has LEAD, DBL IN L/R and DBL (D19) |
| Q10 mix versions | No tracking versions. Delay compensation on Automatic |
| Q11 one per song | Standalone sheets with their own returns (D12) |
| Q12 maxed out | LEAD uses 10/10 slots in all five, plus parallel and return tracks as needed |
| Q13 rap + melody | The Auto-Tune base (foundation §5.1), self-ducking beds, Silk Stack's harmonies on sung lines only, Vampire Haze's hall eases and Neon Bleach's bed dips on rap |
| Q14 placement | D6, set per sheet through presence, density and wet level |
| Q15 translation | D7 mono rules, a translation note per sheet, and the foundation §5.4 test |
| Q16 key moves | 2–3 per sheet (audited) |
| Q17–Q18 | Phantom Twin's demon engine |
| Q19–Q20 | Neon Bleach's air stages and soft bed |
| Q21–Q22 | Silk Stack's harmony engine |
| Q23–Q24 | Vampire Haze's hall, throws and dark tone |
| Q25–Q26 | Rockstar Grit's crunch engine and four-layer yell control |
| Q27 | An upgrades list in every sheet |
| Q28 | These sheets |

**Slots and CPU (audited):**

| | VOX IN | LEAD | DBL IN L/R | DBL | Parallel | Returns | VOX BUS | Auto-Tune | Pro-R 2 | Saturn 2 |
|---|---|---|---|---|---|---|---|---|---|---|
| Phantom Twin | 3 | 10 | 3 + 3 | 6 | 6 | 2 + 2 | 1 | 4 | 1 | 3 |
| Neon Bleach | 3 | 10 | 3 + 3 | 6 | 4 | 2 + 2 | 1 | 4 | 1 | 2 |
| Silk Stack | 3 | 10 | 3 + 3 | 5 | 4 + 4 | 2 | 1 | 4, plus Pitcher | 1 | 2 |
| Vampire Haze | 3 | 10 | 3 + 3 | 5 | — | 3 + 2 | 1 | 3 | 2 | 3 |
| Rockstar Grit | 3 | 10 | 3 + 3 | 5 | 5 | 2 + 2 | 1 | 3 | 1 | 3 |

No track exceeds 10 slots. The heaviest song runs four Auto-Tune instances plus Pitcher, or two Pro-R 2 instances. That's a normal load for a modern computer, and within the maxed-out scope.

### Step 4 · Verification log

**4A · Spec trace.** Every answer lands somewhere concrete:

| Spec | Where it's implemented |
|---|---|
| Q1–Q5 | Foundation §1–2. Audit: every slot uses FL stock, Auto-Tune Artist, Fresh Air or FabFilter |
| Q6–Q8 | Zone map (foundation §3), Alto/Tenor input, body support and saturation in every LEAD, box control, the gentle expander |
| Q9 | LEAD, DBL IN L/R and DBL in every sheet. No ad-lib chains |
| Q10 | No tracking or low-latency versions |
| Q11 | Standalone sheets with their own returns |
| Q12 | LEAD uses 10 of 10 slots in all five |
| Q13 | Flex-Tune/Humanize base, self-ducking beds, harmonies off on raps, hall eases, bed dips |
| Q14 | Placement per sheet (D6) |
| Q15 | Mono rules (D7), an actionable translation note per sheet, foundation §5.4 test |
| Q16 | 2–3 key moves per sheet |
| Q17–Q18 | Demon fader −15 dB under a Pro-L 2 ceiling. Transpose −12, Formant on, Throat 120 |
| Q19–Q20 | Fresh Air 25% / 55% plus a 12 kHz shelf. Ducked 1/8 ping-pong, no throws |
| Q21–Q22 | Octave via Auto-Tune and 3rd via Pitcher (or NewTone), both made from the tuned lead |
| Q23–Q24 | 2.5 s dark hall plus a near-frozen throw return. Shelf −5 dB at 8 kHz, high cut at 10 kHz |
| Q25–Q26 | British Rock crunch layer. Four-layer yell control, no second chain |
| Q27 | An upgrades list in every sheet |
| Q28 | Markdown sheets in this repo |

Out-of-scope sweep: clean. The only master-track touch is the mono test's temporary stereo-separation check.

**4B · Technical audit.** Web searches corrected five plugin facts, and the sheets now match:
- Timeless 3 ducks its Wet level, not a Mix control.
- Pro-R 2's Decay Rate runs 25–400%, and its styles are Modern, Vintage and Plate. The three returns that said "Default" now say Modern.
- Pro-MB: a positive Range compresses upward, so every band now uses a negative Range. Attack and Release read in %, so Rockstar Grit and Vampire Haze now use % values.
- Controls inside plugins get automated through Tools › Last tweaked, not a right-click. The foundation and the sheets say so.
- Also confirmed: Saturn 2's style labels (British Rock included), Auto-Tune's 0–400 Retune range and Vintage Chorus's Mix control.

Slots, sends, sidechains and delay compensation all check out. Updated load:

| | VOX IN | LEAD | DBL IN L/R | DBL | Parallel | Returns | VOX BUS | Auto-Tune | Pro-R 2 | Saturn 2 |
|---|---|---|---|---|---|---|---|---|---|---|
| Phantom Twin | 3 | 10 | 3 + 3 | 7 | 6 | 3 + 2 | 1 | 4 | 1 | 3 |
| Neon Bleach | 3 | 10 | 3 + 3 | 7 | 4 | 2 + 3 | 1 | 4 | 1 | 2 |
| Silk Stack | 3 | 10 | 3 + 3 | 6 | 4 + 4 | 2 | 1 | 4, plus Pitcher | 1 | 2 |
| Vampire Haze | 3 | 10 | 3 + 3 | 6 | — | 3 + 3 | 1 | 3 | 2 | 3 |
| Rockstar Grit | 3 | 10 | 3 + 3 | 7 | 5 | 2 + 2 | 1 | 3 | 1 | 3 |

**4C · Signal math.** Four real errors, all fixed:
- **Lead limiter gain.** Loudness-matched stages leave peaks around −14 to −12 dBFS, so every LEAD Pro-L 2 now starts near +10 dB (foundation §4 expects +8 to +13).
- **Doubles level.** Without a matching limiter, the doubles would have sat about 18 dB under the lead. Every DBL chain now ends with Pro-L 2 (D23).
- **Parallel EQ losses.** High-pass trims weren't counted in the fader values. Every level line now counts them, and parallel and return EQ stays at Output 0 dB (D24).
- **Gate thresholds.** A −45 dB expander sat below breath level, so all five VOX INs now use −35 dB. The demon gate is −35 dB and the crunch gate −24 dB, set for the level each one is fed.

**4D · Sonic logic and translation.** Sibilance on bright returns gets a de-esser (Neon Bleach's plate, Phantom Twin's delay). Boosts that came after a de-esser moved in front of it (Rockstar Grit). Gates guard every distortion stage, including Rockstar Grit's amp-driven doubles. Every translation note now ends in a check and a fix instead of "Step 4 checks it."

**4E · Fidelity and distinctness.** All five still match their Phase 1 identities and Step 2 positions. Neon Bleach keeps the most presence, Vampire Haze the darkest top, Silk Stack the most width and Rockstar Grit the most density.

**4F · Fresh-eyes review.** Five reviewer agents, one per sheet. Every finding was checked against the spec, the 1A notes or a search, and the confirmed ones were applied:
- **Phantom Twin:** body bell +2.5 dB (nets +2 after slot 9), demon compressor makeup about +5–6 dB, a de-esser ahead of the delay, a duplicate delay high-pass removed, the demon room's width named in the notes, and moves drawn after the blend (D24).
- **Neon Bleach:** plate de-esser, re-leveled octave-up ghost and delay, key-move values matched to the new faders.
- **Silk Stack:** a full 3rd-line procedure (tuned stem from bar 1, cleanup before transposing, the harmonic-minor exception), a fallback that keeps its own channel and adds a Pro-L 2 stage, harmonies panned L35 / R35, Pitcher at half speed.
- **Vampire Haze:** low-mid control on the lead and the hall, a 10 kHz high cut, and throws that duck and fade out.
- **Rockstar Grit:** softer crunch gate and high-pass, re-leveled crunch moves in one clip, LEAD slots 7–9 reordered, a gate on the doubles, and a reason the doubles skip the slap.

Audit script, final run: structure, toolkit, value ranges, negative Pro-MB Range, Pro-MB times in %, Pro-R 2 styles, DBL ending in Pro-L 2, decision refs, links and anchors all pass.

Still open, and none of them blocks a build: the ends of the Throat range (the sheets use only 100 and 120), some FL panel wording, Pro-R 2's Ducking unit and maximum Decay Rate (both have a fallback in the sheets), and the scales on Pitcher's knobs (the sheets give positions).

### Step 5 · Final cut log

**5A · Consistency pass.** One field order per plugin type in every sheet:
- Pro-L 2: style, Gain, Output, Lookahead.
- Pro-DS: mode, band mode, threshold with its target, Range, detection, Lookahead. The doubles' de-essers now name a target (5–8 dB on S's) and a lookahead too.
- Auto-Tune: transposing tracks list their controls in the same order as VOX IN, with Natural Vibrato 0 and Classic Mode off.
- Timeless 3: sync and time first, then the time mode, the filters, Mix and Wet Level. Ducking points to the foundation's how-to.
- Pro-Q: bands in frequency order, and every Side-only cut has a slope. Zero Latency and the default Q are stated once in the reading guide (foundation §5.6), and every parallel or return EQ row shows Output 0 dB (D24).

Also standardized: the per-song key-move step, the VOX IN expander's reason, the density checks (with the slots they add up), and the doubles' send lines. Two doubled low cuts came out: Neon Bleach's delay and Rockstar Grit's slap already high-pass inside Timeless, the same fix Phantom Twin got in Step 4. Rockstar Grit's slap return drops to one slot.

**5B · Ear checks.** Every sheet now has a build-order table of 22–24 stages, one line each on what you should hear change. The shared routine is foundation §5.7:
- Park unbuilt tracks with mutes.
- Loop 8 bars of rap and melody.
- Add one stage, switch it off and on, and listen for the change the table names.

Translation notes became check / watch for / fix tables in the §5.4 order, with each preset's biggest risk marked.

**5C · Cold read.** Five fresh reviewers each built one preset from its sheet and the foundation, as an intermediate FL user. Every finding was checked against FabFilter's and Image-Line's documentation through web search before it was fixed. The four blockers:
- **Timeless 3's controls.** It has one Delay Time knob with a pan ring, a Mix slider and a Wet Level knob. It has no left and right time knobs and no Dry control. Every delay row now uses the real controls, with Mix at 100% on returns. Phantom Twin gets its 1/4 and dotted 1/8 from sync 1/4, Delay Offset 75%, and the left side lengthened to 133%.
- **Pro-R 2's width scale.** Stereo Width reaches full stereo at 50%, and 100% is dual mono. Every reverb width was halved to keep its intent, and the mono fixes now narrow below 50%.
- **The doubles' routing.** The wiring steps left the doubles' Master route on. The DBL IN tracks now use Route to this track only, and sends go in last.
- **Pitcher's octave.** Plain MIDI mode keeps only the note name, so the 3rd line now runs in Octaves mode. The stem render clears the loop selection first.

Also fixed:
- The build order: unbuilt tracks stay muted, returns are switched with their mute, VOX BUS is set after the doubles, and no check relies on solo.
- Pro-C's Auto Gain stays off, and Vampire Haze's ducker gets a starting threshold.
- The dynamic-EQ shorthand is defined.
- Silk Stack's fallback is re-leveled for where its limiter sits.
- Key-move timing is clearer.
- Translation fixes point at automation clips.
- Rockstar Grit's yell clamp has a set-up routine.
- Wording that tripped a cold reader was rewritten.

Audit script, final run: structure, toolkit, value ranges, negative Pro-MB Range, Pro-MB times in %, Pro-R 2 styles and widths, Timeless controls, Pro-L 2 field order, parallel and return EQ at Output 0 dB, DBL ending in Pro-L 2, ear-check order, translation rows, decision refs, links and anchors all pass.

**5D · Ship.** README updated, and everything committed and pushed.
