# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page website for skemantix.com, a freelance web development business. It is hosted on GitHub Pages with a custom domain configured via the CNAME file.

## Architecture

- **No build system**: Pure static HTML/CSS with no bundling, transpilation, or package manager
- **Single page**: `index.html` is the only page
- **Styling**: `css/style.css` uses vanilla CSS with Lato font from Google Fonts
- **Images**: Stored in `img/` directory
- **Analytics**: Google Analytics (UA-669094-1) embedded in the HTML

## Development

To preview locally, open `index.html` directly in a browser or use any static file server:

```bash
python3 -m http.server 8000
```

## Deployment

Push to `master` branch. GitHub Pages automatically serves the site at skemantix.com (configured via CNAME).
