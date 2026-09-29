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

## Step 2 · Blueprints

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

## Step 3 · Dial-In

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

## Step 4 · Stress Test

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

## Step 5 · Final Cut

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
| D15 | Return ducking is keyed from VOX IN over a sidechain-only connection. | LEAD already feeds the returns, and "Sidechain to this track" works by zeroing a connection's audio send. |
| D16 | Auto-Tune runs in the Modern algorithm (Classic Mode off) unless a sheet says otherwise. | Classic turns off Flex-Tune, Formant, Throat and Transpose. |
| D17 | Levels are set with the audio clip channels' volume knobs. Only whole-section clips get normalized, never short phrase clips one by one. *(Refines D10.)* | Keeps the contrast between quiet and loud lines. |
| D18 | Where a plugin offers a latency choice on a parallel track, it runs at zero latency, and FL's automatic PDC handles the rest. *(Refines D5.)* | The simplest way to keep parallel layers locked to the lead. |
