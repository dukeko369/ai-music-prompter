# Structure Guide — Song Architecture Design

## Philosophy

A song structure does more than label sections. It gives the AI model a **performance map** — telling it where to breathe, where to push, and how the emotional arc flows. The best structures read like a director's shot list: each section has a clear role, energy target, and instrumental identity.

Structure design has three layers:
1. **Section assignment** — what goes where (the skeleton)
2. **Dynamic annotation** — how each section performs (the muscle)
3. **Transition design** — how sections connect (the joints)

---

## Section Tag Reference

### Core Structure Tags (all platforms)
| Tag | Role | Typical Length |
|-----|------|----------------|
| `[Intro]` | Sets tone, instrumental or soft vocal entry | 2–8 bars |
| `[Verse]` / `[Verse 1]` / `[Verse 2]` | Story, narrative, lower energy | 8–16 bars |
| `[Pre-Chorus]` | Tension build, transition to chorus | 4–8 bars |
| `[Chorus]` | Hook, peak energy, title line, most memorable | 8 bars (typical) |
| `[Post-Chorus]` | Extension after chorus, secondary hook | 4–8 bars |
| `[Bridge]` | Contrast, emotional shift, often features key change or new perspective | 4–8 bars |
| `[Outro]` | Resolution, fade or final cadence | 4–8 bars |
| `[Interlude]` | Instrumental or atmospheric break between sections | 4–8 bars |
| `[Hook]` | Catchy repeated phrase or riff, can appear anywhere | 2–4 bars |

### Specialty Tags (Suno V5+)
| Tag | Use |
|-----|-----|
| `[Guitar Solo]` | Guitar solo — add bar count and style |
| `[Piano Solo]` | Piano solo |
| `[Sax Solo]` | Saxophone solo |
| `[Synth Solo]` | Synthesizer lead solo |
| `[Drum Break]` | Drum-focused section |
| `[Drop]` | EDM bass drop — the climax |
| `[Build]` | Rising tension, usually before a Drop |
| `[Breakdown]` | Stripped-back, minimal section |
| `[Fade Out]` | Gradual volume decrease to silence |
| `[Cold End]` | Abrupt stop, no fade |
| `[Loop]` | Section designed to loop seamlessly |

### Energy & Mood Tags (Suno V5+)
Layer these inside sections for dynamic control:
| Tag | Effect |
|-----|--------|
| `[Energy: Low]` | Subdued, intimate, sparse |
| `[Energy: Medium]` | Steady, conversational |
| `[Energy: Rising]` | Gradual build, layering |
| `[Energy: High]` | Full, powerful, peak |
| `[Energy: Maximum]` | All-out, climactic |
| `[Mood: Dark]` / `[Mood: Uplifting]` / `[Mood: Triumphant]` / `[Mood: Melancholic]` / `[Mood: Peaceful]` | Emotional color per section |
| `[Structure: Focused Performance]` | Tight, medium energy storytelling |
| `[Structure: Build-up]` | Rising tension, instruments layering |
| `[Structure: Anthemic Peak]` | Big hook energy, maximum impact |
| `[Structure: Minimalist Breakdown]` | Stripped back, intimate |

---

## Vocal Anchors

The vocal anchor is the **first line of the lyrics field** (Suno) — it's the single most important instruction for getting the right singer. The model locks in a voice within the first 1–2 seconds of generation.

### Templates

**Male:**
```
[Vocal: male, deep husky timbre, relaxed but intense delivery, clear diction, precise rhythm]
```

**Female:**
```
[Vocal: female, smooth and soulful, airy on quiet lines, powerful natural belting on peaks, contemporary R&B inflection]
```

**Rap:**
```
[Vocal: male, sharp articulate flow, precise enunciation, natural breath control, conversational rhythm]
```

**Duet:**
```
[Vocal: male and female duet, male baritone leads verses, bright female soprano joins chorus in harmony]
```

