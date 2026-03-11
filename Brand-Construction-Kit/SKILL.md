---
name: f1r3fly-brand-system
description: "F1R3FLY brand design system specification for creating on-brand deliverables. Use this skill whenever creating ANY visual deliverable for F1R3FLY — presentations (PPTX), PDFs, documents (DOCX), HTML pages, social media assets, templates, or layouts. Also use when the user asks to apply F1R3FLY branding, references F1R3FLY colors/fonts/logos, or needs to produce anything that should look like it came from F1R3FLY Industries or F1R3FLY.IO. This skill provides exact color values, font specs, logo file paths, layout rules, and gradient definitions so Claude can produce pixel-accurate brand-compliant output every time. Even if the user says 'make me a quick PDF' or 'throw together some slides' for F1R3FLY — use this skill."
---

# F1R3FLY Brand Design System

This is the machine-readable brand specification for F1R3FLY. Read this before producing any F1R3FLY-branded deliverable.

**Two distinct entities exist with separate brand identities:**

| Entity | Role | Logo Icon | Wordmark |
|--------|------|-----------|----------|
| **F1R3FLY Industries** | Parent company | Trefoil knot ("The Mark") | F1R3FLY INDUSTRIES |
| **F1R3FLY.IO** | Developer platform (subsidiary) | Firefly bug icon | F1R3FLY.IO |

Never swap these. The trefoil knot is never used for .IO materials; the firefly bug is never used for Industries materials.

---

## 1. Brand Assets — File Locations

**Source of truth: GitHub repository**

**Repo:** `hannahadamsdesign-spec/f1r3fly-brand-guide`
**GitHub Pages:** `https://hannahadamsdesign-spec.github.io/f1r3fly-brand-guide/`
**Raw file base URL:** `https://raw.githubusercontent.com/hannahadamsdesign-spec/f1r3fly-brand-guide/main/`

```
f1r3fly-brand-guide/
├── F1R3FLY Industries Brand Assets/
│   ├── circle-f1r3fly-industries-logo.svg       # Circle logo (for light backgrounds)
│   ├── circle-f1r3fly-industries-logo.png
│   ├── circle-f1r3fly-industries-logo.pdf
│   ├── f1r3fly-industries-horizontal-logo.svg   # Horizontal lockup (knot + wordmark)
│   ├── f1r3fly-industries-horizontal-logo.png
│   ├── f1r3fly-industries-horizontal-logo.pdf
│   ├── f1r3fly-industries-horizontal-logo-black.svg  # Black version (light bg)
│   ├── f1r3fly-industries-horizontal-logo-black.png
│   ├── f1r3fly-industries-horizontal-logo-black.pdf
│   ├── f1r3fly-industries-vertical-logo.svg     # Vertical lockup (knot + wordmark stacked)
│   ├── f1r3fly-industries-vertical-logo.png
│   ├── f1r3fly-industries-vertical-logo.pdf
│   ├── f1r3fly-industries-vertical-logo-black.svg
│   ├── f1r3fly-industries-vertical-logo-black.png
│   ├── f1r3fly-industries-vertical-logo-black.pdf
│   ├── f1r3fly-knot-icon-alone.svg              # Knot icon only (color, no wordmark)
│   ├── f1r3fly-knot-icon-alone.png
│   ├── f1r3fly-knot-icon-alone.pdf
│   ├── f1r3fly-knot-icon-alone-black.svg        # Knot icon only, black
│   ├── f1r3fly-knot-icon-alone-black.png
│   ├── f1r3fly-knot-icon-alone-black.pdf
│   └── F1R3FLY-INDUSTRY-Brand-Guidebook.pdf     # Brand book PDF
│
└── F1R3FLY.IO Brand Assets/
    └── [firefly bug logo variants]
```

**Which logo to use where:**

