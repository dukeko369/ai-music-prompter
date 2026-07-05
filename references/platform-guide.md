# Platform Guide — Suno vs Universal Formatting

## When to Use Which Mode

Ask the user at the start: "Are you generating on Suno specifically, or do you want a universal format that works across platforms?"

- **Suno Mode**: The user says Suno, or they're unsure but want maximum control. Suno has the richest tag vocabulary.
- **Universal Mode**: The user names Udio, Lyria, Eleven Music, or wants one prompt for multiple platforms. Stick to common-denominator syntax.

---

## Style Prompt Comparison

### Suno: Concise Comma Tags
Suno's style field works best with concise comma-separated tags — not full sentences. Maximum ~200 characters.

**✓ Good (Suno):**
```
modern pop, bright confident, mid-tempo, crisp drums soft synths, female vocal, catchy chorus
```

**✗ Bad (Suno):**
```
A modern pop song with a bright and confident mood at mid-tempo featuring crisp drums and soft synthesizers with female vocals and a catchy chorus.
```

**Suno length guideline:** 5–8 strong, non-conflicting tags. Front-load the 3 most important.

### Universal: Tags or Full Sentences
Other platforms (Udio, Lyria) are more flexible — both formats work. Use full sentences only when it helps clarity.

**✓ Good (Universal, either format):**
```
lo-fi ambient, calm, slow tempo, soft piano, vinyl texture, instrumental
```
OR
```
A calm lo-fi ambient track at slow tempo with soft piano and vinyl crackle texture, instrumental only, for studying.
```

---

## Lyrics Field Comparison

### Suno: Rich Tag Vocabulary

Suno supports the richest set of inline tags in the lyrics field. Use them:

```
[Intro]
(piano solo, 4 bars, soft arpeggios)

[Verse 1]
[Energy: Low]
[Vocal Style: Soft, breathy]
lyrics here...

[Pre-Chorus]
[Energy: Rising]

[Chorus]
[Energy: High]
[Vocal Style: Power]
[Mood: Triumphant]
lyrics here...

[Bridge]
[Structure: Minimalist Breakdown]
[Vocal Style: Intimate]
lyrics here...

[Outro]
[Fade Out]
```

Available Suno inline tags:
- `[Vocal Style: Soft/Breathy/Power/Raspy/Falsetto/Belt/Spoken Word/Rap/Whisper/Operatic]`
- `[Vocal Effect: Reverb/Delay/Auto-tune/Vocoder/Distortion]`
- `[Vocal Mix: Loud/Balanced/Soft/Double Tracked/Echo]`
- `[Energy: Low/Medium/High/Rising/Maximum]`
- `[Mood: Dark/Uplifting/Melancholic/Triumphant/Peaceful]`
- `[Structure: Focused Performance/Build-up/Anthemic Peak/Minimalist Breakdown]`
- `[Instrumental]` `[Guitar Solo]` `[Piano Solo]` `[Synth Solo]` `[Drum Break]` `[Drop]` `[Build]` `[Breakdown]`
- `[Callback: <instruction>]` — for Extend mode to maintain coherence

### Universal: Cleaner, Fewer Tags

```
[Intro]
(piano solo, 4 bars, soft arpeggios)

[Verse 1] — soft, breathy vocal, sparse piano
lyrics here...

[Pre-Chorus] — building energy
lyrics here...

[Chorus] — full power, all instruments
lyrics here...

[Bridge] — stripped back, intimate, key change
lyrics here...

[Outro] — fade out, piano only
```

Skip Suno-only tags. Use descriptive comments after the section tag instead (with `—` or parentheses). Section annotations keep the structural intent without platform-locked syntax.

---

## Vocal Anchor Comparison

### Suno
Place a detailed vocal anchor as the very first line:
```
[Vocal: male, deep husky timbre, relaxed but intense delivery, clear diction, precise rhythm]
```

### Universal
Same concept, slightly less specific (some platforms ignore or misinterpret very detailed anchors):
```
[Vocal: deep male, husky, relaxed delivery]
```

