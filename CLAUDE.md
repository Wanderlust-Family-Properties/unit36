# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A single-file static vacation rental listing page for **Beach Bliss Retreat** — a 2BR/2.5BA townhouse in Indian Rocks/Indian Shores, Florida (Airbnb listing `1413996032984261454`). Host: Elizabeth.

There is no build system, no package manager, and no dependencies. All HTML, CSS, and JavaScript live in `index.html`. All images are AVIF files in the root directory.

## Development

Open `index.html` directly in a browser, or serve the root with any static server:

```bash
python3 -m http.server
```

No build step, no transpilation, no tests.

## Architecture

Everything is self-contained in `index.html` (~1,738 lines):

- **CSS** (lines 20–901): All styles are inline `<style>` blocks. Design tokens are CSS custom properties on `:root` (colors, fonts, radii, shadows). Two blocks: main styles then a second block for the weather widget.
- **HTML** (lines 903–1604): Sections in order — lightbox overlay, mobile menu overlay, nav, hero, highlights strip, about, gallery, amenities, reviews, location (with weather card + OpenStreetMap iframe), house rules, evacuation info, booking CTA, footer.
- **JS** (lines 1605–1734): One inline `<script>` at the bottom handling: nav scroll state, `IntersectionObserver` for `.fade-up` animations, mobile menu toggle, lightbox (opens from `.gm-item` clicks, keyboard nav via arrow keys/Escape), and live weather via the key-free Open-Meteo API (lat `27.8833`, lon `-82.8482`).

## Key conventions

**CSS tokens** — all colors, font families, border radii, and shadows are referenced via `var(--token-name)`. The palette is coastal: `--navy`, `--ocean`, `--sky`, `--teal`, `--sand`, `--coral`, `--gold`. Always use tokens rather than hardcoded values.

**Images** — all photos are `.avif` format. Filenames follow the pattern `unit36_<room/feature>.avif`. Hero images use `loading="eager"`; everything else uses `loading="lazy"`.

**Responsive breakpoints** — `1100px` (amenities grid), `1024px` (nav collapses to hamburger, hero stacks, single-column layouts), `640px` (full mobile).

**Fade animations** — add class `fade-up` to any new element and the `IntersectionObserver` will animate it in on scroll. No extra JS needed.

**Section IDs** — nav links and footer anchor to `#about`, `#gallery`, `#amenities`, `#reviews`, `#location`, `#evacuation`, `#book`.

## Known placeholder

Line 1554 has a comment marking where the Indian Shores official evacuation page URL should go once it's available:
```html
<!-- ⬇ Replace with the Indian Shores official evacuation URL when available -->
```
