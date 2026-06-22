---
name: f1r3fly-brand-kit
description: "Self-contained F1R3FLY brand system for producing on-brand deliverables — social media graphics, PDFs, presentations, documents, HTML pages, templates, and layouts. Use this whenever creating ANYTHING branded for F1R3FLY Industries or F1R3FLY.IO, or when the user references F1R3FLY colors, fonts, or logos. Contains the exact color values (June 12 2026 system), typography rules, logo fetch URLs, layout specs, and brand voice so any AI can produce brand-accurate output on the first try. Triggers on requests like 'make a F1R3FLY social post', 'F1R3FLY PDF / slide deck / one-pager', 'apply F1R3FLY branding', 'use the F1R3FLY brand rules', or 'make this look like F1R3FLY'."
version: "1.1"
updated: "2026-06-20"
---

# F1R3FLY Brand Kit

This is the authoritative, machine-readable brand specification for F1R3FLY. Read it fully before producing any branded deliverable. It overrides your own defaults and any older F1R3FLY material you may have seen.

If you are an AI reading this on someone's machine: this file IS the brand. Follow it exactly. When you can't, say so out loud instead of improvising.

---

## 0. How to use this skill (read first)

You are about to make something for F1R3FLY. Before you produce anything, confirm these with the user in one short message. Do not guess.

1. **Content** — What words go in it? Headline, body, call to action, any data. If they didn't say, ask. Offer to draft the copy in F1R3FLY's voice (Section 8) if they want.
2. **Format and size** — What is it, and what dimensions? For social, name the exact platforms and pixel sizes. If they just say "social media," propose a standard set (below) and confirm before building.
3. **Entity** — F1R3FLY Industries or F1R3FLY.IO? They use different logos and you must not mix them. Default to Industries if unstated, but confirm.

**Standard social sizes to offer** (px): Instagram square post 1080×1080, Instagram/Facebook story 1080×1920, Instagram portrait 1080×1350, LinkedIn post 1200×627, X/Twitter post 1600×900, Facebook post 1200×630, YouTube thumbnail 1280×720.

**Flag accessibility up front.** Tell the user that every color combination must meet WCAG AA contrast against its background, and share the contrast checker (in Links and resources) so they can verify a pairing before publishing. When in doubt, check it.

### Hard rules — never violate