**Character / Genre-specific:**
```
[Vocal: female, breathy and delicate, slight vibrato on held notes, whisper-close, indie folk timbre]
[Vocal: male, gritty rock delivery, chest voice power, raspy high end, live stage energy]
[Vocal: Japanese female, soft anime-influenced timbre, clear enunciation, melodic pop delivery]
```

---

## Structure Templates by Genre

### Template A — Standard Pop / Folk (Most Common)
Best for: pop, folk, acoustic, singer-songwriter, R&B, country, mandopop, J-pop, K-pop
```
[Intro] (4 bars, main instrument theme)
[Verse 1] — narrative, low-mid energy
[Pre-Chorus] — build tension
[Chorus] — full hook, peak
[Verse 2] — develop story, slightly higher energy than V1
[Pre-Chorus] — build again
[Chorus] — repeat hook, stronger
[Bridge] — contrast, emotional turn
[Chorus] — final hook, maximum energy
[Outro] — resolve, fade or final cadence
```
Total: ~3:00–3:45

### Template B — Compact (Short-form / Single)
Best for: short-form content, demos, folk, indie, lo-fi, jingles
```
[Intro] (2–4 bars)
[Verse 1]
[Chorus]
[Verse 2]
[Chorus]
[Outro]
```
Total: ~2:00–2:30

### Template C — EDM / Dance
Best for: EDM, house, trance, dubstep, future bass, techno, hardstyle
```
[Intro] (8-16 bars, DJ-friendly, beat-only start)
[Build] — riser, filter sweep, tension
[Drop] — full energy, bass drop, main hook
[Breakdown] — strip back, vocal or pad focus
[Build] — second riser, more intense
[Drop] — second drop, variation or bigger
[Outro] — DJ-friendly fade or beat-only end
```
Total: ~3:30–5:00 (DJ-friendly lengths)

### Template D — Hip Hop / Trap
Best for: hip hop, trap, drill, melodic rap, boom bap
```
[Intro] (4 bars, beat tag or producer tag)
[Hook] — catchy refrain (chorus function)
[Verse 1] — 16 bars, main rap
[Hook]
[Verse 2] — 16 bars, feature or second perspective
[Hook]
[Bridge] — switch-up, new flow or instrumental
[Hook] — final, ad-libs heavy
[Outro]
```
Total: ~2:30–3:30

### Template E — Metal / Rock
Best for: metal, rock, punk, hard rock, metalcore, post-hardcore
```
[Intro] (4-8 bars, main riff)
[Verse 1] — lower intensity, build narrative
[Pre-Chorus] — tension
[Chorus] — explosive, full band
[Verse 2]
[Pre-Chorus]
[Chorus]
[Guitar Solo] (8 bars, bluesy/shredding/melodic)
[Bridge] — breakdown or key change
[Chorus] — final, most powerful
[Outro] — riff fade or cold end
```
Total: ~3:30–5:00

### Template F — Cinematic / Orchestral
Best for: film scores, trailer music, epic, fantasy, game soundtracks
```
[Intro] (atmospheric, drone or single instrument)
[Theme A] — main motif introduced, soft
[Build] — layering instruments, rising
[Theme A - Full] — full orchestra, peak
[Breakdown] — quiet, tension rebuild
[Build] — aggressive riser
[Theme B - Climax] — secondary theme, maximum intensity
[Resolution] — thematic resolution
[Outro] — return to atmosphere, fade
```
Total: ~3:00–6:00

### Template G — Chinese Ancient Style (古风)
Best for: 古风, 中国风, Chinese folk, traditional fusion
```
[引子 Intro] (4 bars, guzheng/dizi/xiao solo)
[主歌 Verse 1] — storytelling, sparse arrangement
[副歌 Chorus] — emotional peak, full traditional ensemble
[间奏 Interlude] (4 bars, erhu solo)
[主歌 Verse 2] — second narrative
[副歌 Chorus] — stronger delivery
[桥段 Bridge] — modulation or new perspective
[副歌 Chorus] — final, most dramatic
[尾声 Outro] — single instrument, fade to silence
```
Total: ~3:30–4:30

