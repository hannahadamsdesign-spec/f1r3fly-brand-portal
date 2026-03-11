# F1R3FLY Brand Construction Kit

This folder contains everything an AI assistant (Claude) or a human designer needs to produce on-brand F1R3FLY deliverables from scratch.

## What's in this folder

| File | What it is | How to use it |
|------|-----------|---------------|
| **SKILL.md** | Complete brand specification | Read this first. It has every color, font, spacing rule, and logo path. |
| **f1r3fly-brand-grid.svg** | Proportional construction grid | Place as bottom layer in any layout. Stretches to any aspect ratio. Delete before export. |
| **f1r3fly-brand-values.json** | Machine-readable brand values | Import into build scripts (Node.js, Python). All colors, fonts, spacing as structured data. |
| **f1r3fly-gradient-line.png** | Pre-rendered brand gradient accent | Drop into any deliverable as the gradient underline/accent. 2000×6px, Sky→Yellow. |

---

## For AI assistants (Claude)

### Before creating any F1R3FLY deliverable:
1. Read **SKILL.md** — it has the full spec, pre-flight checklist, and deliverable-specific instructions
2. Load **f1r3fly-brand-values.json** — import the values directly instead of hardcoding hex values
3. Use **f1r3fly-brand-grid.svg** as the construction layer (see below)
4. Use **f1r3fly-gradient-line.png** for accent lines — don't regenerate it each time

### Using the construction grid

The grid SVG uses a `viewBox="0 0 1000 1000"` with `preserveAspectRatio="none"`, which means it stretches to fit any container dimensions while maintaining the proportional column/margin/gutter relationships. All values are percentages, not fixed measurements.

**Grid structure:**
- 6 columns, 8.3% margins on all sides, 2% gutters between columns
- Derived from the brand's 60/20/20 logo proportion

**Vertical zones (horizontal guide lines):**
- **Title zone** — top 20% of the page. Page title lives here.
- **Gradient line** — at ~22%. The brand accent line sits just below the title.
- **Eyebrow / subheader** — at ~27%. Yellow ALL-CAPS label.
- **Content start** — at ~31%. Body text and columns begin here.
- **Footer** — at 93%. Copyright, page number, knot icon.

**Visual language:**
- Cyan dashed lines = column/margin boundaries
- Pink dashed lines = vertical zone boundaries
- Faint orange fills = gutters (so you can see where NOT to place content)
- Labels are outside the content area and will be cropped in most layouts

**In code (pptxgenjs, ReportLab, etc.):**
The grid doesn't get placed as an image layer — use the percentages directly:
```
Left margin:    8.3% of width
Right margin:   91.7% of width
Column width:   (83.4% - 5 gutters × 2%) / 6 = ~12.23% of width
Gutter:         2% of width
Title zone:     8.3% to 20% of height
Content start:  ~31% of height
Footer:         93% of height
```

**In Illustrator / InDesign / PowerPoint:**
Place the SVG as the bottom layer, stretch to page dimensions, lock the layer, build on top. Delete the grid layer before exporting the final deliverable.

---

## For human designers

### The grid SVG
Open `f1r3fly-brand-grid.svg` in Illustrator or place it in InDesign. Scale it to match your artboard — the proportions hold at any size. Use it as a visual guide while building layouts, then delete or hide the layer before export.

### The gradient line
`f1r3fly-gradient-line.png` is a pre-rendered 2000×6px brand gradient (Sky blue → Yellow, left to right). Place it as a thin accent line below page titles. In InDesign, you can also recreate this as a native gradient swatch using the stops defined in SKILL.md.

### Brand values
`f1r3fly-brand-values.json` is useful if you're building web templates or automated workflows. Every hex value, font name, and spacing rule is in there as structured data.

---

## Grid math reference

All values are proportional (percentages of total width or height):

```
Page width = 100%

Left margin:     8.3%
Right margin:    8.3%
Content zone:    83.4% (what's left)
Gutters (×5):    2.0% each = 10.0% total
Columns (×6):    12.23% each = 73.4% total
                 73.4% + 10.0% = 83.4% ✓

Page height = 100%

Top margin:      8.3%
Title zone:      8.3% → 20%   (page title, large text)
Gradient line:   ~22%          (brand accent underline)
Eyebrow:         ~25-27%       (section label, yellow caps)
Content start:   ~31%          (body text begins)
Content zone:    31% → 93%     (main content area)
Footer:          93% → 100%    (copyright, page number, knot icon)
```

### Applying to specific formats

| Format | Width | Height | Margin | Column width |
|--------|-------|--------|--------|-------------|
| A4 landscape | 297mm | 210mm | 24.6mm | 36.3mm |
| A4 portrait | 210mm | 297mm | 17.4mm | 25.7mm |
| 16:9 slide (10") | 10" | 5.625" | 0.83" | 1.22" |
| Social square | 1080px | 1080px | 89.6px | 132.1px |
| Social story | 1080px | 1920px | 89.6px | 132.1px |
| OG/banner | 1200px | 628px | 99.6px | 146.8px |
| US Letter landscape | 11" | 8.5" | 0.913" | 1.35" |

---

## Two entities — never mix them

| | F1R3FLY Industries | F1R3FLY.IO |
|---|---|---|
| **Logo icon** | Trefoil knot ("The Mark") | Firefly bug |
| **Wordmark** | F1R3FLY INDUSTRIES | F1R3FLY.IO |
| **Role** | Parent company | Developer platform (subsidiary) |

Confirm which entity you're designing for before starting. The logos, brand books, and asset folders are separate.

---

## File version

| Field | Value |
|-------|-------|
| Kit version | 1.0 |
| Created | March 10, 2026 |
| SKILL.md version | 1.6 |
| Grid math verified | ✓ |
