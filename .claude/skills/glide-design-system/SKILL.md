---
name: glide-design
description: Use this skill to generate well-branded interfaces and assets for Glide, either for production or throwaway prototypes/mocks/etc. Contains essential design guidelines, colors, type, fonts, assets, and UI kit components for prototyping.
user-invocable: true
---

Read the README.md file within this skill, and explore the other available files.
If creating visual artifacts (slides, mocks, throwaway prototypes, etc), copy assets out and create static HTML files for the user to view. If working on production code, you can copy assets and read the rules here to become an expert in designing with this brand.
If the user invokes this skill without any other guidance, ask them what they want to build or design, ask some questions, and act as an expert designer who outputs HTML artifacts _or_ production code, depending on the need.

## Quick map
- `readme.md` — full design guide: voice/content, visual foundations, iconography, index.
- `styles.css` — link this one file to pull in every token + font. `@import` manifest.
- `tokens/` — colors, typography, spacing, effects, fonts, base reset (CSS custom properties).
- `components/` — React primitives (`core/`, `forms/`, `feedback/`, `study/`). Each has a `.prompt.md` with usage.
- `ui_kits/ios/`, `ui_kits/macos/` — full interactive screen recreations to copy from.
- `guidelines/` — foundation specimen cards.
- `assets/` — `logo-mark.svg`, `logo-wordmark.svg`.

## The one-paragraph brief
Glide is a calm, playful study app for high-school & college students (macOS + iOS). Warm paper background, soft periwinkle "Glide" primary (#6c7bf0), sage/apricot/lilac accents, generous rounding, soft diffuse shadows, gentle glide-y motion. Type: Bricolage Grotesque (display), Hanken Grotesk (body), JetBrains Mono (timers/stats). Icons: Lucide (rounded line). Voice: warm, encouraging, sentence-case, low-pressure, never shaming, no emoji in UI.
