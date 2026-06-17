# Codezen Branding Guide — "Prism"

## About

Codezen is a cybersecurity firm specializing in blockchain and Web3 technologies. We provide tailored security solutions designed to meet the distinct challenges of decentralized systems.

**Mission:** Protect the future of decentralized finance, applications, and networks through thorough audits and expert consulting services.

---

## Tagline

> Securing the Future of Blockchain & Web3

---

## Visual language

**Overall feel:** engineered, precise, atmospheric. The system is called **Prism** — a dark, crystalline expression of the brand's imagery direction (translucent glass forms, iridescent blues). Near-black tinted toward the mark's indigo, frosted-glass surfaces, soft rounded geometry, an iridescent cyan accent, and a monospace technical layer.

- **Dark-first.** Page base is `--cz-base` (`#0A0B12`) — a near-black with a faint indigo tint — rendered with `--field-bg`, a radial atmosphere that pools cyan, indigo, and navy glows across the surface. Solid raised surfaces use `--cz-night` (`#11131D`).
- **Glass.** Cards, panels, buttons, and the hero surface are frosted glass: `rgba(255,255,255,0.04–0.09)` fill, 1px white hairline border, `backdrop-filter: blur(12px)`. This is the default surface — not opaque fills.
- **Iridescent accent.** The hero accent is Cyan `#04D9FF`, evolved into `--iris` (cyan → `#2EE2FF` → `#168CCD` → cool white) for display words, stat numbers, and hairline rules.
- **Glow over shadow.** Depth comes from `--glow-cyan` (diffuse, soft), not drop shadows or hard rings. Interactive elements gain a cyan glow and border on hover.
- **Shape — soft.** No hard corners. `--radius-sm` 10px (fields), `--radius-md` 16px (buttons, cards), `--radius-lg` 24px (panels, modal).
- **Motion — calm.** `0.25–0.4s ease`. Buttons carry an arrow that glides on hover. Eyebrow dots pulse with a cyan glow. No bounces, no parallax.
- **Layout.** Centered `1240px` container, `32px` gutters, `72px` section rhythm. Section heads are left-aligned with a mono eyebrow; content grids are 3-up (services, work) or 4-up (process, stats).

---

## Color

All tokens are defined in [`brand.css`](./brand.css). Reference that file — values here are the canonical source.

### Logo colors
These three blues live in the logo mark. Use them for atmospheric glow and the iridescent gradient; **never** as flat UI fills.

| Token | HEX | Usage |
|---|---|---|
| `--cz-logo-dark-blue` | `#312e81` | Dominant — indigo atmospheric glow |
| `--cz-logo-navy` | `#0760ab` | Secondary |
| `--cz-logo-light-blue` | `#168ccd` | Accent, iridescent partner |

### Accent
| Token | HEX | Usage |
|---|---|---|
| `--cz-cyan` | `#04d9ff` | Hero interactive accent |
| `--cz-cyan-bright` | `#2ee2ff` | Hover / highlight |
| `--cz-cyan-soft` | `#5be4ff` | Mono labels, small accents on dark |
| `--cz-cyan-ink` | `#008dd3` | Accent on light backgrounds |

### Base surfaces
| Token | HEX | Usage |
|---|---|---|
| `--cz-base` | `#0a0b12` | Page base (use via `--field-bg`) |
| `--cz-night` | `#11131d` | Solid raised surface |
| `--cz-white` | `#ffffff` | Light surfaces, reversed text |

### Semantic aliases (dark theme default)
| Token | Value | Usage |
|---|---|---|
| `--surface-base` | `--cz-base` | Page wrapper |
| `--surface-raised` | `rgba(255,255,255,0.04)` | Cards, panels (glass) |
| `--surface-solid` | `--cz-night` | Opaque raised elements |
| `--text-strong` | `#f4f7ff` | Headings, primary text |
| `--text-body` | `rgba(232,238,255,0.66)` | Body copy |
| `--text-muted` | `rgba(232,238,255,0.40)` | Labels, captions |
| `--accent` | `--cz-cyan` | Interactive, highlights |
| `--border-default` | `rgba(255,255,255,0.10)` | Card borders |

