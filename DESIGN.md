# REPS design rules

REPS is used mid-session, on a phone, one-handed, between sets. Every screen
is judged against that moment. These rules apply to every change in `v2.html`.

## Principles
1. **Less, but better (Rams).** Every element earns its place on the main path.
   If unsure, it goes behind a tap.
2. **Don't make me think (Krug).** The next action is obvious without reading.
3. **Progressive disclosure.** Show what's needed now; the rest is one tap
   away (Adjust, More, ⓘ, the coach).
4. **Fewer choices on screen (Hick).** Settings that rarely change do not sit on
   the main screen.
5. **Thumb zone (Fitts).** The primary action is big and at the bottom.
6. **Data-ink (Tufte).** No decoration that carries no information: no
   repeated labels, no decorative badges, no emoji as icons.

## Screens: one job each
- **Today:** what do I do now, and log it.
- **Week:** see and rearrange the week.
- **Progress:** am I getting better.
- **Settings** (gear icon): location and kit legs, races, hand stages,
  preferences, backup, coach sync.

## Hard limits
- The first exercise is visible without scrolling on a 390 × 844 screen.
- One primary button per screen, pinned at the bottom while training.
- At most one hint line per screen. No explanatory paragraphs on the main path;
  the "why" lives behind ⓘ or with the coach.
- At most one badge per card.
- Session options (time, pairs or straight sets, warm-up length, kit) live in
  one **Adjust** sheet.
- Secondary actions (move, skip, add exercise, cardio, quick workout, pause)
  live in one **More** sheet.

## Visual system
- **Colour is semantic: every colour has one job, and the same job everywhere.**
  | Colour | Means |
  |---|---|
  | Blue (`--accent`) | Lift sessions, **pairs** (alternate on the clock), the primary button, links, a suggested weight |
  | Purple | **Supersets** (back to back) |
  | Grey | **Straight sets**, neutral information |
  | Green | Runs, done, ↑ add weight |
  | Lime | Conditioning, finishers |
  | Amber | Warm-up, "find your weight" |
  | Red | The hand and warnings |
  Structure is shown with colour plus a label (rail + tag + badge), never colour
  alone. No decorative colour that means nothing.
- **Type scale (the only sizes allowed):** 34 display (screen title), 22 sheet
  title, 20 numbers (maxes, stats), 15 body and names, 13 meta, 12 labels.
  Barlow Condensed italic for 34/22/20 only; Plus Jakarta Sans for the rest. Use
  weight for hierarchy, not extra sizes. No ALL-CAPS, no letter-spacing.
- **Spacing:** multiples of 4, mostly 8, 16 and 24. Side gutter 16.
- **Surfaces:** white cards with 14px radius on cream. No borders inside
  borders, no shadows on nested cards.
- **States:** an exercise is not started (0/4), in progress (2/4) or done
  (filled ✓). It looks the same everywhere.

## Gym-floor ergonomics
- Tap targets are at least 44pt; set inputs at least 40pt tall.
- Numbers are readable at arm's length (15pt+, semibold).
- Number keypad for kg and reps. Nothing needs two hands.

## Copy
- Plain, short, second person. Units always shown ("22 kg", "4 × 4–6").
- Exercise meta line: `sets × reps · weight cue`. Nothing else.
- Say it once: if the header says the week's effort, no exercise repeats it.

## Before shipping a UI change
- Screenshot it at 390 × 844 and check the hard limits above.
- If it adds something to the main path, say what it replaces.
