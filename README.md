<p align="center">
  <img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/social/banner.webp" alt="Invoicerr" width="820">
</p>

# Invoicerr brand assets

Every Invoicerr logo, icon and social image, in one place, so a Markdown file anywhere in the
organisation can link to a stable URL instead of carrying its own copy.

- **[DESIGN.md](./DESIGN.md)** - the palette, typefaces and radii, in the
  [DESIGN.md format](https://www.npmjs.com/package/@google/design.md): machine-readable tokens in the
  YAML front matter, so a tool can diff them against what the product actually declares, and the
  citation of the source file for every value in the prose below it.
- **[TRADEMARK.md](./TRADEMARK.md)** - what you may do with the name and the logos, and what you may
  not. The code is AGPL-3.0; these assets are not.

**To use an asset in Markdown, copy the raw URL under it.** Raw URLs are served with the right content
type and work in a README, an issue, a release note and on a third-party site. Do not link to the
`github.com/.../blob/...` page: that serves an HTML page, not an image.

---

## The mark

The mark alone. A rounded square cut along a 19.3 degree slash, the right half lifted.

| | | |
| --- | --- | --- |
| <img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/mark-duo.svg" height="72"> | <img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/mark.svg" height="72"> | <img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/preview/mark-white-on-dark.png" height="72"> |
| **mark-duo.svg** | **mark.svg** | **mark-white.svg** |
| The default. Ink plus azure. Use it on any light ground. | Single-ink. For one-colour printing, a stamp, or anywhere the azure would clash. | For a dark or photographic ground, where the ink half would disappear. |

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/mark-duo.svg
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/mark.svg
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/mark-white.svg
```

PNG: [mark-duo-256.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/mark-duo-256.png) - [mark-duo-512.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/mark-duo-512.png) - [mark-white-512.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/mark-white-512.png)

## The lockup: mark plus wordname

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/lockup.svg" width="340">

The default lockup. Ink wordname, duo mark. **Use this one unless you have a reason not to.**

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/lockup.svg
```

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/preview/lockup-white-on-dark.png" width="360">

All white, for a dark ground. This is what the documentation site's navbar switches to in dark mode.

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/lockup-white.svg
```

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/lockup-ink.svg" width="340">

All ink, no azure. For one-colour printing and for a ground the azure would fight.

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/lockup-ink.svg
```

PNG: [lockup-512.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/lockup-512.png) - [lockup-1024.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/lockup-1024.png) - [lockup-white-1024.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/lockup-white-1024.png)

## The wordname alone

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/wordmark.svg" width="260">

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/preview/wordmark-white-on-dark.png" width="290">

For a context that already carries the mark right next to it, such as a header whose favicon is
already the mark.

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/wordmark.svg
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/wordmark-white.svg
```

PNG: [wordmark-512.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/wordmark-512.png) - [wordmark-white-512.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/png/wordmark-white-512.png)

## The app icon

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/app-icon.svg" width="96">

The mark on a filled azure tile, with the iOS squircle corner. For an app icon, an avatar, a favicon
tile, or anywhere the logo needs its own shape rather than sitting on the page's background.

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/logo/app-icon.svg
https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/icon-512.png
```

## Banner

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/social/banner.webp" width="600">

1621 x 810. The header image at the top of a README. It carries its own dark background, so it reads
the same under GitHub's light and dark themes and needs no second variant.

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/social/banner.webp
https://raw.githubusercontent.com/invoicerr-app/brand/main/social/banner.png
```

## Open Graph image

<img src="https://raw.githubusercontent.com/invoicerr-app/brand/main/social/og.jpg" width="600">

1200 x 600. The link preview card, for `og:image` and `twitter:image` with
`twitter:card=summary_large_image`. This is the exact file served at `https://invoicerr.app/og.jpg`.

```
https://raw.githubusercontent.com/invoicerr-app/brand/main/social/og.jpg
```

## Favicons

The whole stack the product ships, unchanged. `favicon.svg` themes itself: it carries an embedded
`prefers-color-scheme` rule and switches between the brand ink and a near-white, so one file covers a
light and a dark browser tab. The PNG pairs cover the browsers that understand `media` on a
`<link rel="icon">` but do not render an SVG favicon.

| File | Size | For |
| --- | --- | --- |
| [favicon.svg](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/favicon.svg) | vector | The modern default. Self-theming. |
| [favicon.ico](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/favicon.ico) | 16, 32, 48 | The file browsers still request from the site root. |
| [favicon-16.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/favicon-16.png) / [favicon-32.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/favicon-32.png) | 16, 32 | Light-scheme and universal fallback. |
| [favicon-16-dark.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/favicon-16-dark.png) / [favicon-32-dark.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/favicon-32-dark.png) | 16, 32 | Dark-scheme pair. |
| [apple-touch-icon.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/apple-touch-icon.png) | 180 | iOS home screen. |
| [icon-96.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/icon-96.png) / [icon-192.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/icon-192.png) / [icon-512.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/icon-512.png) | 96, 192, 512 | Web manifest, PWA install. |
| [icon-512-maskable.png](https://raw.githubusercontent.com/invoicerr-app/brand/main/favicon/icon-512-maskable.png) | 512 | Android adaptive icon, with the safe-zone padding `purpose: maskable` requires. |

---

## Which one do I want

| Situation | File |
| --- | --- |
| README header | `social/banner.webp` |
| Link preview card | `social/og.jpg` |
| Logo in a light page header | `logo/lockup.svg` |
| Logo in a dark page header | `logo/lockup-white.svg` |
| Avatar, app icon, square slot | `logo/app-icon.svg` |
| Small inline mark next to text | `logo/mark-duo.svg` |
| One-colour print, engraving, a stamp | `logo/lockup-ink.svg` or `logo/mark.svg` |
| Browser tab | `favicon/favicon.svg` |

## Rules worth one line each

- **SVG is the source of truth.** The PNGs are exports. If you need a size that is not here, render it
  from the SVG rather than upscaling a PNG.
- **Keep the colours exact.** Ink `#0f1f2a`, azure `#0099cb`. Both are in DESIGN.md with their
  origin.
- **Do not redraw or recolour the mark.** If none of the variants fits your ground, ask.
- **Leave clear space** around the logo of at least the height of the mark's own corner radius.
- Read [TRADEMARK.md](./TRADEMARK.md) before using the name or the mark for anything of your own.

## A note on the previews in this page

The three images above showing a white asset on a dark plate live in `preview/`. They are PNGs with
the background baked in, and they exist only so this page stays readable: GitHub strips a `style`
attribute from a README, so a white SVG shown here directly would be invisible under the light theme.
**Do not use `preview/` anywhere else.** The assets to link to are the SVGs, whose raw URLs are in the
code block under each one.

## Where these came from

Nothing in this repository was drawn for it. Provenance, and the exports, are recorded in
[PROVENANCE.md](./PROVENANCE.md).
