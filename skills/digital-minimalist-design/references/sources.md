# Sources

## Static style (sections 1–6)

- The app curation of the Digital Minimalist blog (all 162 posts read, ~815 images reviewed, key screens pixel-measured). Not affiliated. See `measurements.md` for the method.

## Behavior (section 7)

These references were chosen because they share the same philosophy as the static style: minimal attention, quiet feedback, no manipulation.

| Topic | Reference | What we took from it |
|---|---|---|
| Attention | Mark Weiser & John Seely Brown, "Designing Calm Technology" (1995); Amber Case, *Calm Technology* (O'Reilly, 2015) and calmtech.com | Require the smallest possible amount of attention; use the periphery; communicate without speaking; work even when it fails |
| Motion | Apple HIG, *Motion* | Add motion purposefully; keep feedback brief and precise; avoid motion on frequent interactions; let people cancel motion; never rely on motion alone |
| Easing / duration | Material Design 3, *Easing and duration* tokens | Standard `cubic-bezier(0.2, 0, 0, 1)`, decelerate `(0, 0, 0, 1)`, accelerate `(0.3, 0, 1, 1)`; short durations for small, frequent changes |
| Haptics | Apple HIG, *Playing haptics* | Prefer short haptics for discrete events; use them consistently; match intensity to the visual; don't overuse |
| Widgets | Apple HIG, *Widgets* | Deep-link to the right place; simple interactivity (toggles) without app-like layouts; update when data changes; system-rendered dates/times; data-change animations up to 2 s; 16 pt margins; text ≥ 11 pt |
| Live Activities | Apple HIG, *Live Activities* | Only for tasks with a defined start and end; update only when content changes; tap opens the right location; end promptly |
| Notifications | Apple HIG, *Notifications* | Ask for consent; use alerts, not notifications, for errors; badges only for unread notifications |
| Gestures | Clear (Realmac) and the gesture-driven list pattern | Swipe right to complete, swipe left to delete, pull to add, contextual cues that follow the finger |
| Contrast | WCAG 2.2, 1.4.3 Contrast (Minimum) | 4.5:1 for normal text; computed ratios for this palette are listed in `SKILL.md` section 7 |

Durations and thresholds in section 7 (100–150 ms, 200–250 ms, 300 ms cap, 40% swipe threshold, 5 s undo, 300 ms loading delay) are our own choices within these guidelines, not values copied from a single source.
