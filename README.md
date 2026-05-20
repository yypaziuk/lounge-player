# 🎵 Lounge · Always On
 
> A beautiful internet radio player that never stops. Auto-reconnects on network changes, remembers your stations, and looks stunning doing it.
 
![Lounge Player](https://raw.githubusercontent.com/yypaziuk/lounge-player/main/preview.png)
 
## ✨ Features
 
### 🎨 Visual
- Spinning vinyl record with tonearm animation
- 6 spectacular themes that auto-change by time of day
- Golden Hour · Midnight Jazz · Velvet Bordeaux · Tokyo Neon · Cabin Fire · Arctic Aurora
- Ambient glow and sonar rings around the vinyl
- Drifting light particles in the background
- Glassmorphism UI panels
### 📻 Radio
- Search 50,000+ stations via Radio Browser
- One-click presets (SomaFM Groove Salad, Lush, Drone Zone and more)
- Add any stream URL manually
- Now Playing metadata (track & artist)
- Export / Import your station collection as JSON
### 🔄 Reliability
- Auto-reconnects on network change (WiFi ↔ Mobile)
- Exponential backoff retry (1.2s → 12s max)
- Watchdog timer detects silent stalls
- Cache-busting on every reconnect
- Wake Lock — screen stays on while playing
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
- Sleep timer (15m · 30m · 1h · 2h)
- Focus mode — fullscreen vinyl + clock
- Drag & drop station reorder
- Per-station vinyl label color
- PWA — installable as desktop/mobile app (on HTTPS)
- MediaSession API — works with headphone buttons
---
 
## 🚀 Quick Start
 
**Option A — Open locally**
1. Download `lounge-player.html`
2. Open in any modern browser
3. Click **+ Add** or pick a preset station
4. Press Play ▶
No server, no install, no dependencies. Just one HTML file.
 
**Option B — Live demo**
👉 [yypaziuk.github.io/lounge-player](https://yypaziuk.github.io/lounge-player)
 
---
 
## 🖥️ Screenshots
 
| Golden Hour | Tokyo Neon | Arctic Aurora |
|:-----------:|:----------:|:-------------:|
| warm sunset gradient | pink neon glow | northern lights |
 
---
 
## 🛠️ How it works
 
Single self-contained HTML file (~100KB). No frameworks, no build step, no npm.
 
- **Audio** — native `<audio>` element with ICY stream URLs
- **Reconnect logic** — `online/offline` events + stall watchdog
- **Themes** — CSS custom properties swapped on the fly
- **i18n** — pure JS translation table, 6 languages
- **Storage** — `localStorage` with in-memory fallback
- **Metadata** — SomaFM API + Icecast `status-json.xsl` polling
---
 
## 🤝 Contributing
 
Pull requests are welcome! Some ideas if you want to contribute:
 
- New themes
- New language translations
- Better Now Playing metadata support
- Bug fixes
- Mobile UX improvements
1. Fork the repo
2. Make your changes in `lounge-player.html`
3. Open a Pull Request with a short description
---
 
## 📄 License
 
MIT — free to use, modify and share.
 
---
 
<div align="center">
  Made with ♥ and good music
  <br>
  <a href="https://github.com/yypaziuk/lounge-player/stargazers">⭐ Star if you like it</a>
</div>
