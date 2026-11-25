---
name: digital-minimalist-design
description: Use when designing or building app, web, widget, or desktop UI (mockups or front-end code) in a calm "digital minimalist" style — monochrome, text-first, one-purpose interfaces that avoid grabbing attention. Includes measured type and spacing plus rules for motion, gestures, haptics, states, notifications, and accessibility.
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
| text-2 | `#707070` (measured `#808080`) | `#8E8E93` | dates, meta, counts. `#808080` is only 3.7:1, so use `#707070` for small text (see §7) |
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

## 7. Behavior: motion, interaction, and states

The static rules above came from screenshots. This section covers what screenshots can't show. It is grounded in references that share the same philosophy: Calm Technology (Weiser & Brown; Amber Case), Apple HIG (Motion, Playing haptics, Widgets, Live Activities, Notifications), Material 3 motion tokens, and gesture-first lists like Clear. See `references/sources.md`.

**Rule of thumb:** behavior should be noticed only when it carries information, then get out of the way.

### Motion

- **Default to no custom motion.** Frequent interactions (tapping rows, opening the same screen again) get only the system's built-in animation. Add motion only to explain a change: where something went, what just changed.
- **Durations:**
  - Micro feedback (checkbox, toggle, press state): **100–150 ms**
  - In-place changes (row collapse, strikethrough, reorder settle): **200–250 ms**
  - Screen transitions: use the platform default (push, sheet); don't customize
  - Nothing over **300 ms** in regular UI, except system widget updates and deliberate pacing screens (below)
- **Easing:** standard `cubic-bezier(0.2, 0, 0, 1)` for moves, decelerate `(0, 0, 0, 1)` for entering, accelerate `(0.3, 0, 1, 1)` for exiting (Material 3). SwiftUI: `.smooth(duration: 0.25)` or `.easeOut(duration: 0.2)`. Springs must be critically damped (`.smooth`): **no overshoot**.
- **Allowed:** fade, crossfade, short slide (≤ 12 pt), height collapse, strikethrough drawn left to right.
- **Not allowed:** bounce, overshoot, scale-pop, confetti, parallax, shimmer skeletons, attention-pulsing, any looping animation on an idle screen.
- **Numbers change in place.** Use a crossfade or `.contentTransition(.numericText())`, never a count-up.
- **Motion never blocks input** and can always be interrupted.
- **Pacing exception:** breathing, focus, and intervention screens may use slow, rhythmic motion (e.g., a ring that expands over 4 s and contracts over 4 s), because slowing down is the point. Keep it low-amplitude and monochrome, and let people skip it.

### Gestures and direct manipulation

- **Gestures are shortcuts, never the only path.** Every gesture has a visible equivalent (button, menu item).
- **List rows:** swipe right = complete, swipe left = delete or archive. Reveal a monochrome cue (✓ / ×) that follows the finger. Commit at about 40% of row width; below that, snap back.
- **Tap the checkbox** to complete. **Tap the text** to edit it inline. Single-line items don't need a separate edit screen.
- **Long-press** opens secondary actions (context menu); long-press then drag reorders.
- **Pull-to-add** at the top of a list is fine (Clear-style), as long as a `+` button also exists.
- **Undo over confirm.** Destructive actions happen at once and show a text-only "Undo" toast for about 5 s. Only irreversible bulk actions get a confirmation dialog.

### Haptics

- **Only for discrete, meaningful events:** completing an item (light impact), toggling (selection), snapping into place during a drag (selection). Never for scrolling, navigation, or every tap.
- **One event, one pattern,** used consistently. Keep intensity light to match the restrained motion.
- Respect system settings. Haptics are never the only feedback.

### Feedback and states

- **Saving is silent.** Autosave everything; no "Saved!" toasts. Show state only when something fails.
- **Loading:** show nothing for the first 300 ms, then one thin spinner or a hairline progress bar. No skeleton shimmer. Prefer local-first data so lists render instantly.
- **Empty:** one quiet sentence and one button.
- **Error:** plain-language inline text with a "Try again" text button. Use an alert only when the error blocks the task. No red banners.
- **Offline:** keep working. Show a small "Offline" label in the top bar and sync quietly later.
- **Completion:** strikethrough + text-3 over 200 ms. The item stays visible (until the day ends or the next open). No celebration, no streak counter.
- **Session end** (focus, timer): one sentence and one number. No confetti.

### Notifications (opt-in, rare)

- **Never ask on first launch.** Ask for permission only when the person creates something that needs a reminder.
- **Send only what the person scheduled** (their reminder, their timer) or a time-critical event they asked for. No re-engagement, streak, recap, or promotional notifications.
- **Text:** what + when, in sentence case. No emoji, no app name, no exclamation marks. Offer actions like "Done" and "Snooze".
- **No badge,** unless it counts truly unread items the person cares about.
- **Prefer passive surfaces** (widget, Lock Screen, Live Activity) over a push.
- **Live Activities** only for things with a defined start and end (focus session, timer). Update only when content changes, end promptly, and make a tap open that exact item.

