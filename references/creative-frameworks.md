# Creative Frameworks — Inspiration & Expansion

When the user has a vague idea or wants something unique, use these frameworks to generate directions.

---

## Framework 1: Spark-to-Full-Plan

### The Algorithm

When the user gives only a one-sentence spark ("深夜开车", "a rainy day", "something like Coldplay"), complete all 8 dimensions by association:

| Spark | → Dimension | → Suggestion |
|-------|------------|--------------|
| 深夜开车 | Genre | Synthwave / Dream Pop |
| | Mood | Nostalgic, lonely but peaceful |
| | Tempo | Mid-slow, 80-95 BPM, steady cruise |
| | Vocal | Male, breathy, intimate, slight reverb |
| | Instruments | Pulsing synth bass, soft pads, electric piano |
| | Texture | Warm analog, slight haze |
| | Era | 80s retro / timeless |
| | Mix | Medium reverb, wide stereo, like through a car window |

Then present the plan: "Here's what I'm hearing for 'late-night drive': synthwave base with a nostalgic lonely feel, mid-slow cruise tempo around 85 BPM, male breathy vocal with reverb, pulsing synth bass and electric piano, warm analog haze, wide stereo mix like looking through a car window. Sound right, or shall I go in a different direction?"

### Spark Categories with Common Paths

| Spark Type | Default Path | Alt Path 1 | Alt Path 2 |
|------------|-------------|------------|------------|
| "Night drive" | Synthwave, nostalgic | Lo-fi hip hop, chill | Dark ambient, cinematic |
| "Rainy day" | Lo-fi, melancholic | Solo piano, classical | Jazz trio, cozy |
| "Workout" | EDM, high energy | Hard rock, aggressive | Trap, heavy 808 |
| "Heartbreak" | Piano ballad, sad | Alt R&B, sensual sad | Indie folk, bittersweet |
| "Morning coffee" | Acoustic folk, warm | Bossa nova, sunny | Lo-fi beats, relaxed |
| "Epic moment" | Orchestral, triumphant | Synthwave, heroic | Cinematic hybrid, massive |
| "Like [reference artist]" | Match genre + era | Genre-fusion nearby | Opposite genre, same mood |
| "Something unique" | Dissonant pairing (see below) | World fusion | Decade clash |
| "Chinese ancient" | 古风, guzheng+dizi | Chinese folk-pop fusion | Cinematic Chinese orchestral |
| "Cyberpunk" | Industrial electronic, dark | Synthwave, dystopian | Dark trap, futuristic |

---

## Framework 2: Dissonant Pairing Generator

Push the model into interesting territory by pairing rarely-connected styles. When the user wants "something different" or "a unique sound," suggest 2–3 pairings and let them pick:

| Pairing | What It Sounds Like |
|---------|-------------------|
| Orchestral + Phonk | Cinematic Memphis — grand strings over distorted cowbell 808s |
| Math Rock + Gospel | Odd-time guitar tapping with soulful choir call-and-response |
| Shoegaze + Trap | Wall of reverb guitars over 808 hi-hats |
| Bossa Nova + Electronic | Brazilian swing with glitch beats and synth pads |
| Chinese Ancient + Synthwave | Guzheng over retro arpeggios — neon dynasty |
| Doom Metal + Ambient | Crushing slow riffs dissolve into atmospheric drone |
| Celtic Folk + Drum & Bass | Fiddle reels at 170 BPM with rolling basslines |
| Opera + Industrial | Classical soprano over mechanical percussion and noise |
| Lo-Fi + Flamenco | Vinyl crackle and chill beats with passionate Spanish guitar |
| 80s City Pop + Jersey Club | Japanese funk bass with chopped sample bounce beats |
| Bluegrass + Trap | Banjo rolls over 808 slides and hi-hat rolls |

Pairing rules:
- **Contrast tempo** (slow + fast elements) — creates tension
- **Contrast era** (ancient instrument + modern production)
- **Contrast geography** (traditional from one culture + genre from another)
- **Avoid**: 3+ genres, same-family pairs (rock + metal = not dissonant enough)