### Template H — Jazz
Best for: jazz, bebop, cool jazz, jazz fusion
```
[Intro] (4 bars, piano or bass establishes changes)
[Head] — main melody, full ensemble
[Solo 1] (piano/keys, 8-16 bars)
[Solo 2] (sax/trumpet, 8-16 bars)
[Solo 3] (optional, 8 bars)
[Head] — melody return
[Outro] — tag ending or fade on turnaround
```
Total: ~3:00–5:00

---

## Dynamic Arc Design

### The Energy Curve

Every song has an energy profile. Before writing structure, sketch the emotional shape:

```
Energy
  ▲
  │        ╭──╮       ╭──╮
  │       ╱    ╲     ╱    ╲    ╭──╮
  │      ╱      ╲   ╱      ╲  ╱    ╲
  │  ╭──╱        ╲─╱        ╲╱      ╲──╮
  │ ╱                                    ╲
  └────────────────────────────────────────▶ Time
    Intro V1 Pre C  V2 Pre C  Bridge C  Outro

Classic Pop Arc: Start moderate → build to first chorus →
drop for V2 → build higher → bridge contrast → final peak → resolve
```

### Arc Strategies

| Strategy | Description | Best For |
|----------|-------------|----------|
| **Gradual Rise** | Each section slightly higher energy than the last. Peaks at final chorus. | Ballads, cinematic, post-rock, trance |
| **Peaks & Valleys** | Alternating high/low. Chorus=peak, verse=valley. | Pop, rock, R&B, country |
| **Start Hot** | Explosive from bar 1. Sustain then dip for bridge. Final peak. | Punk, metal, EDM, trailer |
| **Slow Burn** | Minimal start, slow build across entire song. One big climax near end. | Post-rock, ambient, cinematic, experimental |
| **Flat Platform** | Consistent energy throughout. Subtle variations. | Lo-fi, ambient, study music, house, techno |
| **Inverted Arc** | Start big → gradually strip away → end intimate. | Art pop, experimental, film scenes |

---

## Transition Design

Bare section tags produce jarring cuts. Annotate transitions for smoother flow:

### Transition Types

```
[Transition: 2-bar riser, filter sweep up, white noise]
[Transition: drum fill 4 beats, crash cymbal into next section]
[Transition: bass drop-out, one beat silence, full band enters]
[Transition: reverse reverb swell into chorus]
[Transition: piano arpeggio descends, handoff to guitar]
[Transition: sub-bass fade out, atmospheric pad bridges]
[Transition: tape stop effect, restart at new tempo]
[Transition: key change, modulate up one whole step]
[Transition: seamless — instrumental sustains through]
```

### Placing Transitions

- **Verse → Pre-Chorus**: subtle, often just a bass movement or drum fill
- **Pre-Chorus → Chorus**: dramatic — riser, crash, or drop-out before impact
- **Chorus → Verse 2**: quick reset, often a drum fill or single instrument drop
- **Bridge → Final Chorus**: the biggest transition — key change, full band build, or silence before explosion
- **Chorus → Outro**: resolve — instruments drop, reverb tail, or final hit

---

## Outro Styles

| Style | Instruction | When to Use |
|-------|-------------|-------------|
| **Fade Out** | `[Fade Out]` — gradual volume decrease over 4-8 bars | Pop, folk, lo-fi, ambient |
| **Cold End** | `[Cold End]` — abrupt stop on final chord | Rock, punk, jazz, dramatic |
| **Loopable** | `[Loop]` — ending that connects back to beginning | Game music, background, meditation |
| **Final Hit** | Final bar has a big chord + reverb tail. All instruments together. | Cinematic, epic, orchestral |
| **Solo Instrument** | Single instrument (piano/guitar) plays final motif and decays | Ballad, intimate, singer-songwriter |
| **Reverse Fade** | Instruments fade in one by one, then stop — a reverse intro | Experimental, art pop, electronic |
| **Callback Outro** | Outro reprises the intro motif — bookend structure | Pop, folk, concept pieces |

---

## Design Workflow

