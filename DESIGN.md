---
version: alpha
name: Lagune
description: >-
  The Invoicerr design system. Every token below is transcribed from
  invoicerr/frontend/src/index.css, which stays the source of truth; the prose under each
  section names the exact block a value came from. A token with no suffix is the light theme
  (:root); a token suffixed -dark is the dark theme (.dark). The format has no theme axis, so
  that suffix is this file's own convention and is not a name used in the code.
colors:
  background: "oklch(0.975 0.005 230)"
  foreground: "oklch(0.200 0.030 230)"
  card: "oklch(0.995 0.003 230)"
  card-foreground: "oklch(0.200 0.030 230)"
  popover: "oklch(0.995 0.003 230)"
  popover-foreground: "oklch(0.200 0.030 230)"
  primary: "oklch(0.640 0.130 230)"
  primary-foreground: "oklch(0.180 0.028 230)"
  secondary: "oklch(0.940 0.012 230)"
  secondary-foreground: "oklch(0.280 0.030 230)"
  muted: "oklch(0.940 0.008 230)"
  muted-foreground: "oklch(0.470 0.020 230)"
  accent: "oklch(0.910 0.030 230)"
  accent-foreground: "oklch(0.280 0.050 230)"
  border: "oklch(0.890 0.010 230)"
  input: "oklch(0.890 0.010 230)"
  ring: "oklch(0.760 0.121 230)"
  overlay: "oklch(0 0 0 / 50%)"
  destructive: "oklch(0.570 0.220 24)"
  destructive-foreground: "oklch(0.990 0.010 24)"
  destructive-soft: "oklch(0.930 0.060 24)"
  destructive-soft-foreground: "oklch(0.350 0.160 24)"
  destructive-solid-foreground: "oklch(0.990 0.010 24)"
  success: "oklch(0.920 0.060 145)"
  success-foreground: "oklch(0.300 0.110 145)"
  warning: "oklch(0.920 0.070 70)"
  warning-foreground: "oklch(0.320 0.130 55)"
  info: "oklch(0.920 0.045 210)"
  info-foreground: "oklch(0.300 0.080 225)"
  sidebar: "oklch(0.965 0.006 230)"
  sidebar-foreground: "oklch(0.200 0.030 230)"
  sidebar-primary: "oklch(0.640 0.130 230)"
  sidebar-primary-foreground: "oklch(0.180 0.028 230)"
  sidebar-accent: "oklch(0.910 0.030 230)"
  sidebar-accent-foreground: "oklch(0.280 0.050 230)"
  sidebar-border: "oklch(0.890 0.010 230)"
  sidebar-ring: "oklch(0.760 0.121 230)"
  chart-1: "oklch(0.640 0.130 230)"
  chart-2: "oklch(0.650 0.110 230)"
  chart-3: "oklch(0.350 0.059 230)"
  chart-4: "oklch(0.780 0.119 230)"
  chart-5: "oklch(0.550 0.020 230)"
  background-dark: "oklch(0.175 0.014 230)"
  foreground-dark: "oklch(0.950 0.006 230)"
  card-dark: "oklch(0.225 0.016 230)"
  card-foreground-dark: "oklch(0.950 0.006 230)"
  popover-dark: "oklch(0.225 0.016 230)"
  popover-foreground-dark: "oklch(0.950 0.006 230)"
  primary-dark: "oklch(0.760 0.136 230)"
  primary-foreground-dark: "oklch(0.160 0.024 230)"
  secondary-dark: "oklch(0.270 0.018 230)"
  secondary-foreground-dark: "oklch(0.920 0.008 230)"
  muted-dark: "oklch(0.270 0.014 230)"
  muted-foreground-dark: "oklch(0.680 0.020 230)"
  accent-dark: "oklch(0.320 0.045 230)"
  accent-foreground-dark: "oklch(0.930 0.012 230)"
  border-dark: "oklch(1 0 0 / 10%)"
  input-dark: "oklch(1 0 0 / 14%)"
  ring-dark: "oklch(0.760 0.114 230)"
  destructive-dark: "oklch(0.680 0.200 24)"
  destructive-foreground-dark: "oklch(0.160 0.030 24)"
  destructive-soft-dark: "oklch(0.280 0.070 24)"
  destructive-soft-foreground-dark: "oklch(0.850 0.130 24)"
  success-dark: "oklch(0.280 0.060 145)"
  success-foreground-dark: "oklch(0.850 0.130 145)"
  warning-dark: "oklch(0.280 0.070 55)"
  warning-foreground-dark: "oklch(0.850 0.140 80)"
  info-dark: "oklch(0.280 0.050 225)"
  info-foreground-dark: "oklch(0.850 0.090 210)"
  sidebar-dark: "oklch(0.200 0.016 230)"
  sidebar-foreground-dark: "oklch(0.950 0.006 230)"
  sidebar-primary-dark: "oklch(0.760 0.136 230)"
  sidebar-primary-foreground-dark: "oklch(0.160 0.024 230)"
  sidebar-accent-dark: "oklch(0.320 0.045 230)"
  sidebar-accent-foreground-dark: "oklch(0.930 0.012 230)"
  sidebar-border-dark: "oklch(1 0 0 / 10%)"
  sidebar-ring-dark: "oklch(0.760 0.114 230)"
  chart-1-dark: "oklch(0.760 0.136 230)"
  chart-2-dark: "oklch(0.600 0.102 230)"
  chart-3-dark: "oklch(0.850 0.079 230)"
  chart-4-dark: "oklch(0.450 0.076 230)"
  chart-5-dark: "oklch(0.680 0.020 230)"
  brand-ink: "#0f1f2a"
  brand-azure: "#0099cb"
  brand-white: "#ffffff"
  brand-favicon-dark: "#ebeff2"
  destructive-surface-60-dark: "#9b3c3d"