---

## Framework 3: Mood–Style Pairing Matrix

Not every style works equally well for every mood. This matrix shows high-probability matches:

| Mood ↓ / Style → | Pop | Rock | Electronic | Hip Hop | Orchestral | Lo-Fi | Jazz | Metal | Folk |
|-------------------|-----|------|------------|---------|------------|-------|------|-------|------|
| **Happy/Upbeat** | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | ⭐⭐ | ⭐⭐ | ✗ | ⭐⭐ |
| **Melancholic** | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ | ⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ✗ | ⭐⭐⭐ |
| **Epic/Triumphant** | ⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐ | ⭐⭐⭐ | ✗ | ✗ | ⭐⭐⭐ | ⭐ |
| **Dark/Brooding** | ⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐ | ⭐ | ⭐⭐⭐ | ⭐ |
| **Romantic** | ⭐⭐⭐ | ⭐ | ⭐ | ⭐ | ⭐⭐ | ⭐⭐ | ⭐⭐⭐ | ✗ | ⭐⭐ |
| **Energetic** | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ✗ | ⭐ | ⭐⭐⭐ | ⭐ |
| **Chill/Relaxed** | ⭐ | ✗ | ⭐⭐ | ⭐ | ⭐ | ⭐⭐⭐ | ⭐⭐⭐ | ✗ | ⭐⭐ |
| **Tense/Suspense** | ✗ | ⭐ | ⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐ | ⭐ | ⭐⭐ | ✗ |
| **Nostalgic** | ⭐⭐ | ⭐ | ⭐⭐ | ⭐ | ⭐⭐ | ⭐⭐⭐ | ⭐⭐ | ✗ | ⭐⭐⭐ |
| **Spiritual** | ⭐ | ✗ | ⭐⭐ | ✗ | ⭐⭐⭐ | ⭐ | ⭐⭐ | ✗ | ⭐⭐ |

⭐⭐⭐ = High-probability match, ⭐⭐ = Works with care, ⭐ = Possible but tricky, ✗ = Avoid

Use this to steer users away from doomed combinations and toward ones that AI models handle well. "Melancholic metal" almost never works — suggest "melancholic post-rock" or "aggressive metal" instead.

---

## Framework 4: Reference Artist Decoder

When the user says "like [Artist X]", decode what they actually mean:

