# CLAUDE.md

## Project Context

This is a productized agency website styled to look and feel like a SaaS product.
We iterate on design in code (fast, with Claude Code), then port sections into
Framer using the "HTML to Framer" Chrome extension. The code here is NOT production
— it's a high-fidelity design reference optimized for clean Framer import.

## Brand

### Colors
- **Deep Teal (primary background, dark sections):** #113333
- **Green (primary accent, CTAs, highlights):** #2CC27D
- **Bright Green (secondary accent, gradients, hover states):** #83E85A
- **White:** #FFFFFF
- **Off-white (light backgrounds):** #F5F7F5
- **Light gray (borders, dividers):** #E0E5E0
- **Medium gray (secondary text):** #6B7B6B
- **Dark (text on light backgrounds):** #0D2626

### Gradient
No gradients on buttons or text — ever. Gradients are only used for radial dark
section backgrounds. Two standard dark radial gradients:
- **Default dark:** `radial-gradient(ellipse at 50% 0%, #153d30 0%, #0E2B2B 60%, #091E1E 100%)`
- **Offset dark (banners):** `radial-gradient(ellipse at 70% 50%, #153d30 0%, #0E2B2B 60%, #091E1E 100%)`
All CTAs use flat solid #83E85A.

### Typography
- **Font family:** Poppins (load from Google Fonts)
- **Weights:** 400 (body), 500 (UI elements), 600 (subheadings), 700 (headings, stats). Never use 800 or 900.
- **Scale:**
  - h1 (hero): 64px / 700 / line-height 1.15 / letter-spacing -1px / max-width 860px
  - h2: 40px / 700
  - h3: 28px / 600
  - h4: 22px / 600
  - body: 17px / 400
  - body-small: 15px / 400
  - caption: 13px / 500
- **Line heights:** h1 hero 1.15, other headings 1.2, body 1.6
- **Letter spacing:** h1 hero -1px, other headings -0.5px, body 0
- **Hero h1 is the same on every page** — 64px, 700, line-height 1.15, letter-spacing -1px. No smaller subpage variants.

### Spacing Scale (px only)
4, 8, 12, 16, 24, 32, 48, 64, 80, 120

### Border Radius
- Buttons: 8px
- Cards: 12px
- Large containers: 16px
- Pills/tags: 100px

### Shadows
- Card shadow: 0 2px 8px rgba(17, 51, 51, 0.08)
- Elevated shadow: 0 8px 24px rgba(17, 51, 51, 0.12)
- Hover lift: 0 12px 32px rgba(17, 51, 51, 0.16)

## Visual Direction

This should feel like a polished SaaS product page — clean, confident, modern.
Think Linear, Vercel, Raycast — not a typical agency portfolio. Key traits:

- **Confident whitespace** — let sections breathe, don't cram
- **Strong typographic hierarchy** — big bold headings, smaller calm body text
- **Subtle depth** — light shadows, slight background color shifts between sections
- **Green as the action color** — CTAs, highlights, active states use the green
- **Dark sections** — use #113333 for hero and key emphasis sections with white/green text
- **Light sections** — use #F5F7F5 or white with dark text for content-heavy sections
- **Alternate dark/light** — create rhythm by alternating section backgrounds

## Framer-Compatible Code Rules (CRITICAL)

Every line of HTML/CSS must be written with Framer import in mind:

1. **Flexbox only** — no CSS Grid anywhere. Framer's layout engine is flexbox.
2. **Shallow DOM** — max 4 levels of nesting. Fewer divs = cleaner Framer layers.
3. **Explicit px values** — all widths, heights, padding, margins, gaps in px.
   No rem, em, %, calc(), clamp(), or min/max. The only exception is
   max-width on containers (use px there too).