| Context | Logo file | Notes |
|---------|-----------|-------|
| Document/page header (dark bg) | `f1r3fly-industries-horizontal-logo.*` | Horizontal lockup is default for headers |
| Document/page header (light bg) | `f1r3fly-industries-horizontal-logo-black.*` | Black variant for white backgrounds |
| Small icon in footer or nav | `f1r3fly-knot-icon-alone.*` | Knot only, no wordmark |
| Light background (DOCX, print) | `circle-f1r3fly-industries-logo.*` | Preferred over black-on-white variants |
| Hero / title slide | `f1r3fly-industries-vertical-logo.*` | Vertical lockup for large placements |

**When fetching assets programmatically:** Download from the GitHub repo using the raw file URL pattern:
`https://raw.githubusercontent.com/hannahadamsdesign-spec/f1r3fly-brand-guide/main/F1R3FLY%20Industries%20Brand%20Assets/{filename}`

For example, to fetch the vertical logo PNG:
`https://raw.githubusercontent.com/hannahadamsdesign-spec/f1r3fly-brand-guide/main/F1R3FLY%20Industries%20Brand%20Assets/f1r3fly-industries-vertical-logo.png`

If the repo is unavailable or the file can't be fetched, ask the user to upload the specific asset needed. **Never draw a placeholder or approximation of the logo** — either use the real file or leave a clearly marked empty frame.

---

## 2. Color System

### Foundation
Background: **#0A0A0A** (near-black) — This is the brand surface, not just a background color. Everything exists in relationship to it.

### Primary Brand Palette (passes WCAG AA on black)

| Name | Hex | RGB | Role |
|------|-----|-----|------|
| **Brand Yellow** | `#F3D630` | 243, 214, 48 | Primary accent, gradient anchor (warm end) |
| **Brand Sage** | `#8BB999` | 139, 185, 153 | Secondary accent, gradient midpoint |
| **Brand Sky** | `#3FA9F5` | 63, 169, 245 | Tertiary accent, gradient anchor (cool end) |

### Primary Brand Gradient
The signature F1R3FLY identifier — a two-stop sweep from **Brand Sky (#3FA9F5) → Brand Yellow (#F3D630)**.
- **Stops:** Sky (left) → Yellow (right). Two stops only. The midpoint naturally blends through a sage-green tone — that's not a third stop, just the color math.
- **Direction:** Left to right (cool to warm) — this matches the gradient bar shown in the brand book
- **Use for:** Section labels, navigation highlights, brand accents, decorative strokes, icon creation for templates
- **Usage note:** Brand accents are used sparingly — a few well-placed gradient touches, not everywhere. Less is more.
- **Never use as:** Background fill
- **Gradient stroke weight:** 0.5px (for thin accent lines and rules)
- **CSS:** `linear-gradient(to right, #3FA9F5, #F3D630)`
- **InDesign/Illustrator:** Linear gradient, 0°, stop 1: #3FA9F5 at 0%, stop 2: #F3D630 at 100%

### Extended Palette

| Name | Hex | Context | Notes |
|------|-----|---------|-------|
| Client Purple | `#5C0269` | Client/enterprise | Fails on black, passes on white |
| Client Scarlet | `#7B0429` | Client/enterprise | Fails on black, passes on white |
| Dev Blue | `#007BC4` | Developer section | Borderline on black (large text only) |
| Dev Teal | `#009188` | Developer section | |
| Partner Green | `#0C8E23` | Partner section | |
| Partner Lime | `#7A9D0E` | Partner section | |
| Neutral Indigo | `#2E31AE` | Neutral/general | No PPTX theme slot available |
| Neutral Gray | `#3F3F3F` | Neutral/general | |
| White | `#FFFFFF` | Text on dark backgrounds | |

### PPTX Theme Color Mapping (12 slots)

```
dk1=#000000  lt1=#FFFFFF
dk2=#5C0269  lt2=#7B0429
accent1=#F3D630  accent2=#8BB999  accent3=#3FA9F5
accent4=#007BC4  accent5=#009188  accent6=#0C8E23
hlink=#7A9D0E   folHlink=#3F3F3F
```

### WCAG Contrast Notes
- Primary palette (Yellow, Sage, Sky): **Pass AA/AAA on black**, fail on white
- Client gradient (Purple, Scarlet): **Fail on black**, pass on white
- Dev Blue: **Borderline on black** — large text only (18pt+ or 14pt bold)
- Always test text legibility; prefer Yellow or White for small text on black

---

## 3. Typography

### Display Typeface: Josefin Sans
- **License:** SIL Open Font License (Google Fonts) — no per-user licensing friction
- **Use for:** Eyebrows, subheaders, section labels, column headers, captions, footer text
- **CDN source:** `https://cdn.jsdelivr.net/fontsource/fonts/josefin-sans@latest/latin-{weight}-normal.ttf`
- **Available weights:** 100 (Thin), 200 (ExtraLight), 300 (Light), 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold)

