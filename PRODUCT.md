# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

High-school and college students, discovering Glide for themselves. They arrive
mostly on a phone, usually from social or word of mouth, in a moment between
other things — not at a desk doing research. They are the deciders: there is no
parent, teacher, or admin to convince, and no separate buyer to design a second
argument for.

Their situation is the one the product is built around: work is piling up,
existing productivity tools have made them feel behind rather than capable, and
they are looking for something that will help them start rather than something
that will grade them.

## Product Purpose

Glide is a calm, playful study app for macOS and iOS. It helps students plan
work, focus in timed sessions, review with flashcards, and build gentle streaks.

It exists because most study and productivity tools apply pressure — gamified
guilt, broken-streak shaming, dense dashboards — and that pressure is precisely
what stops students from starting. Glide's purpose is to make beginning a study
session feel low-stakes. The product should feel like a deep breath.

This repository is **Glide's marketing website**: the surface that introduces
Glide to a student and moves them toward the apps. The product itself lives in
the native iOS and macOS apps; the web surface is persuasion, not product.

Success for the site is a student who understands what Glide feels like — not
just what it does — and who wants in. Because there is no public build yet
(see Capabilities and Constraints), that currently means capturing intent, not
a download.

## Positioning

Glide competes on emotional register, not feature count. Its differentiator is
that it is deliberately forgiving: a missed day is "Let's pick it back up," not
"You broke your streak." Calm is the mechanism, not the decoration — the low
saturation, soft edges, gentle motion, and non-shaming copy are how the product
works, not how it is dressed.

A neighboring study app can copy the feature list — tasks, timer, flashcards,
streaks — but cannot truthfully claim the same posture toward the user while
still running the standard pressure-and-guilt loop.

## Operating Context

- Students find Glide on a phone, in a small window of attention, often already
  slightly stressed about the work they are avoiding.
- The real usage scene is the study session itself: a phone face-down during
  focus time, a Mac open with a planner and timer beside actual coursework.
- The four things a student actually does in Glide: plan tasks, run a focus
  session, review a deck, keep a streak.
- Glide's native surfaces are the iOS phone app and the macOS desktop app. The
  web has no product functionality and is not a third client.

## Capabilities and Constraints

- **Lifecycle: pre-launch. There is no public build.** No App Store listing, no
  TestFlight link, nothing downloadable. The site must not imply availability,
  must not render a store badge that goes nowhere, and must not use
  download-now language. Its call to action captures interest (waitlist / email)
  until a real build exists.
- App features that may be described: task planning, timed focus sessions,
  flashcard decks and review, streaks. Nothing beyond this list is confirmed.
- Platforms that may be named: macOS and iOS. Android, web app, and any
  integrations are **not** confirmed and must not appear.
- Pricing is undecided. No price, no "free," no "free trial," no tier table
  until it is settled.
- No user counts, ratings, download numbers, school names, or launch dates
  exist. None may be stated or implied, including as placeholder-looking
  numerals.

## Brand Commitments

Glide already has a complete, binding design system at
`.claude/skills/glide-design-system/` (invocable as the `glide-design-system`
skill). It is the **token source and brand authority**: the palette, the type
families, the logo and the voice all come from there and are not reinvented.

It is not, however, the authority on how this website looks. The design system
was authored for the iOS and macOS apps, where calm restraint is the point. The
web surface has a different job and deploys the same tokens differently. **The
web's visual world is recorded in `DESIGN.md` at the project root**, and that
file governs this repo's rendering. Where the two differ on expression, the app
system wins for the app and `DESIGN.md` wins for the web; where they differ on
brand, the design system always wins.

- **Name:** Glide. Mark is an original paper-plane logo with a soft motion
  trail; wordmark sets "Glide" in Bricolage Grotesque.
  (`assets/logo-mark.svg`, `assets/logo-wordmark.svg`)
- **Voice:** warm, plain-spoken, quietly playful — a calm study buddy, never a
  stern coach and never a hype machine. Second person; "we" when Glide acts for
  you.
