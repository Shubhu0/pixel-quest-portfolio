# Pixel Quest Portfolio

An interactive, side-scrolling 16-bit RPG that doubles as **Shubhankar Mishra's** personal portfolio. Walk a pixel-art developer hero through six themed biomes — each mapped to a résumé section — and interact with world objects to read the details.

Features:

- Parallax pixel world (~9320px wide) with a canvas-drawn hero and physics-based movement
- Six biomes (Home, Skills, Experience, Projects, About, Contact) with cross-fading palettes
- In-world dialogs, an RPG character-skills sheet, and a clean **Resume** read-mode
- Fast-travel "rift" portal between zones, a day/dusk/night toggle, and synthesized chiptune audio (muted by default)
- Mobile touch controls; fully self-contained in a single `index.html` (only external dependency is Google Fonts)
- Shareable deep links — append `#skills`, `#experience`, `#projects`, `#about`, or `#contact` to jump straight to a zone
- Remembers your theme and sound choice between visits

## Performance

The scene auto-detects a performance tier. On phones and low-end GPUs it runs a **lite** mode that drops the costliest full-screen blend/filter effects (CRT scanlines, biome tint, hill filters) and thins decoration, keeping movement smooth; desktops get the full effect set. Force a tier with a query param:

- `?perf=hi` — full effects everywhere
- `?perf=lite` — lite mode everywhere

## Controls

- **Walk:** ← → or A / D
- **Jump:** Space / ↑ / W
- **Interact:** E / Enter
- **Fast-travel:** top zone buttons · **Resume:** top-right button

## Run locally

It's a static page — open `index.html` in a browser, or serve the folder:

```bash
npx serve .
```

## Deploy to GitHub Pages

1. Push this folder to a GitHub repo (e.g. `Personal-Portfolio-Website`).
2. In **Settings → Pages**, set **Source** to *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. The site publishes at `https://<username>.github.io/<repo>/`.

`.nojekyll` is included so GitHub Pages serves the files as-is.