Light mode overrides are available via `.light-mode` / `[data-theme="light"]`.

### Status colors
| Token | HEX |
|---|---|
| `--status-success` | `#2fd48a` |
| `--status-warning` | `#f5b945` |
| `--status-danger` | `#ff5c5c` |
| `--status-info` | `--cz-cyan` |

---

## Typography

Three font families. Felix Titling is strictly logo-only.

| Font | Token | Role | Weights |
|---|---|---|---|
| **Outfit** | `--font-body` | All UI text — display, headings, body | 300 / 400 / 500 / 600 / 700 / 800 |
| **JetBrains Mono** | `--font-mono` | Technical layer — eyebrows, kickers, audit IDs, metadata, status chips | 400 / 500 / 600 |
| **Felix Titling** | `--font-logo` | Logo wordmark **only** — never body or UI text | 400 |

Font files are in `fonts/`.

### Type scale

| Token | Size | Usage |
|---|---|---|
| `--fs-display` | 72px | Hero headline |
| `--fs-stat` | 52px | Iridescent metric numbers |
| `--fs-h1` | 56px | |
| `--fs-h2` | 40px | Section heading |
| `--fs-h3` | 24px | Card title |
| `--fs-h4` | 20px | |
| `--fs-body-lg` | 19px | Primary paragraph |
| `--fs-body` | 16px | Default body |
| `--fs-mono` | 12px | Eyebrows / kickers (mono) |
| `--fs-mono-sm` | 11px | Dense metadata (mono) |

Display text uses `--ls-display: -0.03em` (tight tracking). Mono labels use `--ls-mono: 0.14em` or `--ls-mono-wide: 0.22em` (wide tracking, uppercase).

### Fallback stacks
```css
font-family: var(--font-body); /* "Outfit", Arial, sans-serif */
font-family: var(--font-mono); /* "JetBrains Mono", ui-monospace, "SF Mono", Menlo, monospace */
```

---

## Logo

### Variants (`logos/svg/`)

| File | Use when |
|---|---|
| `full-color.svg` | Default — on white or very light backgrounds |
| `full-color-white-bg.svg` | Same, with white bounding box included |
| `white.svg` | On dark or photo backgrounds |
| `white-blue-bg.svg` | White logo on brand blue |
| `white-transparencies.svg` | On photos or textured backgrounds |
| `white-transparencies-blue-bg.svg` | On brand blue with added depth |
| `isologo-white-bg.svg` | Mark only — light backgrounds |
| `isologo-blue-bg.svg` | Mark only — dark or blue backgrounds |

PNG and PDF versions follow the same naming convention in `logos/png/` and `logos/pdf/`.

### Clear space

Maintain a clear space around the logo equal to the height and width of the "C" in CODEZEN. No text, graphics, or other elements may enter this zone.

### Do's
- Always use the official logo files from this repository
- Resize proportionally — never stretch or distort
- Use full-color on solid, contrasting light backgrounds
- Use white (or white-transparencies) versions on photos, patterns, and dark backgrounds
- Use the isologo mark on profile images and app icons

### Don'ts
- Do not alter the logo colors
- Do not rotate, skew, or apply effects (shadows, glows, outlines)
- Do not rearrange mark and wordmark
- Do not place the full-color logo on dark or busy backgrounds
- Do not use Felix Titling anywhere outside the logo itself

---

## Icons

### Service icons (`icons/`)
Five bespoke cyan line-art SVGs. Cyan `#04D9FF` strokes with faint translucent-white fills, drawn for dark backgrounds.

