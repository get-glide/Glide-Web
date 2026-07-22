---
name: Glide Web
description: Cut-paper sticker desk built on the Glide design system, spending all four accent families at once.
colors:
  paper: "#fbf9f4"
  paper-white: "#ffffff"
  paper-sunken: "#f5f1e9"
  paper-edge: "#ece6da"
  paper-rule: "#ded6c6"
  ink: "#292933"
  ink-body: "#45454f"
  ink-quiet: "#6c6c78"
  glide-wash: "#e6eafd"
  glide-tint: "#cdd5fb"
  glide-soft: "#aab6f7"
  glide: "#6c7bf0"
  glide-deep: "#5462df"
  glide-press: "#4450c2"
  sage-wash: "#dcefe6"
  sage-fill: "#a5d6c1"
  sage: "#5fae92"
  sage-deep: "#3c7d66"
  sage-ink: "#123f31"
  apricot-wash: "#fbe6d8"
  apricot-fill: "#f6c3a1"
  apricot: "#ee9a6b"
  apricot-deep: "#bd6537"
  apricot-ink: "#5c3316"
  lilac-wash: "#ede4f8"
  lilac-fill: "#cdb6ec"
  lilac: "#a888dd"
  lilac-ink: "#3d2358"
  coral-deep: "#b0483b"
typography:
  display:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: "clamp(46px, 6.6vw, 98px)"
    fontWeight: 800
    lineHeight: 0.93
    letterSpacing: "-0.045em"
  headline:
    fontFamily: "Bricolage Grotesque, sans-serif"
    fontSize: "26px"
    fontWeight: 800
    lineHeight: 1.1
    letterSpacing: "-0.035em"
  body:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "clamp(16.5px, 1.2vw, 19px)"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: "normal"
  label-sm:
    fontFamily: "Hanken Grotesk, system-ui, sans-serif"
    fontSize: "12px"
    fontWeight: 700
    lineHeight: 1.4
    letterSpacing: "0.06em"
  meter:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: "26px"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: "-0.02em"
  meter-sm:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: "21px"
    fontWeight: 500
    lineHeight: 1
    letterSpacing: "-0.02em"
rounded:
  inline: "8px"
  card: "20px"
  slab: "28px"
  pill: "999px"
  mark: "25%"
components:
  button-primary:
    backgroundColor: "{colors.glide-deep}"
    textColor: "{colors.paper-white}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "15px 30px"
    height: "56px"
  button-primary-hover:
    backgroundColor: "{colors.glide}"
  button-dark:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    padding: "0 24px"
    height: "46px"
  input-email:
    backgroundColor: "{colors.paper-white}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "15px 22px"
    height: "56px"
  sticker-sage:
    backgroundColor: "{colors.sage-fill}"
    textColor: "{colors.sage-ink}"
    rounded: "{rounded.card}"
    padding: "14px 20px"
  sticker-apricot:
    backgroundColor: "{colors.apricot-fill}"
    textColor: "{colors.apricot-ink}"
    rounded: "{rounded.pill}"
    padding: "11px 18px"
  sticker-lilac:
    backgroundColor: "{colors.lilac-fill}"
    textColor: "{colors.lilac-ink}"
    rounded: "{rounded.pill}"
    padding: "11px 18px"
---

# Design System: Glide Web

## Overview

**Creative North Star: "The Sticker Desk"**

Glide's web surface is a student's desk seen from directly above: warm dotted
stock, shapes cut from coloured paper and laid down flat, and the product
itself pinned on top as physical stickers with hard, unblurred shadows. Nothing
glows, nothing floats on a soft cloud, nothing fades into a gradient. Every
element has an edge you could run a thumbnail along.

The Glide design system ships four accent families. Earlier iterations of this
site spent one at a time and read as either timid or corporate. This world
spends all four at once, as flat fields rather than accents on a neutral
ground. Colour is the composition, not the trim. That is what separates this
surface from the app it markets: the iOS and macOS products are calm and
restrained by design, while the web has one job, which is to make a student
stop scrolling.

The visual anti-references are confirmed and specific: the pale minimal
calm-app landing page (soft pastel, one floating rounded screenshot, drop
shadow, App Store badge), and the saturated dark hero that preceded this one.
Both were built and both were rejected.

**Key Characteristics:**

- Flat cut-paper colour fields, hard edges, zero gradients
- Hard offset shadows with no blur radius
- All four accent families present on one screen
- Product elements read as physical stickers, rotated off-axis
- Chunky display type with words colour-blocked and one highlighter swipe
- Warm paper stock with a faint notebook dot grid

## Colors

A warm neutral stock carrying four saturated accent families as flat fills,
each with a dedicated dark ink for text placed on it.

### Primary

- **Glide Periwinkle** (`{colors.glide}`): the brand primary, inherited from the
  logo mark and unchanged. Appears as the plane's dotted flight trail, the
  emphasised word in the headline, and the window's offset shadow. The deeper
  step carries the primary button so white label text clears AA.

