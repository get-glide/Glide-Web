# Glide-Web

Marketing website for Glide, a calm study app for iPhone and Mac. This repo is
the website only. The app itself lives elsewhere.

## Running it

Static HTML. No build step, no framework, no dependencies.

```bash
cd src && python3 -m http.server 8000
```

`src/index.html` is the whole site today: a hero section, and nothing below it
yet. Fonts are self-hosted in `src/assets/fonts/`; the page makes zero external
requests at runtime. Keep it that way.

## Which file wins

Three sources of truth, in this order for their own domain:

| Question | Authority |
|---|---|
| What is true about the product? | `PRODUCT.md` |
| How does the website look? | `DESIGN.md` (+ `.impeccable/design.json`) |
| What are the brand tokens, logo and voice? | `.claude/skills/glide-design-system/` |

The design system was authored for the **apps**, where calm restraint is the
point. It owns the palette, type families, logo and voice. It does **not** own
how this website looks. The web deploys those same tokens far more loudly, and
`DESIGN.md` is what governs that. If the two seem to disagree about expression,
`DESIGN.md` wins for this repo. If they disagree about brand, the design system
wins.

## Hard constraints

These are not style preferences. Breaking them ships something untrue.

- **Glide is not released.** No App Store badges, no download links, no
  pricing, no testimonials, no user or download counts, no launch date. The
  call to action collects interest and nothing more. See PRODUCT.md for the
  full list of what must never be fabricated.
- **The logo is pinned.** Mark and wordmark ship unaltered. Its corner radius
  is `25%` (the asset's own geometry), never a pixel value from the UI scale.
- **Voice is sentence case**, low-pressure, never shaming, no emoji in UI.
  Short headlines. This is product truth, not decoration.
- **No em-dashes in user-visible strings.** Use a comma, a period, or restructure.
- **No gradients and no blurred shadows** anywhere on the site. The visual world
  is flat cut paper with hard offset shadows. See DESIGN.md.

## Installed skills conflict. Read this before following one.

`.claude/skills/` and `.agents/skills/` carry a bundle of third-party design
skills (`design-taste-frontend`, `redesign-existing-projects`,
`high-end-visual-design`, `minimalist-ui`, `stitch-design-taste`, and others).
They are vendored for reproducibility, not because they are authoritative.

Several of them give advice that is **wrong for this project**:

- They discourage purple/periwinkle as an "AI tell". Glide's primary is
  periwinkle `#6c7bf0`, taken from the logo. Their own override applies.
- They cap you at one accent colour. This site deliberately uses four.
- They push Geist / Outfit / Satoshi. Display type is Bricolage Grotesque
  because that is the face set in the Glide wordmark.
- They discourage Lucide icons. The Glide design system specifies Lucide.
- `stitch-design-taste` generates its own `DESIGN.md` and will overwrite ours.

Their generic guidance (accessibility, real images over fake screenshot divs,
hero discipline, dead links, form states) is genuinely useful. Their aesthetic
prescriptions are not. When one conflicts with `DESIGN.md` or `PRODUCT.md`,
those win, and say so rather than silently splitting the difference.

## Checking your work

The impeccable design hook runs automatically on edits. To check by hand:

```bash
node .claude/skills/impeccable/scripts/detect.mjs --json src/index.html
```

`[]` means clean against `DESIGN.md`. Note this CLI does not read
`.impeccable/config.json`, so any configured ignores will still appear here;
the hook applies them.

Before calling UI work done, verify in a browser at desktop and 390px:
contrast (WCAG AA), touch targets at 44px or more, no horizontal overflow, and
`prefers-reduced-motion` honoured.

## Known gaps

Do not mistake these for finished work.

- The site is one hero. There is nothing below the fold.
- Nav links point at `#`. The sections do not exist.
- The waitlist form validates and shows a success state, but stores nothing.
  There is no backend.
- `origin/main` and `origin/production` trail `development`.