### Body / Header Typeface: Source Sans Pro (Source Sans 3)
- **Use for:** Page headers (Bold) and body text (Light or Regular)
- **The page header font is variable** — it can be Source Sans 3 or Josefin Sans depending on the deliverable. **Ask the user which font for the header** if not specified.
- **License:** SIL Open Font License (Google Fonts) — free
- **CDN source:** `https://fonts.googleapis.com/css2?family=Source+Sans+3:wght@300;400;600;700&display=swap`
- **Reportlab CDN:** `https://cdn.jsdelivr.net/fontsource/fonts/source-sans-3@latest/latin-{weight}-normal.ttf`

### Legacy Typeface: Brandon Grotesque
- **Status:** Retained ONLY for fixed vector logo wordmarks (outlined, not editable)
- **Do NOT use** in editable templates, web content, or new documents
- **Reason:** HVD Fonts requires per-user desktop licenses + active Adobe CC subscription

### Proportional Type System

**Core rule: No more than 3 text sizes on a page (excluding footer).** 4 is acceptable but 3 is preferred. Different font weights within the same size are fine — it's the size count that matters. This is a fundamental design discipline, not a suggestion.

All sizes are derived proportionally from the page header size:

| Level | Size | Font | Weight | Case | Color |
|-------|------|------|--------|------|-------|
| Page header | BASE | Source Sans 3 (or Josefin Sans — ask) | Bold (700) | ALL-CAPS, letter-spaced (~2.5pt) | White |
| Eyebrow | 30% of header | Josefin Sans | SemiBold (600) | ALL-CAPS | Brand Yellow |
| Section subheader | 60% of header | Josefin Sans | Regular (400) | Sentence case | Brand Yellow or White |
| Column headers | 30% of header | Josefin Sans | Regular (400) | lowercase | Brand Yellow |
| Body copy | 30% of header | Source Sans 3 | Light (300) | Sentence case | White or light gray |
| Footer | Fixed ~7pt | Josefin Sans | Bold (700) | ALL-CAPS | Brand Sage (#8BB999) |

**This means eyebrow, column headers, and body text are all the same size** — they're differentiated by weight, font, and case, not size. That's how you stay at 3 sizes.

**Example at header = 32pt:**
- Header: 32pt
- Subheader: 19.2pt (60%)
- Body/eyebrow/column headers: 9.6pt (30%)
- Footer: 7pt (outside content hierarchy)

### Typography Rules
- **Section subheaders are sentence case** (e.g., "A section subheader"), not all-caps, not lowercase
- All-caps for page headers and eyebrow text only
- Column headers are lowercase (e.g., "section one")
- **Page headers get letter-spacing** — approximately 2.5pt tracking (CSS: `letter-spacing: 0.12em`)
- Prevent widows and orphans (use non-breaking spaces, CSS `text-wrap: balance`)
- Light weights read well on dark backgrounds — don't default to Bold for everything
- When the brand book shows Brandon Grotesque in outlined vector form, that's intentional and should not be changed

### Vertical Spacing Between Elements
The brand's emphasis on breathing room applies to vertical spacing between text elements, not just logo clearspace. Elements should never feel crowded against each other.

- **Below gradient underline → subheader:** At least 1.5× the subheader font size. The subheader needs clear separation from the line.
- **Below subheader → column headers / body content:** At least 2.5× the body font size. This is a section break — it should read as a distinct zone change.
- **Below column headers → body text:** At least 1.5× the body font size.
- **Between body paragraphs:** At least 1× the body font size.

As a general principle: if two elements feel like they're touching, double the gap. The dark background makes tight spacing more noticeable than it would be on white.

### Icon Creation
When asked to create icons for templates or deliverables, use the brand gradient (Sky → Yellow) or individual brand colors. Keep icons simple, geometric, and consistent with the clean, modern F1R3FLY aesthetic. SVG format preferred.

---

## 4. Layout & Grid System

### Grid
- **Columns:** 6
- **Margins:** 8.3% of page width
- **Gutters:** 2% of page width
- **Origin:** Derived from the brand's 60/20/20 logo proportion

### Logo Proportioning
- **Method:** Three trefoil knots placed side by side — the wordmark text width matches that combined width
- **Vertical lockups:** Tend toward square; mark is often larger than in horizontal configurations
- **Horizontal lockup:** Trefoil knot mark + "F1R3FLY INDUSTRIES" in Josefin Sans Bold, proportioned to three-knot width
- **Default for document/page headers:** Use the horizontal lockup (knot + wordmark), not the knot icon alone

### Logo Clearspace
The logo demands generous breathing room. This is a core brand principle — not optional.
- **Minimum clearspace: 40% of the knot icon width on all four sides** (top, bottom, left, right)
- This rule applies identically to every logo version: vertical lockup, horizontal lockup, logomark alone, and icon
- The 40% is measured from the knot icon's width specifically, not the full lockup width
- "Additional space is always better than tightly fitted" — 40% is the floor, not the target
- No text, graphic elements, or page edges may intrude into the clearspace zone
- The page header title should appear below the logo + clearspace, not beside it
- On title slides or cover pages, increase clearspace further — the logo should feel like it owns its space

### Horizontal Lockup Internal Proportions
(From the brand book — these are fixed and do not change at any size)
- Knot icon is vertically centered to the wordmark text, positioned left
- Space between knot icon and wordmark: **30% of the knot icon width**
- Wordmark text height: **40% of the total lockup height**
- Padding above and below text: **30% of the total lockup height**

### Vertical Lockup Internal Proportions
- Knot icon occupies the center **40%** of the total width
- **30% clear space** on each side of the knot
- Space between knot icon and wordmark below: **20% of the knot icon height**

### Standard Page Elements (content pages — from brand book)

Content pages in the brand book do NOT include the logo in the header area. The layout pattern is:

| Element | Spec |
|---------|------|
| Page size | A4 landscape |
| Background | #0A0A0A |
| Page title | Large (~36pt), Josefin Sans Bold, all-caps, letter-spaced (~3.5pt), white, top of page |
| Title underline | Brand gradient stroke, 0.5px, full content width, below title with air |
| Section subheader | Below underline, Josefin Sans SemiBold, all-caps, Brand Yellow, smaller (~12pt) |
| Body content | Below subheader, in columns per grid |
| Footer left | Page number + optional text (variable — ask user) |
| Footer right | "© F1R3FLY INDUSTRIES, 2026. All Rights Reserved \| [Date]" |
| Footer text style | Josefin Sans Bold, small (~7pt), Brand Sage (#8BB999) |

**The title zone should occupy ~15-20% of page height.** The title needs room to breathe — this is the brand's signature spacious feel. Don't crowd content up into the title zone.

### When the logo DOES appear:
- **Cover / title pages:** Logo (vertical lockup) centered, large, with generous clearspace
- **Headers in non-brand-book documents:** If the user requests a logo in the header, use the horizontal lockup with 40% knot-icon-width clearspace, and place the page title below the clearspace zone — never beside or overlapping the logo
- **Footers:** Knot icon alone (small) can appear in footers alongside page numbers
- **Always ask** if the user wants the logo on the page — don't assume

### Presentation Template Elements (PPTX)

| Element | Spec |
|---------|------|
| Slide size | Widescreen 16:9 |
| Background | #0A0A0A |
| Footer | Bug icon (for .IO) or knot icon (for Industries) + copyright + page number |
| Containers | ROUNDED_RECTANGLE shape type |
| Gradient accent | 0.5px stroke, Sky → Yellow |
| No gradient line in footer | Footer is clean, no decorative gradient rule |
| Image format preference | **SVG preferred over PNG.** Use PNG only when SVG isn't available or practical |

---

## 5. Pre-Flight: Before Creating Anything

**Always ask before starting.** Don't assume dimensions, content, or context. Run through the relevant questions below and confirm specs before producing anything.

### Pre-Flight Checklist (ask these)

| Variable | Question | Default if not specified |
|----------|----------|------------------------|
| **Dimensions / size** | What dimensions? (A4, letter, 16:9, custom, social media size, etc.) | Ask — no default |
| **Orientation** | Portrait or landscape? | Landscape for presentations/PDFs, portrait for DOCX |
| **Number of pages** | Single page or multi-page? | Ask if unclear |
| **Column layout** | How many visible content columns? (1, 2, 3 on the 6-col grid) | Ask — depends on content |
| **Background** | Dark (#0A0A0A) or light/white? | Dark for PDF/PPTX, light for DOCX |
| **Logo variant** | When user says "logo" — ask: vertical lockup, horizontal lockup, or knot icon only? | Ask — don't guess |
| **Logo on page?** | Should the logo appear on this page? Where? | Content pages: no. Cover/title pages: yes. Ask if unclear |
| **Header font** | Source Sans 3 or Josefin Sans for the page header? | Ask — either is valid |
| **Eyebrow text** | Is there an eyebrow above the header? What does it say? | Ask if the layout includes one |
| **Footer left content** | What goes in the footer left? (TOC link, page number, page title, nothing, custom) | Ask — "Return to TOC" is brand-book-specific, not universal |
| **Footer right content** | Standard copyright, or custom? | "© F1R3FLY INDUSTRIES, [year]. All Rights Reserved \| [Date]" |
| **Entity** | F1R3FLY Industries or F1R3FLY.IO? | Industries unless stated |
| **File format** | PDF, PPTX, DOCX, HTML, SVG? Who's the audience — can they edit it? | Ask — see distribution format guidance below |
| **Editable?** | Does user need to edit this in a specific app? (Illustrator, InDesign, etc.) Will others need to edit it? | Ask if unclear |

Not every question applies to every deliverable. Use judgment — but when in doubt, ask. It's faster to confirm up front than to rebuild.

### Logo Selection for Light Backgrounds
On white or light backgrounds (DOCX, light-mode web, print on white stock), **do not use the black logo**. Instead, use:
- **`circle-f1r3fly-industries-logo.svg`** — the preferred logo for light-background contexts
- The black trefoil logo should only appear on dark (#0A0A0A) backgrounds where it would be invisible anyway — so in practice, use the color/circle variant for light contexts and the standard color logo on dark.

---

## 6. Deliverable-Specific Instructions

### When creating a PPTX presentation:
1. Read the PPTX creation skill (if available in your environment) for technical approach
2. Apply all specs from this brand system
3. Use ROUNDED_RECTANGLE for all containers
4. Set theme colors per the 12-slot mapping above
5. Footer: icon + copyright + slide number (no gradient line)
6. Embed Josefin Sans or ensure it's available
7. **Use SVG for logos and icons — avoid PNG unless SVG isn't available**

### When creating a PDF:
1. Read the PDF creation skill (if available in your environment) for technical approach
2. Black background (#0A0A0A), white/yellow text
3. Brand gradient for accent lines at 0.5px
4. A4 landscape orientation unless specifically requested otherwise
5. Use horizontal lockup logo with proper clearspace (40% of knot icon width on all sides, minimum)
6. Fetch logo files from the GitHub repo (see Section 1) — never draw approximations
7. Footer left content: ask user what goes there (don't default to "Return to TOC")

### When creating a DOCX:
1. Read the DOCX creation skill (if available in your environment) for technical approach
2. Note: DOCX typically uses a light/white background — **use `circle-f1r3fly-industries-logo.svg`**, not the black logo
3. Use Client Purple or Scarlet for accents on white (they pass contrast on white)
4. Josefin Sans for all text
5. Footer text: small, Josefin Sans Bold, Brand Sage (#8BB999)

### When creating HTML/web content:
1. Load Josefin Sans from Google Fonts: `https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@100;200;300;400;500;600;700&display=swap`
2. CSS custom properties for the color system:
```css
:root {
  --f1r3fly-black: #0A0A0A;
  --f1r3fly-yellow: #F3D630;
  --f1r3fly-sage: #8BB999;
  --f1r3fly-sky: #3FA9F5;
  --f1r3fly-purple: #5C0269;
  --f1r3fly-scarlet: #7B0429;
  --f1r3fly-dev-blue: #007BC4;
  --f1r3fly-dev-teal: #009188;
  --f1r3fly-partner-green: #0C8E23;
  --f1r3fly-partner-lime: #7A9D0E;
  --f1r3fly-indigo: #2E31AE;
  --f1r3fly-gray: #3F3F3F;
  --f1r3fly-gradient: linear-gradient(to right, #3FA9F5, #F3D630);
}
```

---

## 7. Distribution Format Guidance

When creating branded templates or assets that others will edit, format choice depends on the audience:

### SVG as Core Asset Strategy
SVG is the most versatile source format for branded layout elements. A well-built SVG can be placed into DOCX, PPTX, HTML, and opened directly in Illustrator, Inkscape, or any browser. **Consider building reusable brand elements (headers, footers, title blocks, dividers) as SVGs first**, then placing them into container formats.

### Format-to-Audience Matrix

| Audience | Recommended format | Why | Editing tool |
|----------|-------------------|-----|-------------|
| Designers (have Adobe CC) | SVG, AI, PDF | Native vector editing | Illustrator, InDesign |
| General team / non-designers | PPTX or DOCX with SVGs placed | Already on everyone's computer | PowerPoint, Google Slides, Word |
| Developers / technical | SVG, HTML | Code-editable, version-controllable | Any text editor, browser |
| External partners (view only) | PDF | Universal viewer, locked layout | N/A (view-only intent) |
| External partners (editable) | PPTX or DOCX | Lowest friction | PowerPoint, Word, Google Docs |
| Anyone who needs free editing | PDF + recommend LibreOffice Draw | Free, cross-platform PDF editor | libreoffice.org |

### Open-Source Editing Tools (for people without Adobe CC)
When distributing editable templates, include a note recommending:
- **LibreOffice Draw** — free, opens and edits PDFs directly (libreoffice.org)
- **Inkscape** — free, opens SVGs and PDFs as vector files (inkscape.org)
- **Scribus** — free desktop publishing, InDesign alternative (scribus.net)
- **Google Slides / Google Docs** — free, opens PPTX and DOCX natively

### Templates & Assets Roadmap (from brand book p.17 — in development)
- Presentation template (PowerPoint) — in development
- Email signature template — in development
- Social media templates — in development
- Document template (Word/DOCX) — in development
- Brand asset download portal — in development

These will eventually live in a shared portal. This skill should be updated as templates are completed.

---

## 8. Brand Voice in Design

- **"The F1R3FLY palette is built to be the light in dark environments."**
- Black is the foundation — not a background color, the actual brand surface
- Everything exists in relationship to it — to emphasize light as a metaphor for innovation
- The gradient ties cyan, sage green, and warm yellow together — it's the primary F1R3FLY identifier
- Don't crowd it. Let elements breathe against the black.
- Positioning is "evidence-first, not token-first" — enterprise accountability, AI verification, data sovereignty. Never crypto hype.

---

## 9. Version Control

| Field | Value |
|-------|-------|
| Skill version | 1.6 |
| Last updated | March 10, 2026 |
| Brand book source | F1R3FLY-INDUSTRY-Brand-Guidebook.pdf (1.7 MB, created March 8, 2026) |
| Brand book location | GitHub: `hannahadamsdesign-spec/f1r3fly-brand-guide` → `F1R3FLY Industries Brand Assets/` |

**When the brand has been updated:** Check the GitHub repo for the latest brand book PDF, or ask the user for updated specs. Compare against this document and update the changed values. The structure stays the same — only values change.
