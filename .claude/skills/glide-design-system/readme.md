# Glide — Design System

Glide is a **calm, playful study app for high-school and college students**, built for macOS and iOS. It helps students plan work, focus in sessions, review with flashcards, and build gentle streaks — without the anxiety-inducing, gamified pressure of most productivity tools. The whole product should feel like a deep breath: warm paper, soft edges, and encouraging words.

> **Product surfaces:** iOS app (phone) · macOS app (desktop). No marketing website is in scope yet.

## Sources

This system was authored **greenfield** — no codebase, Figma file, or existing brand assets were provided. The visual direction (calm + playful + focused) was derived from the product brief. Everything here is original:

- **Fonts** are loaded from **Google Fonts CDN** (Bricolage Grotesque, Hanken Grotesk, JetBrains Mono) rather than bundled binaries — see *Caveats*.
- **Icons** use **Lucide** (CDN) — a friendly, rounded line-icon set that matches Glide's soft aesthetic.
- **Logo** is an original wordmark + paper-plane mark (`assets/logo-mark.svg`, `assets/logo-wordmark.svg`).

If a real brand kit or Figma exists, re-attach it and this system should be reconciled against it.

---

## Content fundamentals — how Glide talks

Glide speaks like a **calm, encouraging study buddy** — never a stern coach, never a hype-machine.

- **Voice:** warm, plain-spoken, quietly playful. Second person ("you"), and "we" when Glide is doing something for you. Never corporate.
- **Casing:** **Sentence case everywhere** — buttons, titles, menus. No Title Case, no ALL CAPS except tiny eyebrow labels.
- **Tone:** low-pressure and forgiving. Celebrate small wins, never shame. A missed day is "Let's pick it back up," not "You broke your streak!"
- **Length:** short. Headlines are 2–5 words. Body copy is one gentle sentence where possible.
- **Playful, not silly:** a light touch of warmth and the occasional soft metaphor tied to the name — *glide, drift, coast, breeze, flow, land*. Used sparingly, never punny overload.
- **Emoji:** **avoid in product UI.** Personality comes from words, color, and the mark — not emoji. (A single celebratory sparkle in an empty-state illustration is the ceiling.)

**Examples**

- Empty task list → *"Nothing on deck. Enjoy the calm, or add your first task."*
- Focus session start → *"Let's glide. 25 minutes, phone down."*
- Session complete → *"Nice work. That's 25 focused minutes in the bank."*
- Streak nudge → *"3 days in a row. You're in a good rhythm."*
- Broken streak → *"Yesterday slipped by — no worries. Start a fresh one today."*
- Primary buttons → *"Start focusing"*, *"Add task"*, *"Review deck"*, *"Land it"*.
- Error → *"That didn't save. Mind trying again?"*

---

## Visual foundations

**Overall feel:** warm paper, soft periwinkle, rounded everything. Airy and unhurried. Lots of whitespace. Nothing sharp, nothing loud.