typography:
  heading:
    fontFamily: "Space Grotesk Variable"
  body:
    fontFamily: "Inter Variable"
  numeric:
    fontFamily: "Space Mono"
    fontWeight: 400
    fontFeature: "'tnum' 1"
  numeric-strong:
    fontFamily: "Space Mono"
    fontWeight: 700
    fontFeature: "'tnum' 1"
rounded:
  none: "0px"
  sm: "6px"
  md: "8px"
  lg: "10px"
  xl: "14px"
  full: "9999px"
spacing:
  "0": "0px"
  "px": "1px"
  "0.5": "0.125rem"
  "1": "0.25rem"
  "2": "0.5rem"
  "3": "0.75rem"
  "4": "1rem"
  "6": "1.5rem"
  "8": "2rem"
  "12": "3rem"
  "16": "4rem"
components:
  page:
    backgroundColor: "{colors.background}"
    textColor: "{colors.foreground}"
  card:
    backgroundColor: "{colors.card}"
    textColor: "{colors.card-foreground}"
  popover:
    backgroundColor: "{colors.popover}"
    textColor: "{colors.popover-foreground}"
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.primary-foreground}"
    rounded: "{rounded.md}"
    typography: "{typography.body}"
  button-secondary:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.secondary-foreground}"
  button-destructive:
    backgroundColor: "{colors.destructive}"
    textColor: "{colors.destructive-foreground}"
  badge-destructive:
    backgroundColor: "{colors.destructive-soft}"
    textColor: "{colors.destructive-soft-foreground}"
  badge-success:
    backgroundColor: "{colors.success}"
    textColor: "{colors.success-foreground}"
  badge-warning:
    backgroundColor: "{colors.warning}"
    textColor: "{colors.warning-foreground}"
  badge-info:
    backgroundColor: "{colors.info}"
    textColor: "{colors.info-foreground}"
  panel-muted:
    backgroundColor: "{colors.muted}"
    textColor: "{colors.muted-foreground}"
  state-accent:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.accent-foreground}"
  sidebar:
    backgroundColor: "{colors.sidebar}"
    textColor: "{colors.sidebar-foreground}"
  sidebar-button-primary:
    backgroundColor: "{colors.sidebar-primary}"
    textColor: "{colors.sidebar-primary-foreground}"
  sidebar-item-active:
    backgroundColor: "{colors.sidebar-accent}"
    textColor: "{colors.sidebar-accent-foreground}"
  surface-destructive-solid:
    backgroundColor: "{colors.destructive}"
    textColor: "{colors.destructive-solid-foreground}"
  hairline-border:
    backgroundColor: "{colors.border}"
  field-outline:
    backgroundColor: "{colors.input}"
  focus-ring:
    backgroundColor: "{colors.ring}"
  sidebar-hairline-border:
    backgroundColor: "{colors.sidebar-border}"
  sidebar-focus-ring:
    backgroundColor: "{colors.sidebar-ring}"
  chart-series-1:
    backgroundColor: "{colors.chart-1}"
  chart-series-2:
    backgroundColor: "{colors.chart-2}"
  chart-series-3:
    backgroundColor: "{colors.chart-3}"
  chart-series-4:
    backgroundColor: "{colors.chart-4}"
  chart-series-5:
    backgroundColor: "{colors.chart-5}"
  page-dark:
    backgroundColor: "{colors.background-dark}"
    textColor: "{colors.foreground-dark}"
  card-dark:
    backgroundColor: "{colors.card-dark}"
    textColor: "{colors.card-foreground-dark}"
  popover-dark:
    backgroundColor: "{colors.popover-dark}"
    textColor: "{colors.popover-foreground-dark}"
  button-primary-dark:
    backgroundColor: "{colors.primary-dark}"
    textColor: "{colors.primary-foreground-dark}"
  button-secondary-dark:
    backgroundColor: "{colors.secondary-dark}"
    textColor: "{colors.secondary-foreground-dark}"
  button-destructive-dark:
    backgroundColor: "{colors.destructive-dark}"
    textColor: "{colors.destructive-foreground-dark}"
  badge-destructive-dark:
    backgroundColor: "{colors.destructive-soft-dark}"
    textColor: "{colors.destructive-soft-foreground-dark}"
  badge-success-dark:
    backgroundColor: "{colors.success-dark}"
    textColor: "{colors.success-foreground-dark}"
  badge-warning-dark:
    backgroundColor: "{colors.warning-dark}"
    textColor: "{colors.warning-foreground-dark}"
  badge-info-dark:
    backgroundColor: "{colors.info-dark}"
    textColor: "{colors.info-foreground-dark}"
  panel-muted-dark:
    backgroundColor: "{colors.muted-dark}"
    textColor: "{colors.muted-foreground-dark}"
  state-accent-dark:
    backgroundColor: "{colors.accent-dark}"
    textColor: "{colors.accent-foreground-dark}"
  sidebar-dark:
    backgroundColor: "{colors.sidebar-dark}"
    textColor: "{colors.sidebar-foreground-dark}"
  sidebar-button-primary-dark:
    backgroundColor: "{colors.sidebar-primary-dark}"
    textColor: "{colors.sidebar-primary-foreground-dark}"
  sidebar-item-active-dark:
    backgroundColor: "{colors.sidebar-accent-dark}"
    textColor: "{colors.sidebar-accent-foreground-dark}"
  surface-destructive-solid-dark:
    backgroundColor: "{colors.destructive-surface-60-dark}"
    textColor: "{colors.destructive-solid-foreground}"
  hairline-border-dark:
    backgroundColor: "{colors.border-dark}"
  field-outline-dark:
    backgroundColor: "{colors.input-dark}"
  focus-ring-dark:
    backgroundColor: "{colors.ring-dark}"
  sidebar-hairline-border-dark:
    backgroundColor: "{colors.sidebar-border-dark}"
  sidebar-focus-ring-dark:
    backgroundColor: "{colors.sidebar-ring-dark}"
  chart-series-1-dark:
    backgroundColor: "{colors.chart-1-dark}"
  chart-series-2-dark:
    backgroundColor: "{colors.chart-2-dark}"
  chart-series-3-dark:
    backgroundColor: "{colors.chart-3-dark}"
  chart-series-4-dark:
    backgroundColor: "{colors.chart-4-dark}"
  chart-series-5-dark:
    backgroundColor: "{colors.chart-5-dark}"
  logo-mark-fill:
    backgroundColor: "{colors.brand-ink}"
  logo-mark-lifted-half:
    backgroundColor: "{colors.brand-azure}"
  logo-app-icon-tile:
    backgroundColor: "{colors.brand-azure}"
  logo-mark-fill-on-dark:
    backgroundColor: "{colors.brand-white}"
  favicon-mark-dark-scheme:
    backgroundColor: "{colors.brand-favicon-dark}"
  scrim-modal:
    backgroundColor: "{colors.overlay}"