---

## Negative Prompts / Exclusions

### Suno
Suno responds well to exclusion tags in the style prompt:
```
90s hip hop, boom bap, no trap beats, no auto-tune
heavy metal, aggressive, no synth, no pop structure
```

### Universal
Exclusions are less reliably supported. Instead, be more specific in what you DO want rather than what you don't. If exclusion is necessary, write it as a constraint: "pure acoustic, no electronic elements."

---

## Side-by-Side: Same Song, Two Formats

### Creative Brief
"An introspective rap song about late-night thoughts, moody but with a steady groove, male vocal, 80-90 BPM, warm production with vinyl crackle"

### Suno Output
**Style Prompt:**
```
melodic rap, introspective late-night, mid-slow 85 BPM, warm pads clean drums, male vocal, vinyl texture, no trap, no auto-tune
```

**Lyrics Field:**
```
[Vocal: male, relaxed conversational flow, slight rasp, natural breath timing, clear enunciation]

[Intro]
(8 bars, warm vinyl crackle, soft pad, distant)

[Verse 1]
[Energy: Low]
[Vocal Style: Soft, conversational]
3 AM the city breathing slow
Streetlights painting gold on broken roads
...

[Hook]
[Energy: Medium]
[Vocal Style: Melodic, slightly sung]
Can't sleep when the world's this loud
Head full of clouds, head full of clouds
...

[Verse 2]
[Energy: Medium]
...

[Hook]
[Energy: High]
[Vocal Style: More intense, rhythmic drive]
...

[Outro]
[Energy: Low]
[Fade Out]
(vinyl crackle, pad fades)
```

### Universal Output
**Style Prompt:**
```
melodic rap, introspective and moody, mid-slow 85 BPM, warm pads and clean drums, male vocal, vinyl texture
```

**Lyrics Field:**
```
[Vocal: male, relaxed flow, slight rasp]

[Intro] — 8 bars, vinyl crackle, soft pad, distant

[Verse 1] — soft, conversational
3 AM the city breathing slow
Streetlights painting gold on broken roads
...

[Hook] — melodic, slightly sung
Can't sleep when the world's this loud
Head full of clouds, head full of clouds
...

[Verse 2] — medium energy

[Hook] — more intense, rhythmic drive

[Outro] — fade out, vinyl crackle, pad fades
```

---

## Platform-Specific Quirks

### Suno
- **V5** has tighter tag adherence — use `[Energy:]` and `[Structure:]` tags confidently
- **V4** may ignore some advanced tags; fall back to descriptive comments
- **Extend mode**: Always include `[Callback: maintain energy and key from previous]` or the model drifts
- **Instrumentals**: Add "no vocals" or "instrumental only" to style prompt OR use `[Instrumental]` section tags
- **Covers/Personas**: Not covered by this skill — Suno's Cover and Persona features use different mechanics

### Udio
- Generates in 30-second chunks — design structures with short, self-contained sections
- The Extend feature lets you build intro/outro separately
- Udio's style adherence is looser — a good lyrics structure matters more than a perfect style prompt
- Udio does NOT support `[Energy:]`, `[Structure:]`, or `[Callback:]` tags

### Lyria (Google)
- Supports multi-language lyrics (English, German, Spanish, French, Hindi, Japanese, Korean, Portuguese)
- Best at orchestral, classical, and fusion genres
- Style prompt: full sentences preferred over comma tags
- Place important tags early in the prompt — Lyria front-loads like Suno

### Eleven Music (ElevenLabs)
- Designed for production music — excels at clean, commercial sound
- Strongest with pop, electronic, hip-hop, and background music
- Vocal specification is very detailed — use rich vocal descriptors
- Less responsive to unconventional/experimental genre combos

---

## When the User Doesn't Specify a Platform

Default to **Universal mode** and mention: "This will work on Suno, Udio, Lyria, and most other platforms. If you're using Suno specifically, I can add richer section tags — just let me know."