- **Color:** A warm off-white **paper** base (`--paper-50`) rather than stark white. Primary is a soft **periwinkle "Glide" blue** (`--glide-500 #6c7bf0`) — calm, focused, not corporate-blue. Playful accents come from **sage** (success/focus), **apricot** (streaks/warmth), and **lilac** (gentle tertiary). Text is a soft warm near-black (`--ink-900 #292933`), never pure `#000`. Saturation is kept low across the board for calm.
- **Type:** Display in **Bricolage Grotesque** (warm, slightly characterful) for headings and big moments; **Hanken Grotesk** for all UI and body (clean, friendly, highly legible); **JetBrains Mono** for timers, counters, and stats. Tight tracking on large display sizes, generous line-height (1.5–1.7) on body for relaxed reading.
- **Backgrounds:** solid warm paper, occasionally a very soft single-hue tint wash (`--glide-50`, `--sage-50`). **No busy gradients, no photographic hero images** in-app. A subtle two-stop tint (e.g. paper → faint glide) is the most that appears on feature cards. Optional soft grain is acceptable but low.
- **Corner radii:** generous and consistent — inputs/buttons `--radius-sm` (10px), cards `--radius-md` (14px), panels/sheets `--radius-lg` (20px), modals/hero `--radius-xl` (28px), pills/avatars/rings fully round. Roundness is a core brand signal.
- **Cards:** white (`--surface-card`) on paper, `--radius-md`, a **soft diffuse shadow** (`--shadow-sm`/`--shadow-md`) and usually a 1px `--border-soft`. Never a hard drop shadow, never a colored left-border accent stripe.
- **Shadows:** soft, low-contrast, warm-tinted (`rgba(41,41,51,…)`), diffuse and large-radius. A colored `--shadow-glide` glow appears only on the primary button and the active focus ring — used sparingly. Wells/sunken surfaces use a subtle `--shadow-inset`.
- **Borders:** hairline, warm (`--paper-200/300`). Used to define cards and inputs quietly; color does the heavy lifting, not heavy strokes.
- **Motion:** gentle and glide-y. Standard easing `--ease-glide` (a smooth decelerate, no overshoot) for chrome; a soft spring/bounce is reserved *only* for celebratory moments (streak earned, session complete). Durations 140–380ms. Transitions fade + subtle translate/scale; nothing snaps.
- **Hover states:** primary buttons darken one step (`--primary` → `--primary-hover`) and lift slightly (`translateY(-1px)` + stronger shadow). Ghost/subtle controls get a faint tint fill (`--glide-50` / `--paper-100`). Never opacity-only.
- **Press states:** scale down subtly (`scale(0.97–0.98)`), darken to `--primary-press`, drop the lift. Quick (`--dur-fast`).
- **Focus:** always a visible `--ring` (3px soft glide halo). Accessibility is non-negotiable even in a calm UI.
- **Transparency & blur:** used for overlays and floating chrome only — modal scrims (`--surface-overlay`), and iOS-style translucent tab bars / sheets with backdrop blur. Content surfaces stay opaque for readability.
- **Imagery vibe:** if photos ever appear, warm and softly lit, low-contrast, gentle. Illustration style is simple, rounded, flat with soft fills — matching the mark.

---

## Iconography

- **Set:** **[Lucide](https://lucide.dev)** — rounded-cap, 2px stroke line icons. Loaded from CDN (`https://unpkg.com/lucide@latest`). Their soft, even stroke and rounded joints match Glide's calm-rounded aesthetic exactly.
- **Style:** line (outline) icons only, `stroke-width: 2`, `stroke-linecap: round`, `stroke-linejoin: round`. Default size 20–24px, `--text-muted` or `--text-body` color; primary color only when active.
- **No emoji** as icons in product chrome. No mixed icon sets. No filled/duotone icons except the app logo mark.
- **Common icons:** `book-open`, `check`, `circle`, `play`, `pause`, `timer`, `flame` (streaks), `calendar`, `plus`, `layers` (decks), `sparkles`, `moon`, `settings`, `chevron-right`.
- **Logo:** the paper-plane mark (`assets/logo-mark.svg`) is the one duotone/filled asset — a gliding plane with a soft motion trail on a rounded glide-blue tile. Wordmark pairs it with "Glide" set in Bricolage Grotesque.

Usage in HTML/JSX: include `<script src="https://unpkg.com/lucide@latest"></script>`, add `<i data-lucide="timer"></i>`, then call `lucide.createIcons()`.

---

## Index — what's in this system

**Foundations**

- `styles.css` — global entry point (link this one file). `@import` manifest only.
- `tokens/colors.css` · `typography.css` · `spacing.css` · `effects.css` · `fonts.css` · `base.css`
- Foundation specimen cards live beside the tokens and show in the **Design System** tab (groups: Type, Colors, Spacing, Brand).

**Components** (`components/`) — reusable React primitives. See each `*.prompt.md`.

- `core/` — Button, IconButton, Badge, Tag, Avatar, Card, Divider
- `forms/` — Input, Textarea, Checkbox, Radio, Switch, SegmentedControl, Select
- `feedback/` — ProgressBar, Toast, Tooltip, Dialog
- `study/` — TimerRing, TaskItem, Flashcard, StreakBadge, StatTile

**UI kits** (`ui_kits/`) — full interactive screen recreations.

- `ios/` — Glide iOS app (Today, Focus timer, Decks/review, Streaks)
- `macos/` — Glide macOS app (planner + focus workspace)

**Assets** (`assets/`) — `logo-mark.svg`, `logo-wordmark.svg`.

**`SKILL.md`** — makes this system usable as a downloadable Agent Skill.

---

## Caveats

- **Fonts are CDN, not bundled.** `tokens/fonts.css` uses Google Fonts `@import`. For offline/production self-hosting, add `.woff2` files under `assets/fonts/` and swap in `@font-face` rules. → *If you have preferred/licensed brand fonts, send them and I'll wire them in.*
- **Greenfield brand.** Colors, type, logo, and voice are proposed directions, not an existing brand. Everything is easy to retune — tell me what feels off.
