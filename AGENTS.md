# AGENTS.md

## Cursor Cloud specific instructions

This is a zero-dependency, single-file static web application (`index.html`). There is no build step, no package manager, and no backend.

### Running the app

Serve `index.html` with any static HTTP server:

```
python3 -m http.server 8080 --directory /workspace
```

Then open `http://localhost:8080/index.html` in a browser.

### External CDN dependencies

The app loads two external resources at runtime:
- **GSAP 3.12.2** from `cdnjs.cloudflare.com`
- **Lexend font** from `fonts.googleapis.com`

Internet connectivity is required for full functionality (animations and custom font).

### Testing notes

- There are no automated tests, linter, or build commands in this repo.
- Manual browser testing is the only verification method. Open the app and interact with the grid cards and altar screen.
- The GSAP entrance animation for the altar screen may not complete correctly in headless or automated browser environments. Use a full Chrome instance for reliable testing.