### Secondary

- **Sage Fill** (`{colors.sage-fill}`): the focus-session colour. Backs the
  highlighter swipe under the headline and the timer sticker. Its role in the
  app is success and focus, and it keeps that meaning here.
- **Apricot Fill** (`{colors.apricot-fill}`): warmth and streaks. Backs the
  status tag and the streak sticker.
- **Lilac Fill** (`{colors.lilac-fill}`): the gentle tertiary. Backs the decks
  sticker and the inline emphasis chip in body copy.

### Tertiary

- **Coral Deep** (`{colors.coral-deep}`): the only error colour. Reserved for
  form validation messages, never decorative.

### Neutral

- **Warm Paper** (`{colors.paper}`): the page stock. Never pure white.
- **Card White** (`{colors.paper-white}`): input fields and the app window
  interior only.
- **Paper Rule** (`{colors.paper-rule}`): the notebook dot grid and resting
  input shadows.
- **Soft Ink** (`{colors.ink}`): all primary text and every sticker outline.
  Never pure black.
- **Body Ink** (`{colors.ink-body}`) and **Quiet Ink** (`{colors.ink-quiet}`):
  supporting copy and fine print.

### Named Rules

**The Four Families Rule.** Periwinkle, sage, apricot and lilac must all be
visible in any full viewport. Dropping to one accent returns the surface to the
timid version this world replaced.

**The Ink Pairing Rule.** Every accent fill has one matching dark ink for text
placed on it: sage takes `{colors.sage-ink}`, apricot takes
`{colors.apricot-ink}`, lilac takes `{colors.lilac-ink}`. Never put body ink or
white on an accent fill; the pairings are chosen to clear 4.5:1 and the
alternatives do not.

**The Flat Fill Rule.** Colour is applied as a solid fill. No gradients, no
mesh, no tinted glass, anywhere on the surface.

## Typography

**Display Font:** Bricolage Grotesque (variable, self-hosted)
**Body Font:** Hanken Grotesk (variable, self-hosted)
**Label/Mono Font:** JetBrains Mono (500 only, self-hosted)

**Character:** Bricolage is the face already set in the Glide wordmark, so the
logo and the headline are the same voice rather than a lockup sitting next to
unrelated type. At heavy weight and tight tracking it reads chunky and drawn
rather than corporate. Hanken carries everything readable; JetBrains appears
only where a number is being measured.

### Hierarchy

- **Display** (800, `clamp(46px, 6.6vw, 98px)`, 0.93): the single hero headline.
  One per page.
- **Headline** (800, 26px, -0.035em): the wordmark and any section head.
- **Body** (400, `clamp(16.5px, 1.2vw, 19px)`, 1.6): supporting copy, held to
  roughly 42ch.
- **Label** (700, 15px): sticker text, nav links, button labels, the status tag.
- **Label Small** (700, 12px, 0.06em, uppercase): the one micro-label on the
  surface, sitting under the timer. The only uppercase text in the system.
- **Meter** (JetBrains Mono 500, 26px): timers, counters, durations only.
- **Meter Small** (JetBrains Mono 500, 21px): the meter's step below 620px.

### Named Rules

**The Same-Family Emphasis Rule.** Emphasis inside a headline comes from
colour-blocking a word in `{colors.glide-deep}` or backing it with a
highlighter swipe. Never switch typeface mid-headline.

**The Measurement-Only Mono Rule.** JetBrains Mono appears only on a value
being measured, such as `25:00`. It is never a costume for "technical".

**The Sentence Case Rule.** Sentence case everywhere, including buttons and
headings, per the brand voice. The only uppercase is the tiny sticker label
under the timer.

## Layout

A two-column hero grid at `1.04fr / 0.96fr` inside a `1480px` max-width
container, with copy left and the product right. Below `1080px` it collapses to
a single column, copy first. Section padding is fluid via `clamp()` rather than
a fixed step scale.

Decorative cut-paper shapes are positioned absolutely and bleed off every edge
of the viewport; they are never contained. Two of the four are hidden below
`1080px` so the composition thins rather than crowds.

Full-height surfaces use `100dvh` with a `100vh` fallback. Horizontal overflow
is hidden at the page root so bleeding shapes and off-axis stickers can cross
the boundary without producing a scrollbar.

## Elevation & Depth

This system is **flat with hard offset shadows**. There is no blur anywhere.
Depth is communicated the way a sticker on a desk communicates it: a solid
colour shape offset down and to the right, as if lit by a single hard source.
Elevation is literal, not atmospheric.

### Shadow Vocabulary

- **Press shadow** (`box-shadow: 0 4px 0 <colour>`): buttons and inputs at rest.
  The button's shadow is ink; the input's is paper rule; the nav button's is
  periwinkle.
