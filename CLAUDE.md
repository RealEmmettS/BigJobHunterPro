# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Big Job Hunter Pro is a static landing page for a gamified job tracking application concept. The site uses a 90s arcade hunting game aesthetic ("Big Buck Hunter meets The Office") to promote a job search tool that rewards effort, maintains streaks, and enables social competition through leaderboards.

**Domain:** bigjobhunter.pro
**Status:** Marketing/concept landing page only (no backend functionality yet)

## Tech Stack

- **Frontend:** Vanilla HTML, CSS, JavaScript (no build tools or frameworks)
- **Fonts:** Google Fonts (Press Start 2P for pixel headers, Inter for body text)
- **Assets:** Static images in `/imgs` directory

## Development

To run locally, serve the files with any static server:
```bash
# Python
python -m http.server 8000

# Node.js (npx)
npx serve

# VS Code Live Server extension also works
```

## File Structure

| File | Purpose |
|------|---------|
| `index.html` | Landing page with hero, features, screenshots, CTA sections |
| `styles.css` | All styling including CRT scanline effects, arcade-button components, responsive design |
| `script.js` | Interactions: modal, animated counters, parallax, Konami code easter egg |
| `concept.md` | Full product concept document with design specifications |
| `imgs/` | Marketing screenshots (Title.png, dashboard.png, Jts.png) |

## Design System

### Color Palette (defined as CSS variables in `:root`)
- `--forest-green: #2E4600` - Background accent
- `--blaze-orange: #FF6700` - Primary CTA/highlight
- `--crt-amber: #FFB000` - Score displays/emphasis
- `--terminal-green: #00FF00` - Status text
- `--charcoal: #1a1a1a` - Dark backgrounds

### Key CSS Classes
- `.pixel-title`, `.pixel-header`, `.pixel-text` - Press Start 2P font styling
- `.arcade-button` - Chunky arcade-style buttons with glow effects
- `.scanlines` - CRT overlay effect (fixed position, z-index 9999)

### Naming Conventions (from concept)
UI uses hunting/arcade metaphors:
- "The Lodge" = Dashboard
- "The Armory" = Application tracker
- "Hunting Party" = Friend groups
- "Target Acquisition" = New job application

## JavaScript Features

- **Modal:** `showComingSoon()` / `closeModal()` for the "coming soon" overlay
- **Animated Counters:** Uses IntersectionObserver to animate stat numbers when scrolled into view
- **Parallax:** Hero image moves on scroll
- **Easter Egg:** Konami code (↑↑↓↓←→←→BA) triggers rainbow mode
- **Accessibility:** Respects `prefers-reduced-motion` media query
