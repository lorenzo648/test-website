# AGENTS.md

This file provides guidance to Codex (Codex.ai/code) when working with code in this repository.

## Project Overview

Akdo marketing website — a static HTML prototype for an AI-powered HSE (Health, Safety & Environment) and sustainability training platform. These HTML pages serve as drafts that will be copy-pasted into **Framer** for final deployment (not deployed as static HTML).

## Architecture

- **Pure static HTML** — no build system, no bundler, no package.json, no tests
- **Tailwind CSS** via CDN (`cdn.tailwindcss.com`) with inline config defining the Akdo brand palette
- **Google Fonts** — Poppins (weights 300–900)
- Each page is a self-contained `.html` file with its own `<style>` block and inline Tailwind config
- Single shared asset: `assets/logo.png`

## Brand Color Palette (Tailwind config)

| Token | Hex |
|-------|-----|
| `akdo-dark` | `#02140d` |
| `akdo-green` | `#2cc27d` |
| `akdo-lime` | `#83e85a` |
| `akdo-cream` | `#f5f6f4` |
| `akdo-peach` | `#ffc091` |
| `akdo-yellow` | `#fee581` |

## Pages

- `index.html` — Homepage
- `hse-training.html` — HSE/EHS training product page
- `sustainability.html` — ESG/sustainability training page
- `training-library.html` — Course catalog
- `training-library-course.html` — Individual course detail template
- `security.html` — Security & compliance (ISO 27001, GDPR, SOC 2)
- `book-demo.html` — Demo booking form
- `contact.html` — Contact page
- `careers.html` — Careers page

## SEO/AEO Strategy

The site has a detailed SEO and AEO (Answer Engine Optimization) strategy documented in:
- `KEYWORDS.md` — Full keyword strategy with tiered keywords per page
- `SEO_AEO_PLAN.md` — Implementation plan, distinguishing what goes in the HTML draft vs. what is configured in Framer
- `SEO_REFERENCE.md` — Title tags and meta descriptions for Framer settings

Key constraints when editing copy:
- Use both **HSE** (European) and **EHS** (American) terminology for global reach
- Never reference VR/immersive features — Akdo has none
- Target ICP: Head of Safety / Regional HSE Director at Fortune Global 2000 companies
- Preserve keyword placement in H1s, H2s, and FAQ sections per `KEYWORDS.md`

## Development

To preview, open any `.html` file directly in a browser. No server or build step needed. The Tailwind CDN script handles utility classes at runtime.

## Framer Deployment Note

Content changes (headings, body copy, FAQ text) are made in these HTML drafts. Configuration like title tags, meta descriptions, OG tags, structured data (JSON-LD), sitemaps, and canonical URLs are set in Framer directly — not in these files.