### Widgets and glanceable surfaces

- **Interactive where it saves a trip:** a widget can complete a task with a toggle without opening the app. A tap anywhere else deep-links to the exact item or day, never the app's home.
- **Update when the data changes.** Let the system render dates, times, and timers so you don't spend refresh budget. Data-change animation stays the system default (Apple allows up to 2 s).
- **Lock Screen:** assume others can see it. Avoid sensitive content and support redaction.

### Accessibility

- **Contrast:** the measured secondary gray `#808080` is only **3.7:1** on `#F7F7F7`, below WCAG AA (4.5:1) for small text. Use **`#707070` (4.6:1)** for small secondary text by default; keep `#808080` for large text or non-essential meta. text-3 (`#BBBBBB`, 1.8:1) is for decoration and disabled states only, never for information. In dark mode, `#8E8E93` on `#000` is 6.4:1 (fine).
- **Increase Contrast:** darken text-2 and text-3 one step and show dividers at full strength.
- **Dynamic Type:** support accessibility sizes. Rows grow in height, and big numerals may scale down (minimum scale 0.6) but never truncate.
- **Reduce Motion:** replace slides with crossfades, cap durations at 150 ms, and stop pacing animations (show a static ring plus a countdown).
- **VoiceOver:** label every icon-only button, announce completion state ("Completed"), and expose swipe actions as accessibility actions.
- **Hit targets ≥ 44 pt** even when the visual is smaller (a 20 pt checkbox sits in a 44 pt tap area).

## 8. Platforms

- **iOS:** use stock SwiftUI components and remove color (`.tint(.primary)`). Treat widgets, Live Activities, and the Dynamic Island as first-class. Use Liquid Glass sparingly (tinted/clear).
- **Android:** Material 3 with dynamic color off and a monochrome scheme. Elevation 0. Launcher-style text lists.
- **Web:** single column, 640–720 px, system fonts, one black pill CTA. Header: wordmark + 2–3 links.
- **macOS:** menu-bar first; small floating windows with only traffic lights; Graphite accent; plain Finder-style lists.
- **E-ink / low-stimulus:** pure black and white, outlined line icons inside rounded squares, 1.5–2 pt strokes.

## 9. Copy

- Short declarative sentences in second person: "Plan your week, then put the phone down." "Did you stretch today?" "Take a breath first."
- No exclamation marks, emoji, or hype. Empty states get one quiet sentence and one button.

## 10. Don'ts

- [ ] More than one accent color; color-coded category tags
- [ ] Red badges, streak flames, leaderboards
- [ ] Nested cards, heavy shadows, overused glass
- [ ] Icon + text duplicate labels; decorative illustration
- [ ] More than one primary button per screen
- [ ] Infinite feeds, recommendations, autoplay
- [ ] Forced sign-up onboarding; tutorials longer than 3 steps

## 11. Workflow

1. Write down the **one thing** this app does, in one sentence.
2. Design the surfaces that work without opening the app first: widget, Lock Screen, menu bar.
3. Start the main screen as a text list or a single big number, then apply sections 3–4.
4. Define behavior with section 7: what moves, what gives haptic feedback, what notifies (usually nothing), and every state (loading, empty, error, offline, done).
5. Finish the hierarchy without color. Add gray steps or the one allowed exception only if needed.
6. Check against section 10, then ask whether one more element can go.
7. Render mockups and **check for clipping, overflow, and overlap** (elements outside their container, a cut-off last row, words breaking mid-word in CJK; use `word-break: keep-all` for Korean).

## 12. Starter tokens

See `references/tokens.css` for a drop-in CSS file. SwiftUI equivalents:

```swift
extension Color {
    static let dmBackground = Color(light: 0xF7F7F7, dark: 0x000000)
    static let dmSurface    = Color(light: 0xFFFFFF, dark: 0x1C1C1E)
    static let dmText2      = Color(light: 0x707070, dark: 0x8E8E93) // 4.6:1
    static let dmText3      = Color(light: 0xBBBBBB, dark: 0x48484A)
    static let dmDivider    = Color(light: 0xE2E2E2, dark: 0x2C2C2E)
}
// Header: .font(.system(size: 20, weight: .semibold))
// Row:    .font(.system(size: 15))        Meta: .font(.system(size: 12)).foregroundStyle(Color.dmText2)
// Margins: .padding(.horizontal, 20)      Row min height: 56 / 59
// Motion:  .animation(.smooth(duration: 0.25), value: done)   // no bounce
// Haptics: .sensoryFeedback(.impact(weight: .light), trigger: done)
```

(`Color(light:dark:)` is a small helper you define once, built on `UIColor { traits in ... }`.)