- **Sticker shadow** (`box-shadow: 6px 7px 0 <ink>`): every pinned sticker.
- **Window shadow** (`box-shadow: 14px 16px 0 <glide-soft>`): the app window
  only, in periwinkle rather than ink so it reads as the largest object.
- **Tag shadow** (`box-shadow: 0 3px 0 <apricot>`): the status tag, tinted to
  its own family.

### Named Rules

**The No-Blur Rule.** Every shadow has a zero blur radius. A blurred shadow
anywhere on this surface is a defect.

**The Press-Depresses Rule.** Interactive elements sit on their shadow at rest,
lift on hover (shadow grows), and depress on `:active` (element translates
down, shadow shrinks to `0 1px 0`). The total height stays constant so nothing
reflows.

## Shapes

Four radii, applied by role and never mixed arbitrarily: inline (`8px`) for
marks set behind text, card (`20px`) for the timer sticker and focus targets,
slab (`28px`) for the app window frame and large cut-paper rectangles, and pill
(`999px`) for anything interactive or sticker-shaped. Generous rounding is a
Glide brand signal inherited from the mark's rounded tile.

The logo tile is the one exception and carries its own radius token (`25%`),
because the mark's geometry is proportional: `rx 30` on a `120` viewBox. Stated
as a percentage it stays correct at any rendered size and never needs a
per-instance pixel value.

### Named Rules

**The Mark-Is-Exempt Rule.** The logo tile's corner radius derives from the
asset, not the UI scale. Use `{rounded.mark}` on any instance of the mark and
never snap it to a pixel step.

Stickers and the app window are rotated off-axis between 2° and 9°. Rotation is
what makes them read as placed objects rather than laid-out boxes. Nothing
decorative sits at exactly 0°.

Outlines are heavy and dark: `2.5px` on form controls, `3px` on stickers and the
app window, always in `{colors.ink}`. Hairlines do not belong in this world.

## Components

### Buttons

- **Shape:** fully rounded pill (`{rounded.pill}`)
- **Primary:** deep periwinkle fill, white label in Bricolage 800, `2.5px` ink
  outline, sitting on a `0 4px 0` ink shadow. 56px tall.
- **Hover / Focus:** lifts 2px, shadow grows to `0 6px 0`. Focus shows a `3px`
  periwinkle outline offset 3px.
- **Active:** translates down 3px, shadow collapses to `0 1px 0`.
- **Dark variant:** ink fill with paper label on a periwinkle shadow, used for
  the nav action so it does not compete with the hero's primary button.

### Chips and Stickers

- **Style:** flat accent fill, matching dark ink text, `3px` ink outline, hard
  `6px 7px 0` ink shadow, rotated 3° to 9°.
- **Use:** stickers carry real product facts (a session length, a streak, a deck
  count). They are not decorative labels.

### Inputs / Fields

- **Style:** white fill, `2.5px` ink outline, pill radius, resting on a paper
  rule shadow. 56px tall to match the button.
- **Focus:** outline stays, shadow switches to periwinkle. No glow.
- **Error:** outline and shadow switch to the apricot family; the message below
  is coral. Cleared as soon as the field is edited.
- **Disabled:** 55% opacity, shadow retained.

### Navigation

Paper strip, no background fill, no border. Links are pill-shaped hover targets
that fill with paper edge and lift 2px. Below `940px` the links wrap to their
own row beneath the wordmark and action; nothing is hidden behind a menu.

### The App Window

The signature component. A real product screenshot inside a `3px` ink frame with
slab radius, rotated ~2.4°, sitting on a periwinkle offset shadow, with stickers
pinned around and overlapping its edges. Art-directed per breakpoint: the macOS
capture on desktop, the iOS capture below `620px`, swapped via `<picture>`.

## Do's and Don'ts

### Do:

- **Do** keep all four accent families visible in any full viewport.
- **Do** pair each accent fill with its designated dark ink
  (`{colors.sage-ink}`, `{colors.apricot-ink}`, `{colors.lilac-ink}`).
- **Do** give every shadow a zero blur radius and a visible offset.
- **Do** rotate stickers and product frames off-axis between 2° and 9°.
- **Do** let cut-paper shapes bleed off the viewport edge.
- **Do** use real product screenshots, art-directed per breakpoint.
- **Do** keep the timer in JetBrains Mono and everything else out of it.
- **Do** write in sentence case, including buttons and headings.

### Don't:

- **Don't** use a gradient. Not on backgrounds, not on text, not on fills.
- **Don't** blur a shadow, or add a coloured glow.
- **Don't** reduce the palette to a single accent on a neutral ground.
- **Don't** switch typeface to emphasise a word inside a headline.
- **Don't** use bounce or elastic easing on chrome. Spring is reserved for
  celebratory product moments, per the Glide motion rule.
- **Don't** use an em-dash in any user-visible string.
- **Don't** put white or body ink on an accent fill.
- **Don't** alter the logo mark or wordmark in any way.