1. **Don't try to replicate the artist** — AI music models can't (and shouldn't) copy specific artists
2. **Extract the DNA**: genre, era, production style, vocal character, tempo range, instrument palette, emotional register
3. **Translate into dimensions**: "like Laufey" → jazz-pop, warm analog, female breathy low alto, 70-90 BPM, piano+bass+strings, romantic nostalgic

### Quick Decoder (common references)
| Artist Mentioned | Likely Means |
|-----------------|--------------|
| "Like Laufey" | Jazz-pop, bossa nova influence, warm vintage production, breathy low female vocal |
| "Like Coldplay" | Anthemic pop-rock, piano-driven, building energy, emotional male tenor, atmospheric |
| "Like Billie Eilish" | Dark alt-pop, minimal production, ASMR-quality breathy female vocal, sub-bass |
| "Like Hans Zimmer" | Cinematic orchestral, building layers, epic, Inception braaam, dark atmospheric |
| "Like Joji" | Lo-fi R&B, melancholic, slow tempo, intimate male vocal, sparse production |
| "Like NewJeans" | K-Pop with Y2K/UK garage influence, bright, airy female vocal, minimal beat |
| "Like Jay Chou" | Mandopop, R&B + Chinese traditional fusion, melodic, piano-driven, mid-tempo |
| "Like Arctic Monkeys" | Indie rock, gritty male vocal, driving drums, sharp lyrics, British |
| "Like Frank Ocean" | Alt R&B, experimental, intimate, sparse production, falsetto, emotional |
| "Like RADWIMPS" | J-rock/pop, piano-driven, building energy, emotional male vocal, cinematic |

---

## Framework 5: Use-Case-Driven Design

When the user describes a use case rather than a sound, reverse-engineer from function:

| Use Case | Constraints | Genre → Production → Mood → Tempo |
|-----------|-------------|------------------------------------|
| Podcast intro | 15-30 sec, memorable but not distracting, clear ending | Upbeat pop/electronic → clean mix, bright → energetic but not chaotic → 100-120 BPM |
| YouTube background | Loopable or long, steady energy, no distracting changes | Lo-fi/chill → consistent texture → calm, focused → 80-90 BPM |
| Study/Work | No vocals (or very soft), no sudden changes, no earworms | Ambient/lo-fi/classical → soft dynamics, even → peaceful → 60-80 BPM |
| Gaming montage | Sync-able drops, building energy, impactful | Cinematic hybrid/trap → big transitions → epic, aggressive → 120-150 BPM |
| Wedding video | Romantic, timeless, emotional arc | Acoustic/piano → warm production → romantic, nostalgic → 70-90 BPM |
| Product ad (luxury) | Sophisticated, short, distinctive | Orchestral/jazz → polished, hi-fi → elegant, confident → 80-100 BPM |
| Product ad (youth) | Energetic, trendy, short | Pop/EDM/hip hop → clean commercial → bright, exciting → 120-140 BPM |
| Sleep/Meditation | Very slow, no surprises, no vocals | Ambient/drone → soft, spacious → peaceful → 40-60 BPM |
| Fashion runway | Confident, rhythmic, distinctive | Electronic/industrial → sharp, spatial → cool, edgy → 110-130 BPM |
| Short-form (TikTok/Reels) | 15-60 sec, hook in first 3 sec, loopable | Pop/hip hop → punchy → energetic, catchy → 100-140 BPM |
| Ringtone | 10-30 sec, distinctive but not annoying, loopable | Pop/electronic → clean → bright, catchy → 90-120 BPM |
| Game menu | Loopable, atmospheric, sets mood without fatigue | Ambient/orchestral → spatial → mysterious/calm → 60-100 BPM |
| Presentation background | Not distracting, professional, consistent | Corporate/pop instrumental → clean → positive, neutral → 80-110 BPM |

---

## Framework 6: Lyric Mood → Production Mapping

When the user provides lyrics but doesn't have a production vision, read the emotional content of the lyrics and suggest:

| Lyric Content | → | Production Approach |
|---------------|---|---------------------|
| Confessional, personal, diary-like | → | Intimate, dry, close-mic, minimal arrangement |
| Social commentary, protest, anger | → | Raw, distorted, live energy, aggressive drums |
| Love, devotion, affection | → | Warm, lush, reverb, strings, major key |
| Loss, grief, longing | → | Sparse, echo, minor key, single instrument carries weight |
| Joy, celebration, triumph | → | Bright, big, full band, major key, uptempo |
| Storytelling, narrative, journey | → | Dynamic arc, gradual build, genre-bending allowed |
| Abstract, surreal, dreamlike | → | Washed-out, effects-heavy, unconventional structure |
| Humor, satire, wit | → | Bouncy, playful, unexpected sounds, tight arrangement |
| Nature, landscape, atmosphere | → | Ambient elements, natural sounds, spacious, slow build |
| Urban, night, city, modern | → | Electronic elements, reverb, cold or neon palette |

---

## When to Use Each Framework

| Situation | Framework |
|-----------|-----------|
| User gives one line ("i want a late night driving song") | 1: Spark-to-Full-Plan |
| User says "make it unique" or "something different" | 2: Dissonant Pairing |
| User picks a mood but can't pick a style | 3: Mood–Style Matrix |
| User references an artist | 4: Reference Artist Decoder |
| User describes a use case, not a sound | 5: Use-Case-Driven |
| User pasted lyrics with no musical direction | 6: Lyric Mood → Production |