- **Casing:** sentence case everywhere, including buttons and headings. No Title
  Case, no ALL CAPS beyond tiny eyebrow labels.
- **Tone:** low-pressure and forgiving. Celebrate small wins; never shame.
- **Length:** short. Headlines 2–5 words; body one gentle sentence where
  possible.
- **Metaphor:** a light touch of the name's own vocabulary — glide, drift,
  coast, breeze, flow, land — used sparingly, never as pun overload.
- **No emoji in product UI.** Personality comes from words, color, and the mark.
- **Tokens and foundations** (colors, type, spacing, effects, motion, radii,
  shadows) are defined in `.claude/skills/glide-design-system/tokens/` and
  documented in that skill's `readme.md`. Type is Bricolage Grotesque (display),
  Hanken Grotesk (body), JetBrains Mono (timers/stats); icons are Lucide, line
  only.
- **Motion character is binding across surfaces:** smooth decelerate for chrome,
  with spring or bounce reserved for genuinely celebratory moments (a streak
  earned, a session completed). This rule holds on the web too.
- **Fonts are self-hosted on the web.** `src/assets/fonts/` carries latin-subset
  variable `.woff2` files for all three families, so the site makes no external
  font requests. No licensed brand fonts exist; these are the same open faces
  the design system names.
- The brand is **greenfield and retunable** — it was authored from the product
  brief, not from an existing corporate identity. It is binding until the user
  changes it, but it is not sacred. The logo is the one part explicitly pinned:
  mark and wordmark ship unaltered.

## Evidence on Hand

**Exists and usable as real product imagery:**

- App screenshots at `.claude/skills/glide-design-system/assets/shots/` —
  `ios.png`, `ios-today.png`, `ios-full.png`, `mac.png`, `mac-full.png`. The two
  the site actually ships are vendored to `src/assets/shots/` so the page does
  not depend on tooling paths at runtime.
- Logo assets at `.claude/skills/glide-design-system/assets/`.
- Full brand deck at `.claude/reference/Glide Brand Deck.html`.
- Interactive iOS and macOS UI-kit screen recreations in the design-system
  skill's `ui_kits/`, available as a source of accurate in-product visuals.

**Does not exist — must never be fabricated:**

- App Store or TestFlight links, or any downloadable build.
- Pricing, plans, or a free tier.
- Testimonials, quotes, reviews, star ratings, user or download counts.
- Named schools, press mentions, awards, funding, or team bios.
- A launch date.

## Product Principles

1. **Calm is the product, not the styling.** Every web decision is judged by
   whether it lowers the visitor's heart rate. Urgency devices — countdowns,
   pressure copy, aggressive scroll-jacking — contradict the thing being sold.
2. **Show the feeling, not the feature grid.** A student is choosing a mood to
   study in. Lead with what Glide feels like to use; features are evidence for
   that claim, not the claim.
3. **Never shame, on any surface.** No "stop procrastinating," no guilt framing,
   no productivity moralizing. The site talks to a student the way the app
   would after a missed day.
4. **Say only what is true.** Pre-launch means no store badges, no invented
   numbers, no borrowed credibility. Honesty about being early is more
   persuasive to this audience than manufactured proof.
5. **Phone-first, unhurried.** The primary visitor is on a small screen with
   little patience. Fast, light, and legible in one hand — with room to breathe,
   not density.

## Accessibility & Inclusion

- A visible focus ring is non-negotiable (`--ring`, 3px soft glide halo) — the
  design system states this explicitly and it carries to the web.
- Low saturation and warm near-black text (`--ink-900`, never pure `#000`) must
  still meet contrast requirements; calm is not an excuse for pale text.
- Motion is gentle by default (140–380ms, no snapping), and must respect
  `prefers-reduced-motion` — the celebratory spring especially.
- The audience includes students who find conventional productivity tools
  cognitively punishing; reducing load is an inclusion requirement here, not a
  preference.
