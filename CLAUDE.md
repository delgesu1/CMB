# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Chamber Music Boise - a static website for a classical chamber music concert series in Boise, Idaho.

## Tech Stack

- **Pure HTML** - No framework, no build process
- **Tailwind CSS v4** - Loaded via CDN browser build (`@tailwindcss/browser@4`)
- **Lucide Icons** - Via CDN
- **Google Fonts** - Italiana, Cinzel, Cormorant Garamond, Montserrat

## Architecture

This is a fully static site with no backend. All styling and JavaScript is embedded inline within each HTML file.

### Pages
- `index.html` - Main landing page (hero, about, season, news, gallery, donate, contact)
- `artists.html` - Artist bios and photos
- `venues.html` - Venue information with expandable details

### Content Storage
- All text content is hardcoded directly in HTML files
- `Photos/` - Performance and promotional images
- `Artist Bios and photos/` - Source documents (.docx, .pdf) and headshots
- `Series Blurbs/` - Venue/series descriptions as source documents

### Design System

CSS custom properties defined in `:root` within each HTML file's `<style>` block:
- Primary accent: `--gold-primary` (terracotta #a65d4f)
- Secondary accent: `--teal` (forest teal #3d6b5f)
- Typography: `--text-dark`, `--text-medium`, `--text-light`, `--text-muted`
- Backgrounds: `--ivory`, `--cream`, `--charcoal`

Typography classes:
- `font-cormorant` - Elegant italic accent font
- `font-montserrat` - Clean body text (default)
- Cinzel/Italiana used sparingly for display

## Development

No build step required. Open HTML files directly in browser or use any local server:

```bash
python3 -m http.server 8000
```

## Editing Content

To update copy, edit the HTML files directly. Key sections in `index.html`:
- Hero tagline: ~line 742
- About/Mission section: ~lines 785-812
- Event cards: ~lines 900-1000
- Gallery captions: ~lines 1220-1300