| File | Service |
|---|---|
| `smart-contract-audits.svg` | Smart Contract Audits |
| `blockchain-consulting.svg` | Blockchain Consulting |
| `disaster-recovery.svg` | Disaster Recovery |
| `discovery.svg` | Discovery |
| `support.svg` | Support |

**Always place on a dark container** (`--cz-night` or `--cz-logo-dark-blue`) with ~20% padding. On light backgrounds they lose definition.

Social/UI icons (`linkedin.svg`, `twitter.svg`) are also in `icons/` — thin-stroke line art.

### Chain marks (`icons/chains/`)
Ecosystem marks for bitcoin, ethereum, cosmos, solana, polkadot. Monochrome SVGs. On dark surfaces render white via `filter: brightness(0) invert(1)`.

**No icon fonts. No emoji.** If you need an icon not in `assets/`, use a thin-stroke open-source set (Lucide / Feather at 1.5px stroke) and flag the substitution.

---

## Spacing & layout

| Token | Value | Usage |
|---|---|---|
| `--section-y` | 72px | Vertical section rhythm |
| `--container-max` | 1240px | Max content width |
| `--container-pad` | 32px | Horizontal gutters |

4px base spacing scale: `--space-1` (4px) → `--space-24` (96px). See `brand.css` for the full scale.

---

## Shape

| Token | Value | Usage |
|---|---|---|
| `--radius-sm` | 10px | Fields, small chips |
| `--radius-md` | 16px | Buttons, cards, tiles |
| `--radius-lg` | 24px | Panels, hero visual, modal |
| `--radius-pill` | 999px | Badges, status dots, toggles |

No hard corners. The brand reads calm and precise.

---

## Motion

| Token | Value |
|---|---|
| `--dur-fast` | 0.25s |
| `--dur` | 0.40s |
| `--dur-slow` | 0.60s |
| `--ease` | cubic-bezier(0.22, 0.61, 0.36, 1) |
| `--ease-out` | cubic-bezier(0.16, 1, 0.30, 1) |

Transitions cover color, border, glow, and transform. Press = 1px nudge. Eyebrow dot pulses. Respect `prefers-reduced-motion`.

---

## Imagery

- **Background:** `--field-bg` atmosphere (near-black with radial cyan/indigo/navy glows) + fine SVG grain overlay (`mix-blend: overlay`)
- **Subject:** Translucent glass/crystalline geometric forms — prisms, cubes, polyhedra — catching cool iridescent blue/white light
- **Mood:** Precise, architectural, atmospheric — not warm, organic, or illustrative
- **Avoid:** Stock photography of people, warm/orange tones, "hacker in a hoodie" clichés

---

## Voice & copy

- **Tone:** Confident, precise, technical-but-plain. Authority without hype.
- **Person:** "We" for Codezen; "your" for the client's systems. Rarely "I".
- **Casing:** Title Case for headings and section labels. Sentence case for body. Buttons: sentence-style imperatives (*"Secure your project"*, *"Let's get an audit"*).
- **Rhythm:** Eyebrow → Heading → Body. Eyebrow is a short mono label ("Our Work"); heading is a full value statement.
- **No emoji.** No exclamation-heavy copy.

---

## Social media

| Platform | File |
|---|---|
| LinkedIn | `social-media/linkedin-header.png` |
| Facebook | `social-media/facebook-header.png` |
| X | `social-media/x-header.png` |

Profile image: isologo on blue background (`logos/png/isologo-blue-bg.png` or the SVG equivalent).

---

## Developer reference

All tokens and `@font-face` declarations in one file: [`brand.css`](./brand.css)

```css
/* In your HTML */
<link rel="stylesheet" href="brand.css">

/* Then use tokens */
background: var(--field-bg);
color: var(--text-strong);
font-family: var(--font-body);
accent: var(--cz-cyan);
```

---

## Contact

For press and brand inquiries: [info@codezen.tech](mailto:info@codezen.tech)
Website: [codezen.tech](https://codezen.tech)