4. **No CSS variables** — Framer reads computed styles. Write actual values
   everywhere (#113333 not var(--primary)).
5. **No Tailwind classes** — write plain CSS in a stylesheet or style tags.
   Framer needs to see real CSS properties.
6. **Self-contained sections** — each section (hero, features, pricing, etc.)
   must be a single parent element with no external layout dependencies.
   Every section should be independently copy-pasteable.
7. **Simple img tags** — use `<img>` with explicit width and height attributes.
   No background-image for content images. No srcset or picture element.
8. **No JS-dependent layouts** — everything must look correct as static HTML/CSS.
   No intersection observers, no scroll-triggered layout changes, no
   dynamically computed positions.
9. **Standard CSS properties** — avoid vendor prefixes, CSS nesting, or
   modern CSS features that may not compute cleanly (container queries,
   :has(), etc.)
10. **Font loading** — include Google Fonts link in the head. Don't rely on
    @font-face or local fonts.

## Section Structure Template

Every section should follow this pattern:

```html
<section style="display: flex; flex-direction: column; align-items: center; padding: 80px 24px; background: #FFFFFF;">
  <div style="display: flex; flex-direction: column; align-items: center; max-width: 1200px; width: 1200px; gap: 48px;">
    <!-- Section heading group -->
    <div style="display: flex; flex-direction: column; align-items: center; gap: 16px; max-width: 680px;">
      <h2 style="font-family: Poppins; font-size: 40px; font-weight: 700; color: #0D2626; line-height: 1.2; letter-spacing: -0.5px; text-align: center; margin: 0;">
        Section Title
      </h2>
      <p style="font-family: Poppins; font-size: 17px; font-weight: 400; color: #6B7B6B; line-height: 1.6; text-align: center; margin: 0;">
        Section description text goes here.
      </p>
    </div>
    <!-- Section content -->
    <div style="display: flex; gap: 24px;">
      <!-- Cards, features, etc -->
    </div>
  </div>
</section>
```

## Component Patterns

### Buttons

**Primary CTA (solid green — same color everywhere):**
- background: #83E85A
- color: #113333
- font: Poppins 15px / 600
- padding: 14px 28px
- border-radius: 8px
- No shadow at rest. Clean and flat.
- No gradients on buttons — ever. Flat solid #83E85A only.
- One primary button per section max.

**Secondary / Ghost:**
- background: transparent
- border: 1px solid #E0E5E0 (on light bg) or 1px solid rgba(255,255,255,0.2) (on dark bg)
- color: #0D2626 (light bg) or #FFFFFF (dark bg)
- Same size/radius as primary

Secondary buttons are always ghost.

### Cards

**Light card (on white/off-white bg):**
- background: #FFFFFF
- border: 1px solid rgba(0,0,0,0.08)
- border-radius: 12px
- padding: 24px–32px
- shadow: 0 2px 8px rgba(17,51,51,0.06)
- No colored borders (no green left/top borders on cards — ever)

**Dark card (on dark bg):**
- background: rgba(255,255,255,0.06)
- border: 1px solid rgba(255,255,255,0.1)
- border-radius: 12px
- padding: 32px
- No shadow

### Eyebrow Labels
Two types — never mix them up:

**Section eyebrow** (above a section heading):
- font: Poppins 12px / 600
- text-transform: uppercase, letter-spacing: 0.12em
- color on light bg: #2cc27d (darker green)
- color on dark bg: #83E85A (bright green)
- margin-bottom: 12px

**Card eyebrow** (inside a card):
- font: Poppins 12px / 600
- color: #83E85A (on ALL backgrounds — light and dark)
- text-transform: uppercase
- letter-spacing: 0.15em
- margin-bottom: 8px–12px

### Icon Placeholders (for Framer swap)
- 36px × 36px container, border-radius: 8px
- background: rgba(44,194,125,0.1)
- Centered emoji at 18px (e.g. 🔌 🌐 🔄 📊)
- margin-bottom: 14px
- These get replaced with proper icons in Framer

### Stat Cards
- Big number: 42px / 900, color #0D2626 (light bg) or #FFFFFF (dark bg)
- Never use green for stat numbers — always white on dark, dark on light
- Label below: 15px / 400, #6B7B6B (light bg) or rgba(255,255,255,0.65) (dark bg)

### Tags / Pills

- background: rgba(44,194,125,0.1)
- color: #2CC27D
- font: 13px / 500
- padding: 6px 16px
- border-radius: 100px
- On dark backgrounds: background rgba(44,194,125,0.15)

### Hover / Interaction Rules (CSS classes for design reference)
- **Primary button hover:** brightness(1.1) + translateY(-1px)
- **Ghost button hover (dark bg):** background rgba(255,255,255,0.1), border rgba(255,255,255,0.4)
- **Ghost button hover (green):** background rgba(131,232,90,0.1), border rgba(131,232,90,0.5)
- **Inline links with arrow (`.link-arrow`):** only the arrow SVG slides right (translateX 5px). No opacity change, no color change.
- **Clickable card links (`.card-link`):** only the `.card-link-arrow` element moves (translateX 6px). Never apply opacity hover to the whole card. Never move card content — only the arrow.
- **No opacity hover** on cards or card-level links — ever.

### Form Inputs

- height: 48px
- padding: 0 12px
- border: 1px solid #E0E5E0
- border-radius: 8px
- font: Poppins 17px / 400
- Focus: border-color #2CC27D

## Spacing Application

| Use | Value |
|-----|-------|
| Hero vertical padding | 120px top, 80px bottom |
| Section vertical padding | 80px top and bottom |
| Section horizontal padding | 24px (outer gutter) |
| Inner container width | 1200px max-width |
| Section title → content gap | 48px |
| Heading → subheading gap | 16px |
| Card grid gap | 24px |
| Card internal padding | 32px |
| Between card elements | 16px |
| Button padding | 14px 28px |
| Tag/pill padding | 6px 16px |
| Nav height | 64px |
| Footer vertical padding | 64px |
| Max heading text width | 680px (centered) |
| Max body text width | 600px |

## Section Patterns

### Nav (fixed, white)
- Fixed top, white background, 64px height
- Logo left, links center (17px / 500, #0D2626), "Book a Demo" CTA right
- Bottom border: 1px solid #E0E5E0
- No backdrop-blur, no transparency — plain solid white

### Hero
- Hero can be dark (radial gradient) or light (#FFFFFF) depending on the page
- Centered layout, max-width for text
- h1: 64px / 700 / line-height 1.15 / letter-spacing -1px — same on every page
- Accent words: #2cc27d on light bg, #83E85A on dark bg
- Pill eyebrow above h1 (green dot + label) on light heroes
- No glow orbs, no grain textures, no animations

### Features / Pillars (light or dark, alternating)
- 3-column card layout (flexbox, gap 24px)
- Each card: 12px radius, 32px padding
- Placeholder icon box at top (emoji on green-tinted pill)
- h3 title + body-small description

### How It Works (dark section)
- Horizontal 4-step flow in a single flex row
- Each step: green circle (40px) with number + h4 title + body-small desc
- Steps connected by a 2px green horizontal line

### Comparison Table (light section)
- Flexbox table — header row + data rows
- 3 columns, Akdo column highlighted with green header bg (#2cc27d) and subtle tinted cell bg (rgba(44,194,125,0.05))
- Checkmarks as green "✓", x-marks as gray "—"
- Light rgba(0,0,0,0.08) row dividers only

### Social Proof / Customer Proof (light section, #F5F7F5)
- Dark radial gradient inner card for the quote
- Full-width quote text at 22px / 400 italic, all white — no green highlights in quotes
- Decorative oversized `"` mark as visual filler
- Stat cards in a horizontal row below: big number (42px / 900 white), label (15px / rgba 0.65)
- All stat numbers same color (white on dark) — never highlight individual stats in green

### CTA Band (off-white #F5F7F5)
- Centered text, max-width 600px
- h2 + body + single solid #83E85A CTA button
- Accent word in heading uses #2cc27d (solid, not gradient)
- 80px vertical padding
- No blur orbs, no decorative elements

### Footer (dark, #0E2B2B)
- Logo, links, copyright — centered or row layout
- 64px vertical padding
- Links: body-small, rgba(255,255,255,0.65)
- Copyright / tertiary text: rgba(255,255,255,0.65)

### Form Pages (book-demo, contact)
- Two-column: left content/value prop, right form card
- Form card: white bg, 1px #E0E5E0 border, 12px radius, 32px padding
- Submit: full-width primary solid #83E85A button

### Course Cards (training library)
- 3-column flexbox layout with flex-wrap
- White bg, 12px radius, 1px rgba(0,0,0,0.08) border
- Category pill tag at top, h3 course name, body-small description
- Industry tags at bottom as small pills
- Padding: 24px

## Text Colors by Context

| Context | Element | Color |
|---------|---------|-------|
| Light bg | Heading | #0D2626 |
| Light bg | Body | #0D2626 |
| Light bg | Secondary text | #6B7B6B |
| Light bg | Section eyebrow label | #2CC27D |
| Light bg | Card eyebrow label | #83E85A |
| Light bg | Accent text in headings | #2CC27D |
| Dark bg | Heading | #FFFFFF |
| Dark bg | Body / subtitle / ghost buttons | rgba(255,255,255,0.85) |
| Dark bg | Secondary text / labels / captions | rgba(255,255,255,0.65) |
| Dark bg | Card eyebrow label | #83E85A |
| Dark bg | Accent text | #83E85A (bright green, not #2CC27D) |
| Dark bg | Stat numbers | #FFFFFF (never green) |
| Any bg | Primary CTA button | #83E85A bg, #113333 text |

## Design Principles

- **Contrast first** — text must be clearly readable against its background.
  Never go below rgba(255,255,255,0.85) for body-level text on dark backgrounds.
  rgba(255,255,255,0.65) is the floor for secondary text, labels, and captions
  on dark backgrounds. Never use 0.5 or lower for any readable text.
- **Consistent text tiers** — elements at the same hierarchy level (subtitle,
  ghost button text, pill label) must use the exact same color value. Don't
  let similar-looking text drift to different opacities.
- **Accent text uses #83E85A** (bright green) on dark backgrounds, not #2CC27D.
  #2CC27D is for CTAs, tags, and interactive elements. #83E85A pops more
  against dark teal and reads as a highlight.
- **Dark backgrounds use radial gradients** — never flat solid color. Subtle
  gradient from lighter center to darker edges adds depth.
- **Buttons are rounded rectangles** (8px radius), not pills. Pill shapes
  undercut the enterprise positioning. Only tags/badges use border-radius: 100px.
- **No colored borders on cards** — no green left borders, top borders, or
  accent borders on cards. Cards use only neutral borders (rgba(0,0,0,0.08)
  on light bg, rgba(255,255,255,0.1) on dark bg).
- **No opacity hover on cards or links** — hover effects move an arrow only.
  Never dim/fade the whole card or link text on hover.
- **One green, not two** — don't put #2CC27D and #83E85A next to each other
  (buttons, text, labels). Pick one per context. Buttons always use #83E85A.
  Eyebrow labels always use #83E85A. Accent text in headings on light bg
  uses #2CC27D. Accent text on dark bg uses #83E85A.
- **Stat numbers are never green** — always white on dark, #0D2626 on light.
  Green is reserved for labels, accents, and CTAs — not data.
- **Stat numbers use font-weight 700** — never 800 or 900. Heavier weights
  make Poppins look like a different, condensed typeface. Max weight is 700
  across the entire site (headings, stats, everything).
- **Section backgrounds must alternate** — never two consecutive sections with the
  same background color. Alternate between #FFFFFF and #F5F7F5. Dark gradient
  sections count as a break in the alternation.
- **Two-column sections: visuals take more space** — visual/image side uses
  flex: 1.2, text side uses flex: 1 (~55/45 split). Visuals should feel
  prominent, not squeezed.
- **Flat hierarchy** — no container-within-container nesting. Cards sit directly
  in the section, not wrapped in extra divs. Keep DOM shallow.
- **Don't condense content** — "simplify" means reduce structural complexity
  (fewer layers, flatter DOM), not shorten copy. Never cut content without
  explicit request.
- **Numbered step badges are uniform** — all steps use the same style
  (light green bg rgba(44,194,125,0.1), green #2cc27d text). Don't
  differentiate the last step with a solid badge.
- **Trust signals belong inside their parent section** — cert badges and
  guardrail claims go in a contained card bar within the section, not as a
  separate thin strip. Use a white card with border on light bg.
- **Body text on light bg uses #0D2626** — not #6B7B6B. Use the main text
  color for card descriptions and body copy. #6B7B6B is only for secondary
  text like subtitles under section headings, captions, and meta labels.
  Keep body text consistent across all cards and sections.
- **Cards on off-white (#F5F7F5) sections use white bg + shadow** — white
  cards with border and subtle shadow (0 2px 8px rgba(17,51,51,0.06)) float
  nicely on off-white. Grey-on-grey has too little contrast. Don't match
  card bg to section bg.
- **Body-small is 15px, not 14px** — card descriptions, feature text, and
  any body-level copy in cards uses 15px/400. 14px is too small and
  inconsistent with the rest of the site.
- **Don't split merged sections without asking** — if the original design
  has two content tiers in one section (e.g., promises + cert badges),
  keep them together. Only separate into distinct sections when explicitly
  requested.

## What NOT to do

- Don't add animations or transitions (we'll do those in Framer)
- Don't add hover states via JS (Framer has its own hover system)
- Don't use component libraries or frameworks
- Don't optimize for mobile responsiveness (Framer handles breakpoints)
- Don't add navigation interactivity (dropdowns, mobile menus, etc.)
- Don't use SVG icons inline — use simple placeholder boxes or emoji,
  we'll swap in proper icons in Framer
