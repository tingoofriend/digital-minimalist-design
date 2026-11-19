# How the numbers were measured

The type sizes, spacing, and colors in `SKILL.md` were measured from promotional screenshots of reference apps, not taken from official specs. Treat them as close approximations.

## Method

1. Load the screenshot at native resolution and read pixels on a canvas.
2. Find the phone screen edges by scanning for the dark bezel. Set the scale so screen width = 393 pt (iPhone 15/16 Pro). Screen height came out at ≈854 pt, which cross-checks against 852 pt.
3. Inside the screen, find text lines as horizontal bands of "ink" pixels (luminance below a threshold). Record each band's height, x-extent, and darkest luminance.
4. Convert band height to font size with SF Pro metrics: cap height ≈ 0.705 em, ascender + descender ≈ 0.95 em. Subtract about 1 px of anti-aliasing per edge.
5. Round to the nearest common iOS size.

Expected error: **about ±1 pt** for type, ±2 pt for spacing. Colors come from the darkest core pixel of anti-aliased glyphs, so gray values may be slightly darker than the true fill.

## Raw values

| Reference screen | Measurement | Result |
|---|---|---|
| Week list app, light | background luminance | 247 → `#F7F7F7` |
| | divider luminance | 226 → `#E2E2E2` |
| | day header "Mon" cap band | 15.1 pt → ≈20 pt Semibold |
| | row title (with descender) | 15.1 pt band → ≈15 pt |
| | meta | 10.6 pt band → ≈12 pt, luminance ≈133 |
| | date secondary text | luminance ≈127 → `#808080` |
| | "Add item" / checkbox stroke | luminance ≈186–193 → `#BBBBBB` |
| | checkbox | ≈20 pt circle; text starts at x ≈ 58 pt |
| | row pitch | 59 pt (2-line), 56 pt (1-line) |
| | left/right margin | ≈20 pt |
| | toolbar buttons | ≈44 pt circles |
| Home Screen widgets | small widget | 158 pt, 20 pt gap |
| | widget title / count | ≈15 pt Bold / 15 pt gray |
| | widget items | ≈13 pt, pitch ≈25 pt, checkbox ≈17 pt |
| Text-only to-do list | row text | ≈17 pt, pitch ≈40 pt, margin ≈20 pt |
| Text-first podcast player | episode title | ≈44 pt Bold, line pitch 52 pt (1.2) |
| | margin | ≈22 pt |
| Text launcher (large) | app name | ≈34 pt, line pitch ≈58 pt, margin ≈38 pt (screen width estimated; ±10%) |
| Yes/No widget | answer | ≈38 pt Black on a 158 pt widget (visual estimate) |
