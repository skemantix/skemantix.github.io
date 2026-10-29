# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page website for skemantix.com, web systems, commerce and AI integration (Seb Grinham). It is hosted on GitHub Pages with a custom domain configured via the CNAME file.

## Architecture

- **No build system**: Pure static HTML/CSS with no bundling, transpilation, or package manager
- **Single page**: `index.html` is the only page
- **Styling**: `css/style.css` uses vanilla CSS (colour tokens on `:root`, dark mode via `prefers-color-scheme`) with Lato from Google Fonts
- **Images**: Stored in `img/` directory
- **Analytics**: none. The old Universal Analytics tag (UA-669094-1) was removed in the 2026-10 refresh; UA stopped collecting data in July 2023
- **Email**: the mailto is assembled by a small inline script from `data-u` / `data-d`; the markup holds only "seb at skemantix dot com"

## Development

To preview locally, open `index.html` directly in a browser or use any static file server:

```bash
python3 -m http.server 8000
```

## Deployment

Push to `master` branch. GitHub Pages automatically serves the site at skemantix.com (configured via CNAME).
