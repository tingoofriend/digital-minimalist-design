---
name: digital-minimalist-design
description: Use when designing or building app, web, widget, or desktop UI (mockups or front-end code) in a calm "digital minimalist" style — monochrome, text-first, one-purpose interfaces that avoid grabbing attention. Includes measured type sizes and spacing from real reference apps.
license: MIT
---

# Digital Minimalist Design

A design system for calm software: apps that do one thing, stay out of the way, and are often used without being opened at all.

Distilled from the app curation of the Digital Minimalist blog (all 162 posts read; ~815 images reviewed; key screens pixel-measured). Not affiliated with that blog or any app named here. App names are cited only as style references.

Reference apps: Weeklist, Life Dots, Mononote, Did I Do, Thoughts, Neuecast, Clear, MinimaList, Twodos, SyncTasks, Dumb Phone, Blank Spaces, Before Launcher, Lazy Weather, The Radio, Lettera, iA Writer, Matter, Instapaper, Endel, One Sec, Onigiri, One Thing, Ice, LookAway, Fliqlo, Mudita Kompakt (e-ink).

## 1. Principles (decide everything with these)

1. **Do one thing.** One app, one purpose. Remove before you add.
2. **Technology stays in the background.** Never pull attention: no color for its own sake, no badges, no notification dots, no recommendation feeds, no infinite scroll.
3. **Useful without opening.** Put the core information on widgets, the Lock Screen, Live Activities, the Dynamic Island, or the menu bar, and let one tap finish the job.
4. **Calm over stimulation.** Color and decoration count as stimulation. Grayscale is a deliberate choice.
5. **Text is the hero.** Prefer text labels over icons, thumbnails, and artwork.
6. **Hide to declutter.** Advanced features exist, but they live behind gestures, long-press, or a `···` menu.
7. **Good friction is allowed.** Put one deliberate step (a pause, a breath, a confirmation) in front of compulsive behavior.
8. **Private and account-free.** No sign-up, data stays on device, no ads. Say so in the UI copy.

## 2. Color

| Token | Light | Dark | Use |
|---|---|---|---|
| bg | `#F7F7F7` (alt `#F4F4F4`) | `#000000` | screen background |
| surface | `#FFFFFF` | `#1C1C1E` | widgets, cards, sheets |
| text | `#000000`–`#111111` | `#FFFFFF` | titles, body |
| text-2 | `#808080` | `#8E8E93` | dates, meta, counts |
| text-3 | `#BBBBBB` | `#48484A` | checkbox strokes, "Add item", completed items |
| divider | `#E2E2E2`, 1px | `#2C2C2E` | hairline separators |
| accent | **none** | **none** | emphasis = black (light) / white (dark) |

- Dark mode defaults to **true black `#000`** so it blends with the Lock Screen and OLED.
- **Allowed exceptions (pick at most one per app):**
  - *Warm paper:* cream background near `#F2EDE3` + serif type. For reading, learning, and vocabulary apps.
  - *Single accent object:* exactly one element on screen in color (for example a camera shutter pill). Everything else stays grayscale.
  - *Data signal:* tiny green/red only on small numeric deltas.
- No gradients, except a subtle black-to-gray on app icons and a soft gray panel on intervention screens.

## 3. Typography (measured; iPhone width 393 pt)

Use system sans-serif (SF Pro, Inter; Pretendard for Korean). Build hierarchy **only with size and weight contrast**, never with color, underline, or highlight.

| Role | Size / weight |
|---|---|
| Display numerals | 56–96 pt, Bold–Black, or Ultralight |
| Content title (player, reading) | **40–44 pt Bold, line-height 1.2** |
| Text-launcher app names | 28–34 pt Regular/Medium, line pitch ≈1.7× |
| Large title | 34 pt Bold |
| Section / date header | **20 pt Semibold** + same-size gray secondary ("**Mon** 5 Oct") |
| Text-only list row | 17 pt Regular, row pitch 40 pt |
| Checklist row title | **15 pt Regular** |
| Meta | **12 pt, text-2** |
| Widget title / count | 15 pt Bold / 15 pt text-2 |
| Widget item | 13 pt |
| Widget big answer | 36–40 pt Black (on a 158 pt widget) |

- At most 2–3 weights per screen. Use tabular figures for numbers.
- **Optional character typeface (one per app):** serif for reading bodies, vocabulary apps, and **Lock Screen clocks**; monospace for terminal or typewriter moods (weather, writing, data tables); pixel fonts for retro utilities.
- Text launchers often use **all-lowercase** labels. Both left-aligned and centered layouts are common.

See `references/measurements.md` for how these values were measured and their error margins.

## 4. Layout and spacing (measured)

- Horizontal margins: **20 pt** for lists, 22 pt for reading and player screens, 30–38 pt for launchers.
- Lists are single-column, left-aligned, and icon-free.
  - Checklist row: **20 pt** circular checkbox (1.5 pt stroke, text-3). Text starts at x = 58 pt.
  - Row pitch: **≈59 pt** with title + meta, **56 pt** single-line, 40 pt text-only.
  - Divider: 1 px, running from the text start to the trailing edge.
  - Completed items stay visible with **strikethrough + text-3**; don't remove them.
  - End each section with a single gray "Add item" row.
  - Counts are trailing gray numbers with a thin chevron (`3 ›`).
- Top bar: **44 pt** circular buttons (one icon each) left and right, with a short centered title. Or use a Large Title.
- Bottom bar: a ← → pill on the left and a round `+` (black or glass) on the right, **44–56 pt**. Add a tab bar only if truly needed.
- Leave most of the screen empty. Content sits near the top or center.

