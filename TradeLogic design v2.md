# TradeLogic Report Design System

Extracted from `TradeLogic Market Report 071926 v2.pdf` (The Contech Industry Review) and the TradeLogic logo, for reuse on future reports.

## Logo

![TradeLogic logo](./TradeLogic_logo.png)

## Brand Colors

| Token | Hex | Use |
|---|---|---|
| Brand Blue | `#518AD5` | Logo mark only |
| Ink Black | `#000000` | Logo wordmark |
| Report Navy (dark) | `#0A1D3D` | Cover background |
| Report Navy (band) | `#0C213F` | Category header bands, headings, footer text |
| Accent Blue | `#3F7ED1` | Section numbers, field labels, accent bar, links |
| Card Navy | `#182A48` | Stat cards on cover |
| Body Text | `#26313D` | Paragraph copy on white pages |
| Muted Gray | `#7C8898` | Secondary/caption text |
| Rule Gray | `#CED2D8` | Table dividers |
| White | `#FFFFFF` | Body page background, headline text on navy |

Note: the logo's brand blue (`#518AD5`) sits close in hue to the report's accent blue (`#3F7ED1`) but is lighter. Keep brand blue reserved for the mark itself; use the accent blue for document chrome (labels, numerals, rules) so long-form reports stay readable.

## Typography

- Typeface: Helvetica (Regular, Bold, Oblique) — clean sans-serif throughout, no serif or display font.
- Cover title: Bold, ~40–44pt, white, two-line max, tight leading.
- Cover eyebrow (kicker): Bold, ~11pt, uppercase, letter-spaced, accent blue on navy.
- Cover stat numbers: Bold, ~28pt, white; stat labels: Bold, ~8pt, uppercase, muted blue-gray.
- Section number ("01.1"): Bold, accent blue, same size as heading.
- Section/company heading: Bold, ~16pt, navy.
- Ticker/tag next to heading (e.g. "NYSE: PCOR"): Regular, small caps or upper, muted gray, same baseline as heading.
- Field label (left column, e.g. "PROBLEM SOLVED"): Bold, ~9pt, uppercase, accent blue, can wrap to two lines.
- Body copy (right column): Regular, ~10.5pt, body text color, 1.3–1.4 line height.
- Footer: Regular, ~8pt, muted gray/navy, uppercase for report name.

## Layout Patterns

**Cover page**
- Full-bleed dark navy background.
- Content inset ~150px from left edge.
- Vertical accent bar (4px wide, accent blue) to the left of the title block.
- Eyebrow label above title, title, then 2–4 line description.
- Row of stat cards (equal width, card-navy background, rounded corners) below the description — big bold number + small uppercase label.
- Thin horizontal rule near bottom, footer metadata line beneath it (report name • date • confidentiality).

**Category divider (section header band)**
- Full-width navy band near top of page.
- Large bold section number (e.g. "01") on the left, aligned with the eyebrow/heading block.
- Eyebrow line: "FUNCTIONAL CATEGORY X OF N" in accent blue, bold, uppercase.
- Category title: bold, white, large.
- "TOP 5" list line beneath: bold label + accent-colored, pipe/dot-separated list.

**Profile entry (two-column definition list)**
- Sub-heading row: "01.1  Company Name  TICKER" with a full-width rule beneath.
- Below that, a label/value table: left column ~22% width, bold uppercase accent-blue labels (can wrap); right column body text.
- Each row separated by a thin light-gray rule; generous vertical padding (~16–20px) between rows so the page reads as a scannable spec sheet, not a wall of text.
- Twelve standard fields per entry, always in the same order (Problem Solved, Target Demographics, Financial Metrics, Pricing Model, Packaging & Availability, Role of AI, Technology Stack, Data Security/Privacy/Governance, Future Outlook, Acquisition History, Day-One-to-Now Trajectory, Why They Lead the Category).

**Page footer (body pages)**
- Thin rule across the page width.
- Left: report name • edition, uppercase, small, muted.
- Right: page number.

## Voice & Content Conventions

- Every claim is sourced or explicitly flagged "not publicly disclosed" / "not independently verified here" — no invented numbers.
- Repeated entities (e.g. a company appearing in multiple categories) are cross-referenced ("Full profile under Category 01") rather than restated.
- Tickers/ownership status shown inline next to company names (public ticker, "Private", or parent company).
- Reports close with a "Disclosures & Primary Sources" page listing source categories and reiterating limitations.

## Reuse Checklist for New TradeLogic Reports

1. Cover: navy background, accent bar, title + description, 3–4 stat cards, footer rule.
2. One navy divider band per category/section with number, eyebrow, title, and "TOP 5"-style summary line.
3. Entries as label/value tables with accent-blue uppercase labels and thin gray row dividers.
4. Helvetica throughout; accent blue `#3F7ED1` for structural/navigational elements, navy `#0C213F` for headings and dividers, body text `#26313D`.
5. Reserve brand blue `#518AD5` for the TradeLogic logo only.
6. Close with a sources/limitations page.
