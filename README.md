# 🌙 MiMoDream

> **AI Dream Interpreter powered by Xiaomi MiMo V2.5**
> Paste your dream → get symbol analysis, psychological themes, emotional mapping, and a visual dream constellation

🔗 **Live demo:** [gyoomei.github.io/mimodream](https://gyoomei.github.io/mimodream/) · 📂 **Repo:** [github.com/gyoomei/mimodream](https://github.com/gyoomei/mimodream)

---

## What it does

MiMoDream transforms your subconscious narratives into structured psychological insight. Describe any dream — the AI identifies key symbols (eagle, mirror, water, fire…), maps their Jungian and cultural meanings, detects overarching themes, reads emotional undercurrents, and delivers actionable guidance. Every interpretation is visualized as a dream map — a radial constellation connecting your symbols to a central dream core.

```
You paste:    "I was flying over a golden city at sunset. A white eagle
               guided me to a crystal tower. Inside, I found a book that
               wrote itself as I read it."

MiMo replies: 🔮 Dream Summary — profound spiritual journey toward hidden
                 knowledge and self-discovery
              🪞 Key Symbols — Eagle (higher wisdom), Golden City (ambition),
                 Self-Writing Book (unconscious growth), Crystal Tower (clarity)
              🌀 Themes — Guided Transformation, Hidden Knowledge
              💧 Emotional Undercurrent — wonder, trust, growing confidence
              🧭 Guidance — trust the process, stop second-guessing
              ⚡ Vividness Score — 8/10
```

---

## Features

- 🔮 **Dream Interpretation** — AI-powered symbol analysis using Jungian psychology, cultural traditions, and modern dream research
- 🗺️ **Dream Map** — Canvas-based radial visualization connecting dream symbols to a central core
- 📓 **Dream Journal** — Persistent storage (localStorage) of all interpreted dreams with mood tags
- 📊 **Pattern Tracking** — Recurring symbol frequency charts and mood statistics across sessions
- 📖 **Dream Dictionary** — 30+ common dream symbols with psychological meanings (water, flying, teeth, snake, mirror, fire, ocean, house, tree…)
- 🎭 **Mood Selection** — Tag each dream upon waking: neutral, scared, happy, sad, confused, lucid
- 🌗 **Dark/Light Mode** — Full theme toggle with deep indigo/violet aesthetic
- 🔤 **Unique Typography** — Cormorant Garamond (display) + Nunito (body) for a dreamy, editorial feel
- ✨ **Starfield + Nebula** — Animated CSS starfield with drifting nebula glow orbs
- 📱 **Mobile Responsive** — Fluid layout from 375px to 1920px, safe area inset support
- 🌐 **7 Languages Support** — Interpretations adapt to context (UI in EN/ID)
- 🔁 **Retry Logic** — 3-attempt fetch with graceful fallback on API timeout

---

## How it works

```
┌─────────────────────────────────────────────────────────────┐
│  Input: User describes dream + selects mood                 │
│                          ↓                                   │
│  MiMo V2.5 (Pollinations.ai)  →  Structured interpretation  │
│                          ↓                                   │
│  Symbol Extractor (regex)     →  Parse emoji-tagged symbols  │
│                          ↓                                   │
│  Dream Map (Canvas 2D)        →  Radial node graph           │
│                          ↓                                   │
│  Journal (localStorage)       →  Persist dream + symbols     │
│                          ↓                                   │
│  Pattern Engine               →  Symbol frequency analysis   │
└─────────────────────────────────────────────────────────────┘
```

**Zero backend.** Everything runs client-side in your browser. No API key. No tracking.

---

## Try these dreams

| Dream | Mood | Expected symbols |
|---|---|---|
| "I was flying over a city made of glass" | 😊 Happy | flying, city, glass |
| "A snake chased me through a dark forest" | 😨 Scared | snake, chase, forest |
| "I found a key that opened a door to the ocean" | 😐 Neutral | key, door, ocean |
| "My teeth fell out while looking in a mirror" | 😢 Sad | teeth, mirror |
| "I was in a burning house but felt calm" | ✨ Lucid | fire, house, calm |

---

## Stack

- **Frontend:** Vanilla JavaScript, single HTML file (~37KB total)
- **AI:** [Xiaomi MiMo V2.5](https://github.com/XiaomiMiMo) via [Pollinations.ai](https://text.pollinations.ai/) — free, no API key
- **Canvas:** HTML5 Canvas 2D for dream map visualization
- **Storage:** localStorage for journal, symbols, theme, mood
- **Fonts:** [Cormorant Garamond](https://fonts.google.com/specimen/Cormorant+Garamond) + [Nunito](https://fonts.google.com/specimen/Nunito) + [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts CDN
- **Hosting:** GitHub Pages (zero infra cost)

---

## Architecture decisions

**Why single HTML?** Zero deploy friction, zero backend cost, easy to fork. Anyone can clone and self-host in one minute.

**Why client-side only?** Privacy. Your dreams never hit a server we control. The browser talks directly to Pollinations.ai.

**Why Cormorant Garamond?** Dream interpretation is an intimate, reflective experience. A humanist serif with elegant contrast signals "this is thoughtful" — not "this is a dashboard." Paired with Nunito's warmth for body text, the typography feels like opening an old journal.

**Why a dream map?** Symbols don't exist in isolation — they form constellations of meaning. The radial canvas visualization shows how your dream elements relate to each other and to the central unconscious core.

---

## Roadmap

- [ ] Lucid dreaming induction tips based on dream patterns
- [ ] Dream series analysis (multi-night trend detection)
- [ ] Export journal as PDF with dream map illustrations
- [ ] Shared dream boards (compare symbols with friends)
- [ ] Voice input for dream narration
- [ ] Archetype detection (Hero, Shadow, Anima/Animus, Trickster)

---

## Run locally

```bash
git clone https://github.com/gyoomei/mimodream.git
cd mimodream
python3 -m http.server 8080
# open http://localhost:8080
```

That's it. No build step, no `npm install`, no environment config.

---

## License

MIT — fork it, ship it, interpret your dreams.

---

**Built with 🧠 [Xiaomi MiMo V2.5](https://github.com/XiaomiMiMo) · Submitted to the [Xiaomi MiMo 100T program](https://100t.xiaomimimo.com/)**
