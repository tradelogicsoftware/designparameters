# Spray Foam Calculator — Design System

TradeLogic Report Design System, adapted for a single-page utility app (formerly "Foam Calc," now "Spray Foam Calculator"). Body-page variant: white page background with navy bands/cards as structural accent blocks, one unified accent blue for all interactive and label elements, Helvetica throughout.

## Brand Colors

| Token | Hex | Use |
|---|---|---|
| Accent Blue | `#3F7ED1` | Single brand blue — labels, values, links, borders, toggles, buttons, logo mark. Used everywhere blue appears in the UI, including the TradeLogic logo (recolored from the source cyan to match). |
| Report Navy (heading) | `#0C213F` | Headings (`h1`, card titles), category divider bands, total-panel accents |
| Card Navy | `#182A48` | Total panel (stat-card) background |
| Body Text | `#26313D` | Paragraph/body copy, input values |
| Muted Gray | `#7C8898` | Secondary/caption text, footer text |
| Dimmed Gray | `#9AA5B2` | Toggle thumb (off state), disclosure arrow, copyright line |
| Rule Gray | `#CED2D8` | Card borders, dividers |
| White | `#FFFFFF` | Page background, card background |
| On-Navy Text | `#EDF1F7` | Text placed on navy-band/card-navy surfaces (group-label titles, total figures) |
| Sets Highlight | `#EAF2FC` | Light-blue tint for the "Sets" output cell and add-row button hover |
| Danger | `#C0392B` | Reset button hover state only |

**Note on blue:** earlier drafts of this app carried three separate blues (accent `#3F7ED1`, a darker `#2A62AA` for emphasis figures, and brand cyan `#00AFEA` for the logo). These have been consolidated — every blue element in the app, including the logo mark, now resolves to the same `#3F7ED1`. The logo was hue-shifted from its source cyan to this blue while preserving its original lightness/shading, so the icon still reads with depth but matches the UI's single accent color exactly.

## Typography

- Typeface: Helvetica Neue / Helvetica / Arial (system fallback), sans-serif throughout — no serif, no monospace (numeric fields use tabular-nums on the same Helvetica stack rather than a separate mono font).
- App title (`h1`): Bold, 1.25rem, Report Navy.
- Eyebrow subtitle (under title): Bold, 0.68rem, uppercase, letter-spaced 0.1em, Accent Blue.
- Category divider number ("01", "02", "03"): Bold, 0.78rem, Accent Blue.
- Category divider title: Bold, 0.7rem, uppercase, letter-spaced 0.12em, On-Navy white.
- Card title (section name): Bold, 0.9rem, Report Navy.
- Card subtitle (caption): Regular, 0.7rem, Muted Gray.
- Field/output labels: Bold, 0.58–0.68rem, uppercase, letter-spaced 0.08em, Accent Blue.
- Input/output values: Bold, 0.9–1.6rem, tabular-nums, Body Text (or On-Navy white on dark surfaces).
- Footer text: Regular, 0.62rem, uppercase, letter-spaced 0.06em, Muted Gray.
- Copyright line: Regular, 0.62rem, letter-spaced 0.02em, centered, Dimmed Gray.

## Layout Patterns

**Header**
- Sticky, white background, thin Rule Gray bottom border.
- 4px vertical Accent Blue bar to the left of the logo/title block (cover-page accent-bar convention).
- Logo mark (40px tall) + title block: app name (navy, bold) with an uppercase accent-blue eyebrow beneath it.

**Stat banner (Price per Set / Coverage Rate)**
- White card, Rule Gray border, 10px radius.
- Bold uppercase Accent Blue label above a bordered input row.
- Focus state: Accent Blue border + soft blue glow (`#3F7ED133`).
- Two of these stack directly beneath the header: Price per Set ($) and Coverage Rate (Bd Ft per Set) — the latter is the divisor for the sets calculation (see Math below).

**Category divider band**
- Full-width Report Navy band, thin Rule Gray top/bottom border.
- Bold Accent Blue section number ("01", "02", "03") + bold uppercase white title, e.g. "01 WALLS."
- One band per input group: Walls, Slopes/Ceilings, Rim Joists.

**Section card**
- White card, Rule Gray border (10px radius); border turns Accent Blue when the card is active/expanded.
- Header row: title (navy) + subtitle (muted gray) on the left, a toggle switch on the right. Toggling expands/collapses the card body and includes/excludes it from the totals.
- Body: two-column input grid (Linear Ft, Height, R-Value spanning both columns), a divider, then a three-cell output row (Sq Ft, Board Ft, Sets). The Sets cell gets a light-blue highlight (`#EAF2FC` background, Accent Blue border) to differentiate the key output.

**Add-row button**
- One per group, placed after the last card in that group.
- Dashed Accent Blue border, uppercase Accent Blue label ("+ Add Wall Section," etc.), light-blue hover fill.
- Appends a new section card (same input/output layout, default active) into that group and folds it into totals/breakdown immediately. Reset All removes any added rows and restores the base set.

**Total panel (stat-card)**
- Card Navy background, Accent Blue border, 4px Accent Blue vertical bar on the left edge (same accent-bar convention as the header).
- Two large On-Navy white figures: Total Sets and Material Cost, each with a small uppercase Muted Gray label.
- Collapsible breakdown list beneath a translucent divider, toggled by a dotted-underline text link.

**Footer**
- Thin Rule Gray top rule, small uppercase Muted Gray text: app name/company on the left, version on the right.
- Centered copyright line beneath it.

## Component Conventions

- **Toggle switches**: 44×26px pill. Off = light gray track/dimmed-gray thumb. On = Accent Blue track/white thumb. Used to include/exclude a section from the calculation.
- **Buttons**: Reset All (outlined, muted gray, turns red on hover) sits below the total panel; Add-row buttons (dashed, accent blue) sit at the end of each group.
- **Radius**: 10px for cards/panels/buttons, 6px for inputs/output cells — consistent two-tier rounding.
- **Borders over fills**: cards are white and rely on Rule Gray borders for separation, keeping the page light; navy is reserved for bands/panels that need to stand out (dividers, totals).

## Math (for reference — not a visual convention, but part of the app's defined behavior)

- `Sq Ft = Linear Ft × Height`
- `Board Ft = (R-Value ÷ 7) × Sq Ft` (R-7 per inch of spray foam thickness)
- `Sets = ceil(Board Ft ÷ Coverage Rate)` — Coverage Rate is the user-entered board-feet-per-set banner value; sets show "—" until a coverage rate is entered.
- Totals sum Sets across all active/expanded section cards, including any added via "+"; Material Cost = Total Sets × Price per Set.

## Reuse Checklist

1. Single accent blue (`#3F7ED1`) for every interactive/label/link/logo element — do not reintroduce a second blue.
2. Navy (`#0C213F` / `#182A48`) reserved for headings, divider bands, and the total stat-card — not for general page background.
3. Helvetica throughout; tabular-nums on numeric values instead of a separate monospace font.
4. Category divider bands use the numbered-eyebrow pattern ("01 WALLS") for every input group.
5. Every group ends with a dashed accent-blue "+ Add Section" button; Reset All must clear dynamically-added rows.
6. Footer: app name · company, version right-aligned; centered copyright line beneath.