- **Background is true black `#000000`.** Build on black unless the user explicitly asks for light/white.
- **Only the primary palette leads** (Black, White, Brand Yellow, Brand Sky). The secondary colors are audience/topic coding only — never the dominant color of a layout.
- **Never redraw, recolor, retype, or approximate a logo.** Fetch the real file from the URLs in Links and resources / Section 5. If you can't fetch it, leave a clearly labeled empty frame and tell the user. Never substitute a lookalike or a font-typed wordmark.
- **The icon alone is not the logo.** The bug (.IO) or knot (Industries) on its own may only be used as a profile badge/avatar/favicon, or as a supporting element inside a piece where the full logo already appears. Never as the standalone mark on a cover or a public-facing piece. Full rule in Section 5.
- **Typography:** Josefin Sans for headings/UI, Source Sans 3 for body. Never typeset Brandon Grotesque — it exists only inside the fixed, outlined logo files.
- **Keep it spacious.** Gradient accents are used sparingly — a few well-placed touches, never everywhere. Let elements breathe against the black.
- **Positioning is evidence-first, not token-first.** Never frame F1R3FLY as crypto/blockchain hype.
- **If you cannot comply** with any rule (missing font, can't reach a logo, user asked for an off-brand color), say so plainly and offer the on-brand alternative. Do not silently improvise.

---

## 1. Brand at a glance

| Element | Value |
|---------|-------|
| Surface | True black `#000000` |
| Primary colors | White `#FFFFFF`, Brand Yellow `#F3D630`, Brand Sky `#3FA9F5` |
| Signature gradient | Yellow `#F3D630` → Sky `#3FA9F5` (left to right) |
| Headings / display / UI | Josefin Sans |
| Body text | Source Sans 3 |
| Logo wordmark font | Brandon Grotesque — **outlined in logo files only, never typed** |
| Industries logo | Trefoil knot ("The Mark") |
| F1R3FLY.IO logo | Firefly bug icon |
| Grid | 6 columns, 8.3% margins, 2% gutters |
| Voice | Evidence-first, plain, measured. Light in dark environments. |

---

## Links and resources

Everything an AI or a teammate needs to pull real assets and check their work.

**Brand portal (browse all assets)**
- Portal repo: https://github.com/hannahadamsdesign-spec/f1r3fly-brand-portal
- Portal site: https://hannahadamsdesign-spec.github.io/f1r3fly-brand-portal/

**Logos**
- F1R3FLY Industries logos (knot): https://github.com/hannahadamsdesign-spec/f1r3fly-brand-portal/tree/main/F1R3FLY-Industries-Brand-Assets
- F1R3FLY.IO logos (bug): https://github.com/hannahadamsdesign-spec/f1r3fly-brand-portal/tree/main/F1R3FLY-IO-Brand-Assets
- Raw fetch base (for AI / programmatic download): `https://raw.githubusercontent.com/hannahadamsdesign-spec/f1r3fly-brand-portal/main/`

**Layout grid** (kept at a stable path — updated by saving over the same file)
- Browse: https://github.com/hannahadamsdesign-spec/f1r3fly-brand-portal/tree/main/templates
- Direct: `https://raw.githubusercontent.com/hannahadamsdesign-spec/f1r3fly-brand-portal/main/templates/brand-layout-grid.svg`

**Brand books** (deeper reference — see the caveat in Section 9; both are being revised next)
- F1R3FLY Industries — Brand Style Guide (PDF): https://github.com/hannahadamsdesign-spec/f1r3fly-brand-portal/blob/main/F1R3FLY%20INDUSTRIES-Brand%20Style%20Guide.pdf
- F1R3FLY.IO — Brand Guidebook (PDF): https://github.com/hannahadamsdesign-spec/f1r3fly-brand-portal/blob/main/F1R3FLY.IO-Brand%20Guidebook.pdf

**Check your work**
- Contrast checker (WCAG AA/AAA): https://webaim.org/resources/contrastchecker/
- Editorial style — The Chicago Manual of Style: https://www.chicagomanualofstyle.org/home.html

---

## 2. Two entities — never mix them

| Entity | Role | Logo icon | Wordmark |
|--------|------|-----------|----------|
| **F1R3FLY Industries** | Parent / master brand | Trefoil knot | F1R3FLY INDUSTRIES |
| **F1R3FLY.IO** | Developer platform (sub-brand) | Firefly bug | F1R3FLY.IO |

The trefoil knot is never used on .IO materials; the firefly bug is never used on Industries materials. All sub-brands (F1R3FLY.IO, F1R3FLY Limited, Sports, Medical, Arts/Entertainment) inherit the same colors, typography, dark surface, and layout — they may add a sector accent color, but the foundation does not change.

---

## 3. Color system (June 12, 2026)

This is the current color system. It supersedes anything older. **Brand Sage `#8BB999` was retired June 10, 2026 — do not use it.** If you see sage in an older file or brand book, treat it as out of date.

### Primary — leads every F1R3FLY representation

| Name | Hex | RGB | Notes |
|------|-----|-----|-------|
| Black | `#000000` | 0, 0, 0 | The surface. Build on this. |
| White | `#FFFFFF` | 255, 255, 255 | Primary text on black. |
| Brand Yellow | `#F3D630` | 243, 214, 48 | Warm gradient anchor, primary accent. |
| Brand Sky | `#3FA9F5` | 63, 169, 245 | Cool gradient anchor, primary accent. |

### Signature brand gradient

Yellow → Sky, two stops only. The midpoint blends through a green tone naturally — that is color math, not a third stop. Used for: section labels, nav highlights, accent strokes, dividers, icon fills. Never as a background fill. Use sparingly.

- **CSS:** `linear-gradient(to right, #F3D630, #3FA9F5)`
- **Stroke weight for accent rules:** 0.5px
- **Vector apps:** linear, 0°, stop 1 `#F3D630` at 0%, stop 2 `#3FA9F5` at 100%

### Secondary — audience / topic color coding only, never the lead

Use these to signal which audience a piece is for. They never become the dominant color of a layout, and small body text should not be set in them on black.

| Audience | Colors | Pair gradient |
|----------|--------|---------------|
| **Client** | Purple `#5C0269`, Scarlet `#7B0429` | `#5C0269` → `#7B0429` |
| **Developer** | Blue `#007BC4`, Teal `#009188` | `#007BC4` → `#009188` |
| **Partner** | Green `#0C8E23`, Lime `#7A9D0E` | `#0C8E23` → `#7A9D0E` |
| **Neutral** | Indigo `#1114AD`, Gray `#3F3F3F` | `#1114AD` → `#3F3F3F` |

### Accessibility — non-negotiable

Design to WCAG AA minimum. Verify any color-on-color pairing with the contrast checker before publishing: https://webaim.org/resources/contrastchecker/

- **Safe for small text on black:** White, Brand Yellow, Brand Sky.
- **Audience colors on black:** Dev Teal, Partner Green, Partner Lime, Dev Blue work for large text only (18pt+ or 14pt bold). Client Purple, Client Scarlet, Neutral Indigo, Neutral Gray fail on black — use them on light backgrounds, or as fills behind white text, not as text on black.
- **Muted/secondary text on black:** use a light neutral gray such as `#C5C5C5` (≈12:1 on black, passes AAA) or `#959595` (passes AA). Prefer the lighter value for small text like footers and captions. Never use a dark gray for text on black.
- When in doubt for small text on black, use White or Brand Yellow.

### Hue-variant rule

Any brand color may be lightened, darkened, or shifted in saturation — **the hue stays constant.** Hue anchors: Yellow 51°, Sky 205°; every secondary color locks to its own hue. The full tint/shade ladders are in the Appendix.

---

## 4. Typography — what to use and when

Two free fonts do all the editable work. The third exists only inside logo files.

### Josefin Sans — headings, display, UI

Google Fonts, SIL Open Font License (free, no licensing friction).
Web: `https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@100;200;300;400;500;600;700&display=swap`

| Weight | Use for |
|--------|---------|
| Bold (700) | Eyebrows; primary section headers and dividers |
| SemiBold (600) | Page headers, subheaders, card titles |
| Regular (400) | Secondary UI text, captions, column headers |
| Light (300) | Large display text, hero headlines |

### Source Sans 3 — body

Google Fonts (formerly Source Sans Pro), SIL OFL (free). Light/Regular for body copy, Bold for body headers.
Web: `https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@300;400;600;700&display=swap`

The **page-header font is variable** — it can be Josefin Sans or Source Sans 3 depending on the piece. Ask the user which they want for headers if it isn't specified.

### Brandon Grotesque — logos only

Retained ONLY for the fixed, outlined wordmarks inside logo files. **Never typeset it** in templates, web content, or new documents — it is licensed (HVD Fonts, per-user desktop license + Adobe CC) and is not in the brand repo. If you need the wordmark, use the logo file; do not set the text yourself.

### Type rules

- **Maximum 3 text sizes per page** (4 acceptable, 3 preferred). Differentiate by weight, font, and case — not by adding more sizes. Eyebrow, column headers, and body are typically the *same size*, separated by weight/case.
- **Page headers and eyebrows:** ALL-CAPS with letter-spacing (~2.5pt tracking; CSS `letter-spacing: 0.12em`).
- **Section subheaders:** sentence case. **Column headers:** lowercase.
- Light weights read well on black — don't default everything to Bold.
- Prevent widows and orphans (non-breaking spaces, CSS `text-wrap: balance`).
- Editorial style for any prose: The Chicago Manual of Style (https://www.chicagomanualofstyle.org/home.html).

---

## 5. Logos

**Source of truth: the GitHub brand portal** (links in Links and resources). Fetch the real files — never approximate.

```
f1r3fly-brand-portal/
├── F1R3FLY-Industries-Brand-Assets/   # trefoil knot (parent)
│   # f1r3fly-industries-{lockup}-{variant}.{svg|png|pdf}
│   # lockups: horizontal-logo, vertical-logo, circle-logo, circle-icon, knot-icon
│   # variants: color-on-dark, color-on-light, bw-on-light, white
├── F1R3FLY-IO-Brand-Assets/           # firefly bug (developer platform)
│   # f1r3fly-io-{lockup}-{variant}.{svg|png|pdf}
│   # lockups: horizontal-logo, vertical-logo, bug-icon, circle-icon
│   # variants: color-on-dark, white, white-background, BW-white-background
├── f1r3fly-brand-fonts/               # Josefin Sans ×5, Source Sans 3 ×3 (free)
├── templates/                         # layout grid + social templates
├── F1R3FLY INDUSTRIES-Brand Style Guide.pdf
└── F1R3FLY.IO-Brand Guidebook.pdf
```

**Example fetch** (Industries vertical logo, for a dark title slide):
`https://raw.githubusercontent.com/hannahadamsdesign-spec/f1r3fly-brand-portal/main/F1R3FLY-Industries-Brand-Assets/f1r3fly-industries-vertical-logo-color-on-dark.png`

### How to access files — formats and variants

**Pick the file format for the job:**

| Format | Use it for | Notes |
|--------|-----------|-------|
| **SVG** | Web, print, anything you'll scale or place in another file | Vector, infinitely scalable. The default — prefer it whenever the tool supports it. |
| **PNG** | Tools that don't take SVG (some social schedulers, raster-only apps) | Transparent background; comes in color-on-dark and white variants. |
| **PDF** | Print, view-only sharing | Vector, locked layout. |

**Pick the variant for the background:**

| Variant | When |
|---------|------|
| `color-on-dark` | On the black surface — the default for most F1R3FLY work |
| `color-on-light` | On white/light backgrounds |
| `bw-on-light` | One-color / print-economy on light |
| `white` | Reversed, for placing on a photo or solid dark color |

**To get a file:** humans browse the folder links in Links and resources and download; an AI fetches the raw URL directly (`raw fetch base` + folder + filename). If a needed variant or format isn't in the folder, ask — don't recreate it.

### When the icon may be used alone (bug or knot)

The icon by itself is **not** the logo. The full logo is the icon **plus** the wordmark (the bug or knot together with "F1R3FLY.IO" or "F1R3FLY INDUSTRIES"). The icon alone is allowed only in these cases:

- **As an identity badge** — Discord/LinkedIn/social profile avatars, app icons, favicons. These are inherently small, recognized-in-place marks.
- **As a supporting element inside a piece where the full logo already appears prominently.** Example: a slide deck whose cover/first slide carries the full F1R3FLY.IO logo may use the bug as an SVG accent element on a later slide. That's fine, because the brand is already established front and center in that piece.

The icon alone is **not** allowed:

- On a **cover or title** by itself.
- As the **standalone mark on a public-facing piece** where the full logo doesn't appear — e.g., a social media post carrying only the bug.
- **Crowded against unrelated elements** — give it the same clearspace the full logo gets; never let it sit tight to other graphics or text it isn't part of.

When unsure, use the full logo. The icon-alone exceptions are for badges and for in-context accents, nothing more.

### Logo rules (from the brand books)

- **Generous clearspace** is a core principle. The keep-out lines in the brand book are the *minimum*; more space is always better. Nothing — text, graphics, page edges — intrudes. On covers, give it even more room.
- SVG preferred over PNG wherever practical.
- Don't recolor, distort, rotate, add effects, or place on busy/low-contrast backgrounds. Don't separate the logomark from its wordmark within a lockup.
- The horizontal lockup (knot + wordmark) is the default for headers — not the icon alone.

### Which logo where

| Context | Logo |
|---------|------|
| Document/page header, dark bg | `…-horizontal-logo-color-on-dark` |
| Document/page header, light bg | `…-horizontal-logo-color-on-light` (or `-bw-on-light`) |
| Hero / title / cover | `…-vertical-logo-color-on-dark` |
| Small footer / nav icon | knot icon (Industries) or bug icon (.IO) |
| Light background (DOCX, print on white) | use the color/circle variant — **never the black logo on white** |

---

## 6. Layout, grid, and footer

Use the layout grid file in the portal `templates/` folder (see Links and resources) as the working grid. It is kept at a stable path and updated by saving over the same file.

### Grid

- **6 columns.** Margins **8.3%** of page width each side. Gutters **2%** of width.
- Common content splits on the 6-col grid: full 6, or 4+2, 3+3, 2+2+2.

### Page anatomy (PDF / print, A4 landscape unless told otherwise)

| Element | Spec |
|---------|------|
| Background | `#000000` |
| Page title | Large (~36pt), Josefin Bold, ALL-CAPS, letter-spaced, white, top of page |
| Title underline | Brand gradient stroke, 0.5px, full content width, with air below the title |
| Subheader | Josefin SemiBold, ALL-CAPS, Brand Yellow, smaller (~12pt) |
| Body | Below subheader, in columns per the grid |
| Title zone | Should occupy ~15–20% of page height — let it breathe |
| Footer right | `© F1R3FLY INDUSTRIES, [year]. All Rights Reserved \| [Date]` |
| Footer style | Josefin Bold, small (~7pt), light neutral gray `#C5C5C5` |

> Footer/caption color is a light neutral gray (`#C5C5C5`) for legibility on black. The brand books specify sage here, but **sage is retired** — do not use `#8BB999`.

### Vertical spacing (the brand's spacious feel)

- Gradient underline → subheader: ≥ 1.5× the subheader size.
- Subheader → body/columns: ≥ 2.5× the body size (this is a section break).
- Column header → body: ≥ 1.5× the body size.
- Between body paragraphs: ≥ 1× the body size.
- General rule: if two elements feel like they're touching, double the gap. Tight spacing shows more on black.

### Presentations (PPTX)

16:9, `#000000` background, ROUNDED_RECTANGLE containers, gradient accents at 0.5px (Yellow → Sky), footer = entity icon + copyright + slide number (no gradient line in the footer). SVG over PNG.

---

## 7. Icons

When making icons for a deliverable: use the brand gradient (Yellow → Sky) or single brand colors. Keep them simple, geometric, and consistent with the clean modern aesthetic. SVG preferred.

---

## 8. Brand voice

**Positioning:** evidence-first, not token-first. F1R3FLY is about verifiable, accountable AI and data workflows — enterprise accountability, AI verification, data sovereignty. Never crypto/token hype.

**Design philosophy:** "The F1R3FLY palette is the light in dark environments." Black is the surface, not a background. Everything exists in relationship to it — light as a metaphor for innovation. The gradient is the primary identifier; use it sparingly. Don't crowd anything.

**Copy voice (client/stakeholder/marketing):** plain, honest, measured, evidence-first. Say the true thing simply. Avoid staccato fragments, tricolons, slogan-headlines, and metaphor flourishes in stakeholder-facing work. Confidence comes from clarity, not cleverness.

**Editorial style:** follow The Chicago Manual of Style (https://www.chicagomanualofstyle.org/home.html) for grammar, punctuation, capitalization, and citations.

---

## 9. Deeper reference — the two brand books

For anything not covered here (detailed logo geometry, clearspace diagrams, brand architecture, philosophy), see the published brand books (links in Links and resources):

- **F1R3FLY INDUSTRIES — Brand Style Guide** (March 27, 2026) — trefoil-knot master brand.
- **F1R3FLY.IO — Brand Guidebook** (April 6, 2026) — firefly-bug developer platform.

> **Two caveats.** (1) Both books predate the June 12, 2026 color system. They still show the old Yellow → Sage → Sky gradient and list Brand Sage `#8BB999` as a core color. **For color, this skill is authoritative — ignore sage and the three-stop gradient in the books.** (2) The books are being revised. Use them for logo geometry, grid, clearspace, brand architecture, and voice; for color, typography, and the icon-alone rule, this skill is the current word.

---

## Appendix — Hue-variant ladders

Rule: lighten, darken, or shift saturation, but keep the hue constant. Each row is darkest → original → lightest. "ORIGINAL" marks the named brand color.

**Brand Yellow** (hue 51°)
`#1A1600` · `#403600` · `#A68D00` · `#F2CE00` · **`#F3D630` (ORIGINAL)** · `#FFEC80` · `#FFF5BF`

**Blue family** (hue 205° — Brand Sky and Dev Blue share this hue)
`#001626` · `#003459` · `#00528C` · **`#007BC4` (Dev Blue)** · **`#3FA9F5` (Brand Sky)** · `#7AC2F5` · `#93CCF5`

**Client Purple**
`#220027` · `#33003A` · `#470051` · **`#5C0269` (ORIGINAL)** · `#A14FAC` · `#CA94D2` · `#E9D1ED`

**Client Scarlet**
`#2B000D` · `#430015` · `#5E001D` · **`#7B0429` (ORIGINAL)** · `#B65574` · `#D799AC` · `#EFD3DC`

**Dev Teal**
`#00302D` · `#004C48` · `#006E67` · **`#009188` (ORIGINAL)** · `#58C3BC` · `#9BDEDA` · `#D5F2F0`

**Partner Green**
`#002F08` · `#004B0D` · `#006C13` · **`#0C8E23` (ORIGINAL)** · `#60C171` · `#A0DDAB` · `#D7F1DC`

**Partner Lime**
`#263200` · `#3E5200` · `#5A7700` · **`#7A9D0E` (ORIGINAL)** · `#B0C964` · `#D3E2A4` · `#EDF3D9`

**Neutral Indigo**
`#000136` · `#000259` · `#000382` · **`#1114AD` (ORIGINAL)** · `#6A6CD2` · `#A8A9E6` · `#DBDBF5`

**Neutral Gray**
`#1E1E1E` · `#282828` · `#333333` · **`#3F3F3F` (ORIGINAL)** · `#959595` · `#C5C5C5` · `#E8E8E8`

---

## Provenance

| Field | Value |
|-------|-------|
| Kit version | 1.1 (June 20, 2026) |
| Color authority | f1r3fly-brand-color-system-06.12.2026 (sage retired June 10; black = #000000) |
| Type / logo / layout source | F1R3FLY brand books (Mar–Apr 2026, being revised) + F1R3FLY brand system; color values overridden by the June 12 system |
| Maintainer | Hannah Adams, Creative Director, F1R3FLY |

When the brand changes, update the values here — the structure stays the same. The brand books and layout grid are slated for revision; keep their portal paths/filenames stable so these links don't break.