### Step 1: Count and Categorize
Count lyric lines. Identify natural breaks — where does the topic shift? Where does the emotional peak happen? Short lines (≤6 syllables) may be hook material; long narrative lines are verse material.

### Step 2: Pick a Template
Choose from Templates A–H based on genre. This is a starting point — adjust to fit actual lyric flow.

### Step 3: Allocate Lyrics
- Verses get the narrative/storytelling lines
- Pre-Chorus gets the "about to explode" transition lines (often 2-4 short lines)
- Chorus gets the most impactful, repeat-worthy lines
- Bridge gets the twist, realization, or emotional turn
- Don't force-fit — if lyrics don't fit a pre-chorus, skip it

### Step 4: Annotate Each Section
For each section tag, add:
1. Energy level marker
2. Vocal style (can vary per section — whisper verse → belt chorus)
3. Key instrumental detail
4. Transition to next section (if not the last)

### Step 5: Sanity Check the Arc
- Does the energy profile match the genre?
- Is there a clear emotional climax?
- Are any two consecutive sections too similar? (Add contrast)
- Is the overall length reasonable? (2–5 min for most styles)

### Step 6: Present with Visual

Show the energy curve alongside the structure:
```
[Intro]         ██░░░░░░░░  Low, piano only
[Verse 1]       ███░░░░░░░  Med-Low, sparse
[Pre-Chorus]    █████░░░░░  Building, drums enter
[Chorus]        ████████░░  High, full band
[Verse 2]       ████░░░░░░  Med, richer than V1
[Pre-Chorus]    ██████░░░░  Building, stronger
[Chorus]        █████████░  Very High, peak
[Bridge]        ███░░░░░░░  Med-Low, contrast
[Chorus]        ██████████  Maximum, final
[Outro]         ██░░░░░░░░  Low, fade
```

---

## Platform Formatting

### Suno Lyrics Field Format
```
[Vocal: female, breathy intimate, indie folk timbre]

[Intro]
(piano solo, 4 bars, gentle arpeggios)

[Verse 1]
[Energy: Low]
Walking through the morning light
Shadows fading out of sight

[Pre-Chorus]
[Energy: Rising]
Here it comes, can you feel it now

[Chorus]
[Energy: High]
[Vocal Style: Power]
We are RISING, breaking through the sky
Nothing's gonna stop us, born to fly

[Verse 2]
[Energy: Medium]
...

[Bridge]
[Energy: Medium]
[Mood: Triumphant]
...

[Guitar Solo]
(8 bars, bluesy bends, emotional vibrato)

[Chorus]
[Energy: Maximum]
[Vocal Style: Belt]
...

[Outro]
[Fade Out]
(piano fades, final chord sustains)
```

### Universal Format
Same section tags, skip Suno-only syntax. Keep `[Vocal:]` anchor at top. Energy/Mood tags inside brackets optional — use descriptive comments instead:
```
[Verse 1] — soft, breathy, sparse piano
lyrics here...

[Chorus] — full, powerful, all instruments
lyrics here...
```

---

## Common Pitfalls

| Problem | Solution |
|----------|----------|
| AI skips intro, starts singing immediately | Write `(no vocals, instrumental only)` inside `[Intro]` or add "starts with instrumental intro" to style prompt |
| Vocal changes personality mid-song | Make the vocal anchor detailed enough; use per-section `[Vocal Style:]` for emphasis |
| 2nd chorus sounds identical to 1st | Annotate: `[Chorus]` → `[Chorus - stronger, more ad-libs]` → `[Chorus - maximum, belt, all stops]` |
| Song ends abruptly | Always include `[Outro]` or `[Fade Out]` |
| Bridge doesn't feel different enough | Change key element: strip drums, change vocal style, modulate key, add new instrument |
| Too many sections, model truncates | Simplify. Max ~12 sections for Suno v4/v5. Udio handles shorter segments. |
| Transition between sections is messy | Add explicit transition descriptions: drum fill, riser, or "seamless" |
| Long extend chains lose coherence | Add `[Callback: maintain energy and key from verse 2]` when extending |
