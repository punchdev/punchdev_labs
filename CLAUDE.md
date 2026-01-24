# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static marketing site for punchDev—a supplement brand for developers. Single-page application built with vanilla HTML, Tailwind CSS (CDN), and Lucide icons.

## Architecture

- **index.html**: Self-contained single-page application
  - Tailwind CSS via CDN (inline config for custom `punch` color palette)
  - Custom fonts: Inter (sans), JetBrains Mono (mono)
  - Lucide icons for UI elements
  - Dark-mode terminal aesthetic with scanline effect
  - Three product cards: git push (focus), localhost:3000 (daily), nightly build (sleep)

- **brand_identity.pdf**: Brand guidelines (3 pages)

## Design System

Color palette (defined in Tailwind config):
- `punch-bg`: #020617 (background)
- `punch-card`: #0f172a (card backgrounds)
- `punch-border`: #1e293b (borders)
- `punch-primary`: #6366f1 (indigo—primary actions)
- `punch-accent`: #d946ef (fuchsia—accents)
- `punch-success`: #34d399 (emerald—success states)

Custom animations: `pulse-slow`, `float`, `scanline`

## Development

No build process. Open `index.html` directly in browser or serve via local HTTP server:

```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve
```

## Content Structure

1. Hero: Value proposition + code snippet
2. Products: Three supplement offerings (modular cards)
3. Social proof: Terminal-style testimonials
4. Footer: Navigation links

## Constraints

- All dependencies loaded via CDN (no npm/package.json)
- No JavaScript framework—vanilla JS for Lucide icon initialization only
- Single-file architecture—all styles inline
