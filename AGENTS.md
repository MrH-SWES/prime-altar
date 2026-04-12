# AGENTS.md

## Cursor Cloud specific instructions

### Project overview
This is **Prime Altar / Math Things** — a self-contained, static single-page web app for interactive math education (prime factorization and number composition). There are no build tools, package managers, or backend services.

### Key files
- `index.html` — The main app (all HTML/CSS/JS in one file)
- `archive.html` — An earlier version of the app

### External CDN dependencies
- **GSAP 3.12.2** (animations) — loaded from `cdnjs.cloudflare.com`
- **Google Fonts (Lexend)** — loaded from `fonts.googleapis.com`

### Running the app
Serve the project root with any static HTTP server:
```
python3 -m http.server 8080 --directory /workspace
```
Then open `http://localhost:8080/index.html` in a browser.

### Lint / Test / Build
There are no lint, test, or build commands — this is a plain HTML/CSS/JS project with no tooling.

### Gotchas
- The app uses `pointer` events, `navigator.vibrate`, and GSAP animations — test in a browser (not curl/headless).
- All state is in-memory; reloading the page resets progress.
- Numbers 1–12 are unlocked by default; higher numbers unlock progressively.
