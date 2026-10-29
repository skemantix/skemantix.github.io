# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page website for skemantix.com, web systems, commerce and AI integration (Seb Grinham). Since 2026-10-29 it is hosted on Cloudflare Workers Static Assets (Worker `skemantix`, account Skemantix), with `skemantix.com` and `www.skemantix.com` as Worker custom domains. It was previously on GitHub Pages.

## Architecture

- **No build system**: Pure static HTML/CSS with no bundling, transpilation, or package manager
- **Single page**: `index.html` is the only page
- **Styling**: `css/style.css` uses vanilla CSS (colour tokens on `:root`, dark mode via `prefers-color-scheme`) with Lato from Google Fonts
- **Images**: Stored in `img/` directory
- **Analytics**: Cloudflare Web Analytics, automatic setup (Cloudflare injects the beacon; nothing in the HTML). The old Universal Analytics tag was removed in the 2026-10 refresh
- **Email**: the mailto is assembled by a small inline script from `data-u` / `data-d`; the markup holds only "seb at skemantix dot com"

## Development

To preview locally, open `index.html` directly in a browser or use any static file server:

```bash
python3 -m http.server 8000
```

## Deployment

`npx wrangler deploy` from the repo root (needs `wrangler login` on the Skemantix account). Pushing to `master` does not deploy to Cloudflare. `.assetsignore` keeps repo-only files (notes, CNAME, wrangler.jsonc, .git) off the public site.