### iOS widgets

- Use system sizes (small = 158 pt; 20 pt gaps at 393 pt width), 16 pt inner padding, system corner radius.
- Title 15 pt Bold + trailing gray count; items 13 pt; 17 pt checkboxes; item pitch ≈25 pt.
- **Match the widget background to the wallpaper** so the text appears to float on the Home Screen.
- Tile widget: a small line icon at top-left and a label at bottom-left.

## 5. Shape and iconography

- Corner radius 20–24 pt (continuous). Buttons are pills or circles. Almost no shadows: separate layers with background contrast instead.
- Recurring motifs: **dot grids** (filled = black/white, remaining = light gray, header like "Year 67%"), thin ring timers, hairline progress bars, tick scales.
- UI icons: 1.5–2 pt line. Replace with text whenever possible.
- App icons: a white or black tile with one monochrome symbol or a wordmark. A subtle black-to-gray sheen is fine; color is not.
- Icon-pack style: **thick black outline glyphs with rounded corners**, inverted in dark mode. Folders: pale gray with a gray line glyph.
- Illustration, if any: **solid rounded black glyphs on light gray**. Avoid scenes and characters. A single monochrome line drawing is the most you should use.
- Tags/chips: black rounded rectangles with white text, or a 1 px outlined pill.

## 6. Component patterns

- **Text launcher:** a vertical list of large app names, with the date above it (thin ring clock or "Tuesday / June 2"). Black or white background.
- **Big-answer widget:** a one-line question (15 pt Bold) + one huge answer (Black, ≈25% of widget height) + a small timestamp.
- **Date widget:** "Thu **Nov**" (day black, month gray) above a giant "07".
- **Progress-dots widget:** a "Day 46%" header above a dot grid.
- **Single note:** the whole screen is one text area, with a black "Done" pill at the bottom.
- **Week view:** collapsible day sections, each with its own items and an "Add item" row.
- **Focus mode:** black screen, one task centered in bold white, a small timer below. Variant: a thin ring with a big number.
- **Intervention (friction) screen:** a single centered sentence inviting a pause. Next screen: one big number (e.g. attempts today), one white pill button, one text link.
- **Text-first player/detail:** a 40–44 pt bold title instead of artwork, a hairline progress bar, small controls.
- **Reading view:** serif body, line-height 1.6–1.7, 60–70 characters per line. Optional focus mode that grays out everything but the current sentence.
- **Menu bar app (macOS):** one icon or short text (e.g. "24:53"). Clicking opens a small white popover with one big number and pill choices.
- **Settings:** stock grouped lists, toggles only, no decoration.

## 7. Platforms

- **iOS:** use stock SwiftUI components and remove color (`.tint(.primary)`). Treat widgets, Live Activities, and the Dynamic Island as first-class. Use Liquid Glass sparingly (tinted/clear).
- **Android:** Material 3 with dynamic color off and a monochrome scheme. Elevation 0. Launcher-style text lists.
- **Web:** single column, 640–720 px, system fonts, one black pill CTA. Header: wordmark + 2–3 links.
- **macOS:** menu-bar first; small floating windows with only traffic lights; Graphite accent; plain Finder-style lists.
- **E-ink / low-stimulus:** pure black and white, outlined line icons inside rounded squares, 1.5–2 pt strokes.

## 8. Copy

- Short declarative sentences in second person: "Plan your week, then put the phone down." "Did you stretch today?" "Take a breath first."
- No exclamation marks, emoji, or hype. Empty states get one quiet sentence and one button.

## 9. Don'ts

- [ ] More than one accent color; color-coded category tags
- [ ] Red badges, streak flames, leaderboards
- [ ] Nested cards, heavy shadows, overused glass
- [ ] Icon + text duplicate labels; decorative illustration
- [ ] More than one primary button per screen
- [ ] Infinite feeds, recommendations, autoplay
- [ ] Forced sign-up onboarding; tutorials longer than 3 steps

## 10. Workflow

1. Write down the **one thing** this app does, in one sentence.
2. Design the surfaces that work without opening the app first: widget, Lock Screen, menu bar.
3. Start the main screen as a text list or a single big number, then apply sections 3–4.
4. Finish the hierarchy without color. Add gray steps or the one allowed exception only if needed.
5. Check against section 9, then ask whether one more element can go.
6. Render mockups and **check for clipping, overflow, and overlap** (elements outside their container, a cut-off last row, words breaking mid-word in CJK; use `word-break: keep-all` for Korean).

## 11. Starter tokens

See `references/tokens.css` for a drop-in CSS file. SwiftUI equivalents:

```swift
extension Color {
    static let dmBackground = Color(light: 0xF7F7F7, dark: 0x000000)
    static let dmSurface    = Color(light: 0xFFFFFF, dark: 0x1C1C1E)
    static let dmText2      = Color(light: 0x808080, dark: 0x8E8E93)
    static let dmText3      = Color(light: 0xBBBBBB, dark: 0x48484A)
    static let dmDivider    = Color(light: 0xE2E2E2, dark: 0x2C2C2E)
}
// Header: .font(.system(size: 20, weight: .semibold))
// Row:    .font(.system(size: 15))        Meta: .font(.system(size: 12)).foregroundStyle(Color.dmText2)
// Margins: .padding(.horizontal, 20)      Row min height: 56 / 59
```

(`Color(light:dark:)` is a small helper you define once, built on `UIColor { traits in ... }`.)
