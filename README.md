# TECH/FEST // Cyborg Protocol

A single-page, scroll-driven landing page concept for **Techfest, IIT Bombay**, built around one idea: *the line between human and machine is a design choice.*

One page covers four design briefs at once:

| Brief | Where to see it |
|---|---|
| Cyborg-themed responsive landing page | Hero: half-human, half-machine eye with a cursor-tracking pupil, glitch title, HUD elements |
| 3D interactive site with scroll animation | "Anatomy" section: a stack of layers rotates and explodes apart as you scroll; hover or click a layer |
| Parallax scrolling experience | Grid, orbit rings, floating chips and oversized outline text all move at different speeds |
| Techfest official-site landing page (no 3D assets) | Event arena, stats, legacy timeline and CTA, with content drawn from public Techfest information |

> **No 3D assets are used.** Every "3D" effect is made from CSS 3D transforms, SVG and `<canvas>`.

## Live demo

- Website: `https://<your-username>.github.io/<repo-name>/`
- Demo recording: `<add your Google Drive link here>`

## Features

- **Scroll-pinned 3D scene:** five octagonal layers (Neural, Optics, Signal, Actuators, Core) rotate on three axes and spread out with scroll progress, with captions that change per layer.
- **Multi-depth parallax:** layers shift at different speeds, driven by a smoothed scroll value.
- **Interactive objects:** the eye tracks the cursor and the head tilts in 3D; event cards tilt with a glare that follows the pointer.
- **Living background:** a `<canvas>` circuit network that reacts to the cursor.
- **Details:** animated stat counters, scroll-velocity marquee, scroll progress bar, reveal-on-scroll.
- **Responsive and accessible:** works down to phone widths, respects `prefers-reduced-motion`, and accounts for device safe areas.

## Tech stack

Plain HTML, CSS and vanilla JavaScript in one file. No build step and no dependencies.
Fonts: [Orbitron](https://fonts.google.com/specimen/Orbitron) and [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) via Google Fonts (system fonts are used as a fallback).

## Run locally

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
# open index.html in a browser, or serve it:
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploy with GitHub Pages

1. Push `index.html` and `README.md` to the `main` branch.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
4. After a minute the site is live at `https://<your-username>.github.io/<repo-name>/`.

## Project structure

```
.
├── index.html   # the whole site: markup, styles and scripts
└── README.md
```

## Customising

- **Colours:** edit the CSS variables at the top of `index.html` (`--cy`, `--mg`, `--am`).
- **3D layers:** edit the `L` array in the script to rename or add layers.
- **Stats and timeline:** edit the `data-n` values and the `.tl` block.
- **Dates:** the next edition's dates are not included; add them once announced on [techfest.org](https://www.techfest.org).

## Disclaimer

This is an unofficial student design concept inspired by Techfest, IIT Bombay. It is not affiliated with or endorsed by the festival. Figures and history are taken from publicly available Techfest information and may be out of date.