---

## Overview

The identity is named **Lagune** (decision of 2026-09-15). One azure hue, `230`, runs through almost
the entire palette, varied by lightness and chroma, with three semantic tones sitting deliberately off
it. Surfaces are near-white and near-black rather than pure, and every pairing in the product was
checked against WCAG AA before it shipped.

The tokens in the front matter above are the normative values. This prose says where each one came
from and what it is for.

**Source of truth:** [`frontend/src/index.css`](https://github.com/invoicerr-app/invoicerr/blob/main/frontend/src/index.css)
in the product repository. The landing site
([`landing/src/index.css`](https://github.com/invoicerr-app/landing/blob/main/src/index.css)) carries a
copy of the subset it uses and says so in its own header comment. If a value here disagrees with
`index.css`, `index.css` wins and this file is the bug.

## Colors

### How they are written, and why the front matter is not hex

The product declares every colour in OKLCH, not hex, so the front matter carries the OKLCH string
verbatim. The DESIGN.md format accepts `oklch()` directly and converts to sRGB internally for contrast
checking, so nothing is lost by keeping the original notation, and a diff against `index.css` stays a
character-for-character diff.

The hex values in the tables below are the sRGB rendering of those same triplets, computed
(OKLCH to linear sRGB to sRGB, D65), not sampled from a screenshot. Two values confirm the pipeline:
`frontend/index.html` states in a comment that `oklch(0.975 0.005 230)` is `#f3f7f9` and
`oklch(0.175 0.014 230)` is `#0a1215`, and the computation returns exactly those.

**`*` marks a colour whose OKLCH value sits outside the sRGB gamut**; the hex is the clipped rendering
a browser will show. These markers matter: they say the on-screen colour is not quite the declared one.

### Naming

A token with no suffix is the light theme, read from the `:root` block of `index.css` (line 96
onward). A token suffixed `-dark` is the dark theme, read from the `.dark` block (line 160 onward).
The DESIGN.md format has no theme axis, so that suffix is this file's own convention. It is not a name
used anywhere in the product.

Three tokens exist only once because `.dark` deliberately does not redefine them: `overlay`,
`destructive-solid-foreground`, and the brand literals.

### Surfaces and text

| Token | Light hex | Dark hex | Role, and where it comes from |
| --- | --- | --- | --- |
| `background` | `#f3f7f9` | `#0a1215` | The page itself. Also the two `theme-color` meta values in `frontend/index.html` lines 29 and 30. |
| `foreground` | `#061821` | `#ebeff2` | Body text. Never pure black, never pure white. |
| `card` | `#fbfeff` | `#141d22` | A raised panel, one step off the background. |
| `popover` | `#fbfeff` | `#141d22` | Menus and dialogs. Same pair as `card`. |
| `muted` | `#e6ecef` | `#20282c` | A quiet fill. |
| `muted-foreground` | `#505d64` | `#8c9ba2` | Secondary text. |
| `border` | `#d4dce0` | white at 10% | Every hairline. Dark mode uses translucent white rather than a fixed grey. |
| `input` | `#d4dce0` | white at 14% | Field outlines. |
| `overlay` | black at 50% | the same | The scrim behind a modal. A structural dimming layer, not content, so it is identical in both themes on purpose. |

### Brand and interaction

| Token | Light hex | Dark hex | Role |
| --- | --- | --- | --- |
| `primary` | `#0099cb` * | `#39c0f6` | The brand azure. Primary buttons, links, the lifted half of the mark. |
| `primary-foreground` | `#04141c` | `#030f16` | Ink on a primary fill. Dark in both themes, because `primary` is light in both. |
| `secondary` | `#e3edf2` | `#1d282e` | Secondary button fill. |
| `accent` | `#cee6f2` | `#183745` | Hover and selected states. |
| `ring` | `#50bfef` | `#59beeb` | The focus ring. |

### Semantic tones

Each is a soft fill paired with saturated text on it, so a badge only ever needs
`bg-<tone> text-<tone>-foreground`. `index.css` records that the pairs were verified at 9.3:1 or better
fill-to-text and 10.6:1 or better text-on-card, in both themes; the `components` block above reproduces
those pairings so the linter re-checks them on every run.

| Token | Light hex | Dark hex |
| --- | --- | --- |
| `success` | `#cdf0cd` | `#133015` |
| `success-foreground` | `#003b00` * | `#96e498` |
| `warning` | `#ffddb2` * | `#421d00` * |
| `warning-foreground` | `#601400` * | `#fdc357` |
| `info` | `#c3edf5` | `#83deee` |
| `info-foreground` | `#00354c` * | `#042e3b` |
| `destructive` | `#db192f` | `#fc5858` |
| `destructive-soft` | `#ffd9d5` | `#451817` |
| `destructive-soft-foreground` | `#790006` * | `#ffaba4` |

Two rules the file states outright, and that are easy to break:

- **Green is reserved for `success`.** Never introduce a second green anywhere in the product.
- **`destructive-foreground` flips** between themes, because `destructive` itself lightens in dark
  mode. Near-white ink on a light red no longer clears AA, so the dark theme uses dark ink instead.

### The destructive surface at 60% opacity

`destructive-solid-foreground` is the one token deliberately identical in both themes, and it is the
one that looks like a mistake until you know why. `button.tsx` composites a destructive surface at
`dark:bg-destructive/60`, so the real background in dark mode is not `destructive-dark` but that colour
mixed 60/40 with `background-dark`. That composite is `#9b3c3d`, carried in the front matter as
`destructive-surface-60-dark` so the component above can point at the colour that is actually rendered.

Measured on the composite: **6.49:1** for the near-white ink, **2.89:1** for dark ink. `index.css`
states 6.1 to 6.5:1 and 2.9 to 3.1:1 for the same pair, so this reproduces the product's own numbers.
That is why the token must not get a `.dark` override.

### Charts

Five steps, all on hue 230 except the neutral fifth, so a chart reads as one family.

| Token | Light | Dark |
| --- | --- | --- |
| `chart-1` | `#0099cb` * | `#39c0f6` |
| `chart-2` | `#369bc5` | `#2f8bb1` |
| `chart-3` | `#124053` | `#97d8f8` |
| `chart-4` | `#5ac5f5` | `#1d5d77` |
| `chart-5` | `#66747b` | `#8c9ba2` |

They are declared as components with a `backgroundColor` and no `textColor`, because a series is a
fill, not text on a ground. Asserting a text pairing there would be inventing a relationship the
product does not have.

### The sidebar

The sidebar has its own surface pair; its other tokens repeat the values above. `index.css` also
carries a second `:root` / `.dark` pair for the sidebar inside `@layer base`. It is dead weight and
says so in its own comment: Tailwind v4 resolves unlayered rules before layered ones regardless of
source order, so the unlayered block always wins. Do not read those lines as a second source of truth.

### The logo's own colours

The SVG files in the brand repository do **not** use CSS variables. A favicon is fetched by the browser
outside any DOM and could not read them, so the files carry literals:

| Token | Value | Where it appears | Relation to the palette |
| --- | --- | --- | --- |
| `brand-ink` | `#0f1f2a` | the mark and wordname ink, every `logo/*.svg` | `oklch(0.231 0.030 239.9)`. A fixed brand ink, close to but **not equal to** `foreground` light (`#061821`). Keep it exact; do not substitute the token. |
| `brand-azure` | `#0099cb` | the lifted half in `lockup.svg` and `mark-duo.svg`, the tile in `app-icon.svg` | Exactly `primary` light, clipped into sRGB. |
| `brand-white` | `#ffffff` | `lockup-white.svg`, `mark-white.svg`, `wordmark-white.svg` | Pure white, for a dark or photographic ground. The one place the identity allows pure white. |
| `brand-favicon-dark` | `#ebeff2` | `favicon/favicon.svg`, dark-scheme branch only | `foreground` dark. The favicon themes itself with an embedded `prefers-color-scheme` rule instead of going white. |

The in-app React component (`landing/src/components/brand-mark.tsx`) takes a third route: it paints the
mark in `currentColor` and the lifted half in `fill-primary`, so the mark inherits the surrounding text
colour and the azure follows the theme.

## Typography

Three families, all self-hosted through Fontsource. `index.css` states the reason in its header: the
PWA has to work offline and no font request may leak to a third party. There is no Google Fonts call at
runtime.

| Front matter token | Family | Package | Weights shipped | Used for |
| --- | --- | --- | --- | --- |
| `heading` | Space Grotesk Variable | `@fontsource-variable/space-grotesk` ^5.3.0 | the whole variable axis, one file | `h1` to `h4`, applied in `@layer base` |
| `body` | Inter Variable | `@fontsource-variable/inter` ^5.3.0 | the whole variable axis, one file | body and all interface text |
| `numeric`, `numeric-strong` | Space Mono | `@fontsource/space-mono` ^5.3.0 | static `400` and `700` only | figures and codes |

Fallback stacks, verbatim from `index.css` lines 22 to 24. The front matter carries only the family
name, because `fontFamily` is a single string in this format and the fallback chain has nowhere to go:

```css
--font-sans:    'Inter Variable', ui-sans-serif, system-ui, sans-serif;
--font-heading: 'Space Grotesk Variable', ui-sans-serif, system-ui, sans-serif;
--font-mono:    'Space Mono', ui-monospace, 'SFMono-Regular', monospace;
```

No italic of Space Mono is imported, because the product uses that face only for numbers and codes.

Monetary and numeric cells use a custom utility rather than Tailwind's `tabular-nums`, because the face
has to change too (`index.css` line 293):

```css
@utility amount {
  font-family: var(--font-mono);
  font-variant-numeric: tabular-nums;
}
```

The `fontFeature: "'tnum' 1"` on `numeric` and `numeric-strong` is this file's translation of that
`font-variant-numeric: tabular-nums` into the OpenType feature the format can express. It is the only
value in the front matter that is a translation rather than a transcription.

**No font sizes are declared, and that is not an omission.** `index.css` sets sizes per component and
says in its own comment that a full type-scale pass is still outstanding. Inventing a scale here would
be inventing a design decision the product has not made.

## Layout

No override. Neither stylesheet redefines `--spacing`, so the product runs on Tailwind's default
0.25rem scale. The `spacing` block in the front matter is that stock scale, written out at the steps
the product actually uses, so a tool has something to diff rather than nothing.

## Elevation & Depth

No override either. Grepping `--shadow` and `box-shadow` in both stylesheets returns nothing: the
product uses Tailwind's stock `shadow-*` utilities unchanged. Depth in this identity comes from the
surface ladder (`background`, then `card` and `popover` one step off it) rather than from shadows.

`overlay` is the only deliberate depth token: plain black at 50%, identical in both themes, because a
themed scrim would either wash out in dark mode or barely darken anything in light mode.

## Shapes

One base value, three derived steps (`index.css` lines 18 to 21 and 104):

| Token | Declared as | Computed |
| --- | --- | --- |
| `--radius` | `0.625rem` | 10px, the `lg` step |
| `--radius-sm` | `calc(var(--radius) - 4px)` | 6px |
| `--radius-md` | `calc(var(--radius) - 2px)` | 8px |
| `--radius-xl` | `calc(var(--radius) + 4px)` | 14px |

The front matter resolves those `calc()` expressions to pixels, since the format has no arithmetic.
`none` and `full` are Tailwind's own ends of the scale, included so the set is usable.

**The logo does not use this scale.** The mark's rounded square is a 72-unit corner radius on a
320-unit square (`M168 96H344A72 72 0 0 1 416 168...`), and the app-icon tile is `rx="114.176"` on 512,
the iOS squircle proportion. Those are geometry, not tokens.

## Components

Every component above is a real pairing in the product, not a sample. Each carries a `backgroundColor`,
and a `textColor` only where text genuinely sits on that ground. Hairlines, rings, scrims, chart series
and logo fills are declared with a background alone, because they are fills.

The full set is declared twice, once per theme, with the `-dark` suffix described under **Colors**.
The one component that is not a straight mirror is `surface-destructive-solid-dark`, which points at
the 60% composite rather than the solid colour, for the reason given above.

Three real contrast numbers, computed with the same WCAG formula the linter uses:

| Component | Light | Dark |
| --- | --- | --- |
| `button-primary` | 5.72:1 | 9.27:1 |
| `panel-muted` | 5.70:1 | 5.23:1 |
| `button-destructive` | 4.81:1 | 6.20:1 |

`button-destructive` at 4.81:1 in light is the tightest pairing in the system. `index.css` records that
this was arrived at deliberately after owner feedback that the red was too dark: lightness moved
0.530 to 0.570, and 0.580 was rejected because it drops the same pairing to 4.47:1, under AA.

## Do's and Don'ts

- **Do** take values from `index.css`, not from this file, when you are writing product code. This file
  is a mirror for tools and for people who cannot open the repository.
- **Do** keep `brand-ink` exact in the logo files. It is not `foreground`, and substituting the token
  would shift the mark.
- **Do** use `oklch()` when adding a colour to the product, so it stays in the same space as the rest.
- **Don't** introduce a second green. Green means `success`.
- **Don't** add a `.dark` override for `destructive-solid-foreground`. The composite maths above is why.
- **Don't** treat the `@layer base` sidebar block in `index.css` as a source of truth. It is unreachable
  and documented as such.
- **Don't** invent a type scale from this file. The product has not set one.

## Provenance of every value here

The format has no field for a citation, so the citations live in the prose above rather than in the
front matter, and they are deliberate rather than decorative. Every table names the file and, where it
is stable enough to be useful, the line. The three files cited are:

- `invoicerr/frontend/src/index.css`: the whole palette, the fonts, the radii, the `amount` utility.
- `invoicerr/frontend/index.html`: the two `theme-color` values, and the comment that independently
  confirms the OKLCH to sRGB conversion used throughout.
- `landing/src/components/brand-mark.tsx`: how the mark is coloured in the running interface.

## What this file cannot express

Stated so nobody reads a gap as a decision:

- **Themes.** The format has one flat colour namespace; the `-dark` suffix is a workaround.
- **Alpha-composited surfaces.** `destructive-surface-60-dark` is a precomputed literal because the
  format cannot express "this colour at 60% over that one".
- **Fallback font stacks.** Only the first family survives.
- **`calc()` in radii.** Resolved to pixels here; the product keeps the expressions.
- **Per-component type sizes**, which the product sets in components and has not yet unified.

## The phrases the product actually uses

Quoted with their source. Do not paraphrase them into something new.

| Phrase | Where |
| --- | --- |
| "The invoicing app that keeps up with you." | `landing/src/components/sections/hero.tsx` line 48 |
| "Open-source invoicing, in the cloud or on your own server." | `landing/src/components/footer.tsx` line 54 |
| "Open-source invoicing for freelancers" | `documentation/docusaurus.config.ts` line 11, the Docusaurus `tagline` |
| "OPEN SOURCE · SELF-HOSTED" | the badge rendered in `social/og.jpg` and `social/banner.webp` |
