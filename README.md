# 🎵 Lounge · Always On

> A beautiful internet radio player that never stops. Auto-reconnects on network changes, remembers your stations, and looks stunning doing it.

![Lounge Player](https://raw.githubusercontent.com/yypaziuk/lounge-player/main/preview.png)

**Two editions, one file each — no frameworks, no build step, no npm.**

| | Free | Pro · $3 |
|---|------|----------|
| File | `player.html` | `pro.html` |
| Themes | 6 | **14** |
| Atmosphere effects | core | **15 controls** |
| Profiles | — | **3 (Work / Evening / Weekend)** |
| Curated collections | — | **9** |
| Station groups | — | ✓ |
| Favorites · History | — | ✓ |
| Wake-up alarm | — | ✓ |
| Station artwork | — | ✓ |
| Crossfade · sleep fade-out | — | ✓ |
| Full backup &amp; restore | basic (stations) | **everything (profiles, themes, settings)** |
| Android APK · Windows desktop | — | ✓ |

👉 **Get Pro:** [yypaziuk.gumroad.com/l/lounge-player](https://yypaziuk.gumroad.com/l/lounge-player) — one-time $3, free updates forever.

---

## ✨ Features

### 🎨 Visual
- Spinning vinyl record with tonearm animation
- **14 themes** that can auto-change by time of day
  - **Free (6):** Golden Hour · Midnight Jazz · Velvet Bordeaux · Tokyo Neon · Cabin Fire · Arctic Aurora
  - **Pro (8):** Monsoon Rain · Cozy Library · Cognac & Oak · Nebula Dream · Sakura Dawn · Synthwave · Abyssal Ocean · Noir Velvet
- **One-tap mood presets** — Cozy Evening · Rainy Window · Starlit · Golden Calm · Aurora Night · Reading Room: each sets a theme + a tasteful blend of effects in one tap
- **Atmosphere panel — 15 layered effects:** drifting dust, mote size, halo glow, sonar rings, film grain, breathing gradient, vinyl spin, aurora ribbons, starfield + shooting stars, rain, bokeh orbs, vignette, **god rays (warm light shafts), parallax depth (layers follow your mouse / device tilt), liquid gradient mesh (flowing, theme-tinted)**
- **Living vinyl** — softly breathing shadow, a slow lamplight glint, and a warm bloom when playback begins
- **Procedural vinyl-crackle ambient** (Web Audio) — optional, off by default
- **Warm first-run default** + a **time-of-day greeting** when the record is at rest
- Glassmorphism UI panels
- Respects `prefers-reduced-motion`

### 📻 Radio
- Search 50,000+ stations via Radio Browser (with automatic mirror fallback)
- One-click presets (SomaFM Groove Salad, Lush, Drone Zone and more)
- Add any stream URL manually
- Now Playing metadata (track & artist)
- Export / Import your station collection as JSON (Pro: full backup of everything)

### 🔄 Reliability
- Auto-reconnects on network change (WiFi ↔ Mobile)
- Exponential backoff retry (1.2s → 12s max)
- After repeated failures a station is flagged **⚠ offline** with a prompt to switch
- Mixed-content guard — warns when an `http://` stream is blocked on an `https://` page
- Watchdog timer detects silent stalls
- Cache-busting on every reconnect
- Wake Lock — screen stays on while playing

### 💎 Pro extras
- **3 Profiles** — Work / Evening / Weekend, each with its own stations + theme
- **8 extra themes**, **mood presets**, the full **15-effect atmosphere panel** (incl. god rays, parallax depth, liquid mesh) and **vinyl-crackle ambient**
- **9 Curated collections** with one-tap add (each a unique, hand-checked set)
- **Station groups** — tag stations into your own groups, filter and collapse them, manage groups in one place
- **Favorites** ★ with filter, and **History** of the last played stations
- **Wake-up alarm** — fires a station at a set time (native mobile time picker)
- **Custom station artwork** on the vinyl label
- **Crossfade** between stations and **gradual fade-out** as the sleep timer ends
- **Full backup & restore** — export *everything* (stations, profiles, themes, all settings) to a single JSON file and restore it on any device
- **Service worker** for offline/PWA support
- **Android APK** (Capacitor) and **Windows desktop** (Electron — single-instance tray app + global media keys)

### 🌍 Multilingual
- 🇺🇦 Українська · 🇬🇧 English · 🇩🇪 Deutsch · 🇫🇷 Français · 🇪🇸 Español · 🇵🇱 Polski
- Auto-detects browser language on first launch

### ⌨️ Controls
| Key | Action |
|-----|--------|
| `Space` | Play / Pause |
| `← →` | Previous / Next station |
| `↑ ↓` | Volume |
| `M` | Mute |
| `A` | Search station |
| `F` | Focus / Screensaver mode |
| `T` | Next theme |
| `?` | Shortcuts help |

### 💤 Other
- Sleep timer (15m · 30m · 1h · 2h) with gentle fade-out
- Focus mode — fullscreen vinyl + clock
- Drag & drop station reorder
- PWA — installable as desktop/mobile app (on HTTPS)
- MediaSession API — works with headphone buttons

---

## 🚀 Quick Start

**Option A — Open locally**
1. Download `player.html` (Free), or get `pro.html` on [Gumroad](https://yypaziuk.gumroad.com/l/lounge-player) (Pro)
2. Open in any modern browser
3. Click **+ Add** or pick a preset station
4. Press Play ▶

No server, no install, no dependencies. Just one HTML file.

**Option B — Live demo**
👉 [yypaziuk.github.io/lounge-player](https://yypaziuk.github.io/lounge-player)
- Free player: [`/player.html`](https://yypaziuk.github.io/lounge-player/player.html)
- Pro is available on [Gumroad](https://yypaziuk.gumroad.com/l/lounge-player) (one-time $3)

---

## 🛠️ How it works

Single self-contained HTML file. No frameworks, no build step, no npm.

- **Audio** — native `<audio>` element with ICY stream URLs
- **Reconnect logic** — `online/offline` events + stall watchdog + offline-station detection
- **Search** — Radio Browser API across rotating mirrors (de2 → de1 → nl1 → at1)
- **Themes & effects** — CSS custom properties + body data-attributes swapped on the fly
- **Vinyl crackle** — procedurally generated noise buffer via the Web Audio API (no audio files)
- **i18n** — pure JS translation table, 6 languages
- **Storage** — `localStorage` with in-memory fallback
- **Metadata** — SomaFM API + Icecast `status-json.xsl` polling
- **Desktop/mobile builds** — same `pro.html` wrapped via Electron (Windows) and Capacitor (Android)

---

## 🤝 Contributing

Pull requests are welcome! Some ideas if you want to contribute:

- New themes or atmosphere effects
- New language translations
- Better Now Playing metadata support
- Bug fixes & mobile UX improvements

1. Fork the repo
2. Make your changes in `player.html` (Free)
3. Open a Pull Request with a short description

---

## 📄 License

The **Free** edition (`player.html`) is released under the **MIT** license — free to use, modify and share.
The **Pro** edition (`pro.html`) is a commercial product; buying it supports development and gets you free updates forever.

---

<div align="center">
  Made with ♥ and good music
  <br>
  <a href="https://github.com/yypaziuk/lounge-player/stargazers">⭐ Star if you like it</a>
</div>
