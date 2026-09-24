# Invoicerr design system

Every value on this page was read out of a file in the product, and each one says which file. Nothing
here was chosen for this document. If a value disagrees with the code, the code wins and this page is
the bug.

The identity is named **Lagune** (decision of 2026-09-15). The source of truth is
[`frontend/src/index.css`](https://github.com/invoicerr-app/invoicerr/blob/main/frontend/src/index.css)
in the product repository. The landing site
([`landing/src/index.css`](https://github.com/invoicerr-app/landing/blob/main/src/index.css)) carries a
copy of the subset it uses and says so in its own header comment.

## How colours are written

The product declares every colour in OKLCH, not hex. The hex column below is the sRGB rendering of
that OKLCH triplet, computed (OKLCH to linear sRGB to sRGB, D65), not sampled from a screenshot. Two
values confirm the conversion: `frontend/index.html` states in a comment that
`oklch(0.975 0.005 230)` is `#f3f7f9` and `oklch(0.175 0.014 230)` is `#0a1215`, and the computation
returns exactly those.

`*` marks a colour whose OKLCH value sits outside the sRGB gamut; the hex is the clipped rendering a
browser will show.

## Palette

Hue `230` runs through almost the whole palette. That is the identity: a single azure hue, varied by
lightness and chroma, with three semantic tones sitting off it.

### Surfaces and text

| Token | Light OKLCH | Light hex | Dark OKLCH | Dark hex | Role |
| --- | --- | --- | --- | --- | --- |
| `--background` | `0.975 0.005 230` | `#f3f7f9` | `0.175 0.014 230` | `#0a1215` | The page itself. Also the two `theme-color` meta values. |
| `--foreground` | `0.200 0.030 230` | `#061821` | `0.950 0.006 230` | `#ebeff2` | Body text. Never pure black, never pure white. |
| `--card` | `0.995 0.003 230` | `#fbfeff` | `0.225 0.016 230` | `#141d22` | A raised panel, one step off the background. |
| `--popover` | `0.995 0.003 230` | `#fbfeff` | `0.225 0.016 230` | `#141d22` | Menus and dialogs. Same pair as card. |
| `--muted` | `0.940 0.008 230` | `#e6ecef` | `0.270 0.014 230` | `#20282c` | A quiet fill. |
| `--muted-foreground` | `0.470 0.020 230` | `#505d64` | `0.680 0.020 230` | `#8c9ba2` | Secondary text. |
| `--border` | `0.890 0.010 230` | `#d4dce0` | `1 0 0 / 10%` | white at 10% | Every hairline. Dark mode uses translucent white rather than a fixed grey. |
| `--input` | `0.890 0.010 230` | `#d4dce0` | `1 0 0 / 14%` | white at 14% | Field outlines. |
| `--overlay` | `0 0 0 / 50%` | black at 50% | same | same | The scrim behind a modal. Deliberately identical in both themes. |

### Brand and interaction

| Token | Light OKLCH | Light hex | Dark OKLCH | Dark hex | Role |
| --- | --- | --- | --- | --- | --- |
| `--primary` | `0.640 0.130 230` | `#0099cb` * | `0.760 0.136 230` | `#39c0f6` | The brand azure. Primary buttons, links, the lifted half of the mark. |
| `--primary-foreground` | `0.180 0.028 230` | `#04141c` | `0.160 0.024 230` | `#030f16` | Ink on a primary fill. Dark in both themes, because primary is light in both. |
| `--secondary` | `0.940 0.012 230` | `#e3edf2` | `0.270 0.018 230` | `#1d282e` | Secondary button fill. |
| `--accent` | `0.910 0.030 230` | `#cee6f2` | `0.320 0.045 230` | `#183745` | Hover and selected states. |
| `--ring` | `0.760 0.121 230` | `#50bfef` | `0.760 0.114 230` | `#59beeb` | The focus ring. |

### Semantic tones

Each is a soft fill paired with saturated text on it, so a badge only ever needs
`bg-<tone> text-<tone>-foreground`. `index.css` records that the pairs were checked at 9.3:1 or better
fill-to-text and 10.6:1 or better text-on-card, in both themes.

| Token | Light OKLCH | Light hex | Dark OKLCH | Dark hex |
| --- | --- | --- | --- | --- |
| `--success` | `0.920 0.060 145` | `#cdf0cd` | `0.280 0.060 145` | `#133015` |
| `--success-foreground` | `0.300 0.110 145` | `#003b00` * | `0.850 0.130 145` | `#96e498` |
| `--warning` | `0.920 0.070 70` | `#ffddb2` * | `0.280 0.070 55` | `#421d00` * |
| `--warning-foreground` | `0.320 0.130 55` | `#601400` * | `0.850 0.140 80` | `#fdc357` |
| `--info` | `0.920 0.045 210` | `#c3edf5` | `0.280 0.050 225` | `#042e3b` |
| `--info-foreground` | `0.300 0.080 225` | `#00354c` * | `0.850 0.090 210` | `#83deee` |
| `--destructive` | `0.570 0.220 24` | `#db192f` | `0.680 0.200 24` | `#fc5858` |
| `--destructive-foreground` | `0.990 0.010 24` | near-white | `0.160 0.030 24` | near-black |
| `--destructive-soft` | `0.930 0.060 24` | | `0.280 0.070 24` | |
| `--destructive-soft-foreground` | `0.350 0.160 24` | | `0.850 0.130 24` | |

Two rules the file states outright and that are easy to break:

- **Green is reserved for `--success`.** Never introduce a second green anywhere in the product.
- **`--destructive-foreground` flips** between themes, because `--destructive` itself lightens in dark
  mode. `--destructive-solid-foreground` stays the same near-white in both, on purpose, and must not
  get a `.dark` override: it is used on a destructive surface composited at 60% opacity, where dark
  ink measures 2.9 to 3.1:1 and fails AA while light text keeps 6.1 to 6.5:1.

### Charts

Five steps, all on hue 230 except the neutral fifth, so a chart reads as one family.

| Token | Light | Dark |
| --- | --- | --- |
| `--chart-1` | `#0099cb` * | `#39c0f6` |
| `--chart-2` | `#369bc5` | `#2f8bb1` |
| `--chart-3` | `#124053` | `#97d8f8` |
| `--chart-4` | `#5ac5f5` | `#1d5d77` |
| `--chart-5` | `#66747b` | `#8c9ba2` |

### Sidebar

The sidebar has its own surface pair; the rest of its tokens repeat the values above.

| Token | Light | Dark |
| --- | --- | --- |
| `--sidebar` | `oklch(0.965 0.006 230)` / `#f0f4f7` | `oklch(0.200 0.016 230)` / `#0e171c` |
| `--sidebar-foreground` | same as `--foreground` | same as `--foreground` |
| `--sidebar-primary` | same as `--primary` | same as `--primary` |
| `--sidebar-accent` | same as `--accent` | same as `--accent` |

`index.css` also carries a second `:root` / `.dark` pair for the sidebar inside `@layer base`. It is
dead weight and says so: Tailwind v4 resolves unlayered rules before layered ones regardless of source
order, so the unlayered block above always wins. Do not read those lines as a second source of truth.

## The logo's own colours

The SVG files in this repository do **not** use CSS variables; a favicon is fetched by the browser
outside any DOM and could not read them. They carry two literal values:

| Value | Where | Relation to the palette |
| --- | --- | --- |
| `#0f1f2a` | the mark and wordmark ink, every `logo/*.svg` | `oklch(0.231 0.030 239.9)`. A fixed brand ink, close to but **not equal to** `--foreground` light (`#061821`). Keep it exact, do not substitute the token. |
| `#0099cb` | the lifted half in `lockup.svg` and `mark-duo.svg`, the tile in `app-icon.svg` | Exactly `--primary` light, `oklch(0.640 0.130 230)`, clipped into sRGB. |
| `#ffffff` | `lockup-white.svg`, `mark-white.svg`, `wordmark-white.svg` | Pure white, for a dark or photographic ground. Note this is the one place the identity allows pure white. |
| `#ebeff2` | `favicon/favicon.svg`, dark-scheme branch only | `--foreground` dark. The favicon themes itself with an embedded `prefers-color-scheme` rule instead of going white. |

The in-app React component (`landing/src/components/brand-mark.tsx`) takes a third route: it paints the
mark in `currentColor` and the lifted half in `fill-primary`, so the mark inherits the surrounding text
colour and the azure follows the theme.

## Typefaces

Three families, all self-hosted through Fontsource. `index.css` states the reason: the PWA has to work
offline and no font request may leak to a third party. There is no Google Fonts call at runtime.

| Family | Package | Weights shipped | Used for |
| --- | --- | --- | --- |
| **Inter Variable** | `@fontsource-variable/inter` ^5.3.0 | the whole variable axis, one file | `--font-sans`. Body and all interface text (`body { font-sans }`). |
| **Space Grotesk Variable** | `@fontsource-variable/space-grotesk` ^5.3.0 | the whole variable axis, one file | `--font-heading`. `h1`, `h2`, `h3`, `h4`, applied in `@layer base`. |
| **Space Mono** | `@fontsource/space-mono` ^5.3.0 | static `400` and `700` only | `--font-mono`. Figures and codes. |

Fallback stacks, verbatim from `index.css` lines 22 to 24:

```css
--font-sans:    'Inter Variable', ui-sans-serif, system-ui, sans-serif;
--font-heading: 'Space Grotesk Variable', ui-sans-serif, system-ui, sans-serif;
--font-mono:    'Space Mono', ui-monospace, 'SFMono-Regular', monospace;
```

No italic of Space Mono is imported, because the product uses that face only for numbers and codes.

Monetary and numeric cells use a custom utility rather than Tailwind's `tabular-nums`, because the
face has to change too (`index.css` line 293):

```css
@utility amount {
  font-family: var(--font-mono);
  font-variant-numeric: tabular-nums;
}
```

Heading sizes are deliberately **not** defined globally. They are set per component, and the code says
a full type-scale pass is still outstanding.

## Radii

One base value, three derived steps (`index.css` lines 18 to 21 and 104):

| Token | Value | Computed |
| --- | --- | --- |
| `--radius` | `0.625rem` | 10px |
| `--radius-sm` | `calc(var(--radius) - 4px)` | 6px |
| `--radius-md` | `calc(var(--radius) - 2px)` | 8px |
| `--radius-lg` | `var(--radius)` | 10px |
| `--radius-xl` | `calc(var(--radius) + 4px)` | 14px |

The logo has its own geometry and does not use these: the mark's rounded square is a 72-unit corner
radius on a 320-unit square (`M168 96H344A72 72 0 0 1 416 168...`), and the app-icon tile is
`rx="114.176"` on 512, the iOS squircle proportion.

## Spacing, shadows, motion

- **Spacing:** no override. Neither stylesheet redefines `--spacing`, so the product is on Tailwind's
  default 0.25rem scale.
- **Shadows:** no override. Grep for `--shadow` in either stylesheet returns nothing; the product uses
  Tailwind's stock `shadow-*` utilities.
- **Motion:** the landing's entrance animations are declared in CSS rather than driven by a library,
  because the page is prerendered to HTML at build time and a library would bake `style="opacity:0"`
  into the markup a crawler reads. The shared easing is
  `cubic-bezier(0.21, 0.47, 0.32, 0.98)`, with `enter` at 0.6s, `enter-stage` at 0.9s after a 0.35s
  delay, and `enter-pop` at 0.5s.
- **Reduced motion:** the app collapses every animation and transition to 0.01ms rather than removing
  it, so a spinner stays a visible static circle instead of vanishing.

## Two things that are not decoration

- `color-scheme: light` / `dark` is set on `:root` and `.dark`. Without it the browser draws native
  checkboxes, radios and selects in its own light chrome whatever our theme says. This was a real bug.
- The two `theme-color` meta tags are a pair scoped by `prefers-color-scheme`, because a web manifest's
  single `theme_color` cannot vary with the OS scheme.

## The phrases the product actually uses

Quoted, with their source. Do not paraphrase them into something new.

| Phrase | Where |
| --- | --- |
| "The invoicing app that keeps up with you." | `landing/src/components/sections/hero.tsx` line 48 |
| "Open-source invoicing, in the cloud or on your own server." | `landing/src/components/footer.tsx` line 54 |
| "Open-source invoicing for freelancers" | `documentation/docusaurus.config.ts` line 11, the Docusaurus `tagline` |
| "OPEN SOURCE · SELF-HOSTED" | the badge rendered in `social/og.jpg` and `social/banner.webp` |
