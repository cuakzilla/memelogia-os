# Memelogía OS
### Real-Time Memetic Intelligence System · v9.0

> *"Memetic intelligence should turn cultural chaos into actionable understanding without collapsing uncertainty into false certainty."*

[![Deploy](https://img.shields.io/badge/Deploy-Cloudflare%20Pages-orange)](https://pages.cloudflare.com)
[![Stack](https://img.shields.io/badge/Stack-HTML%20%2B%20Vanilla%20JS-blue)](/)
[![AI](https://img.shields.io/badge/AI-Claude%20%7C%20Gemini%20%7C%20Grok%20%7C%20GPT--4o-purple)](/)
[![License](https://img.shields.io/badge/License-Proprietary-red)](/)

---

## 1. The problem it solves

The internet produces **millions of cultural artifacts per hour** — memes, viral audio, TikTok videos, emerging narratives, shitposts, remixed templates. Organizations have no tooling to turn that chaos into actionable intelligence.

**What exists today isn't enough:**

| Tool | What it does | What it does NOT do |
|---|---|---|
| KnowYourMeme | Explains historical memes | No risk detection, no emerging-narrative signal |
| Brandwatch / Mention | Measures volume and sentiment | No cultural-meaning or irony interpretation |
| ChatGPT directly | Answers questions | No epistemic framework, no self-audit |
| Palantir | Mass data analysis | Enterprise contracts and 6-month implementations |

**Memelogía OS delivers:** what a meme really means (in 4 layers of reading), why it's happening (a causal chain with invisible forces), what risk it carries (6 dimensions, 0–100), how it will evolve (4 simulated scenarios), and it translates all of that into language anyone understands — not just experts.

It works with **image, text, audio, and video.**

---

## 2. Technical architecture

### Stack

```
┌─────────────────────────────────────────────────────────────┐
│                     MEMELOGÍA OS v9.0                       │
│                    Single file · ~217KB                     │
├─────────────────────────────────────────────────────────────┤
│  FRONTEND                                                   │
│  HTML5 + CSS3 + JavaScript ES2022                          │
│  Chart.js 4.4.1 (CDN) · Zero dependencies · Zero build     │
├─────────────────────────────────────────────────────────────┤
│  AI CASCADE (automatic waterfall)                          │
│  1. Anthropic Claude Sonnet (+ native Web Search)          │
│  2. Google Gemini 1.5 Flash (+ native audio/video)         │
│  3. xAI Grok Beta                                          │
│  4. OpenAI GPT-4o                                          │
├─────────────────────────────────────────────────────────────┤
│  PERSISTENCE                                                │
│  localStorage · no backend · no database                   │
│  ml_hist_v2 · ml_api_keys · ml_lang · ml_theme · ml_library│
├─────────────────────────────────────────────────────────────┤
│  DEPLOY                                                     │
│  GitHub → Cloudflare Pages (auto-deploy)                   │
└─────────────────────────────────────────────────────────────┘
```

### Analysis flow (main pipeline)

```
INPUT (image / text / audio / video)
          │
          ▼
┌─────────────────────┐
│  SANITIZATION       │ ← anti prompt-injection
│  + MODE SELECTOR    │ ← Quick (5s) / Deep (web search) / Media
└─────────────────────┘
          │
          ▼
┌─────────────────────────────────────────────────┐
│  AI CASCADE                                     │
│  Anthropic ──→ on failure (quota/rate) ──→      │
│  Gemini    ──→ on failure               ──→     │
│  Grok      ──→ on failure               ──→     │
│  OpenAI    ──→ result or final error            │
└─────────────────────────────────────────────────┘
          │
          ▼
┌─────────────────────────────────────────────────┐
│  10 LAYERS OF MEMETIC ANALYSIS                 │
│  1. Template ID + genealogy                    │
│  2. Humor type (8 categories)                  │
│  3. Narrative type (7 categories)              │
│  4. Emotional vector                           │
│  5. 4 simultaneous interpretations             │
│  6. Confidence scores (4 dimensions)           │
│  7. Risk scoring (6 dimensions, 0–100)         │
│  8. Causal chain                               │
│  9. Decision (SAFE/MONITOR/INVESTIGATE/        │
│               ESCALATE/CRITICAL)               │
│  10. Self-audit (explicit blind spots)         │
└─────────────────────────────────────────────────┘
          │
          ▼
┌─────────────────────────────────────────────────┐
│  SIGNAL LAYER (human narrative)                │
│  · Journalistic headline (≤12 words)           │
│  · Invisible Forces (visual chips)             │
│  · 3 perspectives: journalist/analyst/public   │
│  · Expandable historical context               │
└─────────────────────────────────────────────────┘
          │
          ▼
     RESULT + FOLLOW-UP CHAT + EXPORT
```

### System modules

```
┌──────────────────────────────────────────────────────────────┐
│  ⬡ COMMAND CENTER    Live dashboard, narratives, alerts      │
│  ◎ MEME ANALYZER     Image + Text + Audio + Video + Mic      │
│  ◷ HISTORY           Persistent history, export JSON/MD      │
│  🌐 WORLD·LIBRARY     17 countries, meme of the day, library │
│  ◈ MEME ATLAS        Cultural-ecosystem map                  │
│  ⟁ CAUSALITY ENGINE  Cause-and-effect chains                 │
│  ◧ SCENARIO LAB      4-scenario simulator                    │
│  ◬ RISK ENGINE       Scoring + kill switches + SBOM          │
└──────────────────────────────────────────────────────────────┘
```

### Media flow (audio/video)

```
AUDIO (MP3/WAV/OGG/M4A)                VIDEO (MP4/WebM/MOV)
         │                                       │
         ▼                                       ▼
  Gemini 1.5 Flash              HTMLVideoElement + Canvas
  (native audio base64)         6 key-frame extraction
         │                                       │
         │                               Gemini 1.5 Flash
         │                       (video base64 + jpg frames)
         └─────────────┬─────────────────────────┘
                       ▼
              10-layer analysis
              + detected transcription
              + Signal Card narrative
```

---

## 3. Capabilities

- **Real multimodal analysis:** image, text, audio, and video in one interface.
- **4-provider cascade** with automatic fallback on quota/rate limits.
- **Full ES/EN i18n** — 260+ translation keys, all dynamic modules included.
- **Signal Cards:** narrative copywriting anyone understands without technical training.
- **Zero backend:** runs on any phone from a single HTML file.
- **17 countries covered** with curated cultural context + real-time AI generation.

### Competitive positioning

```
              MEMELOGÍA OS vs ALTERNATIVES

              High ◄──────────────────► Low
Analytical    ████████████████ Memelogía OS
depth         ████████████ Palantir
              ████████ ChatGPT
              ████ Brandwatch
              ██ KnowYourMeme

Accessibility ████████████████ Memelogía OS
for non-exp.  ██████████ ChatGPT
              ████ Brandwatch
              ██ Palantir
              █ KnowYourMeme

Implementation████████████████ Memelogía OS (low)
cost          ██████████ ChatGPT (low)
              ████ Brandwatch (medium-high)
              ██ Palantir (enterprise)
```

---

## 4. Deployment

### Prerequisites

- A GitHub account
- A Cloudflare account (free tier)
- At least one API key from: Anthropic / Google Gemini / xAI Grok / OpenAI

### Deploy in 5 minutes

**Step 1 — push to a repo**
```bash
git init
git add .
git commit -m "feat: Memelogía OS v9.0"
git remote add origin https://github.com/cuakzilla/memelogia-os.git
git branch -M main
git push -u origin main
```

**Step 2 — connect Cloudflare Pages**
1. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → Pages
2. "Create a project" → "Connect to Git"
3. Select the `memelogia-os` repo
4. Settings:
   - **Framework preset:** None
   - **Build command:** *(empty)*
   - **Build output directory:** *(empty or `/`)*
5. "Save and Deploy"

**Step 3 — your URL is live** (e.g. `https://memelogia-os.pages.dev`)

**Step 4 — configure API keys in the app**
Open your deploy URL and enter your API key in the onboarding, or any time via the "APIs" button (Anthropic, Gemini, Grok, OpenAI).

**Auto-deploy:** every `git push` to `main` redeploys in ~30 seconds.

### Local testing

```bash
python -m http.server 8080   # then open http://localhost:8080
```

### Environment variables

There are none — API keys are entered by the user directly in the interface and stored in the browser's `localStorage`. No server-side exposure.

### Repository layout

```
memelogia-os/
├── index.html          ← the entire application
├── _headers            ← security headers (Cloudflare)
├── _redirects          ← SPA redirect (Cloudflare)
├── README.md
├── SECURITY.md · CONTRIBUTING.md · CHANGELOG.md
├── MANUAL_USUARIO.md · GUIA_INICIO.md · GUIA_PROBLEMAS.md · GUIA_CLIENTE.md
└── .gitignore
```

---

## License

Proprietary — all rights reserved. Developed by **A51 · cuakzilla** — 2026.
See `LICENSE`.
