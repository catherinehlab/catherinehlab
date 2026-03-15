# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for **Catherine H. Lab** (프라이빗 파인다이닝 / private fine dining restaurant), hosted on **GitHub Pages** with custom domain `catherineh-lab.com`.

## Architecture

- **Single-file site**: The entire website is a single `index.html` (74 lines, ~416KB) exported from **Framer** (framer.com). It contains all HTML, CSS, and JS inline.
- **CNAME**: Maps to `catherineh-lab.com` for GitHub Pages custom domain.
- **.nojekyll**: Disables Jekyll processing on GitHub Pages.
- **Google Analytics**: Configured with tag `G-PMV5L94L3W`.
- **Language**: Korean (lang="en" in HTML but content is in Korean).

## Deployment

Push to `main` branch triggers GitHub Pages deployment automatically. No build step required.

## Key Considerations

- The `index.html` is machine-generated from Framer — it is not hand-authored. Direct edits to this file will be overwritten if the site is re-exported from Framer.
- For content changes, prefer updating in Framer and re-exporting, unless making quick hotfixes (e.g., analytics tags, meta tags, CNAME).
- The file is very large (~178K tokens) due to inlined assets and minified code. Use targeted searches (grep) rather than reading the whole file.
