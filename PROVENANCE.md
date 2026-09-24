# Where each file came from

Nothing here was drawn for this repository. Every file is either copied byte for byte out of a
product repository, or derived mechanically from one of those files. This page records which.

Assembled on 2026-09-24. Re-synced the same day after `invoicerr-app/invoicerr#458` corrected the
lockup's geometry: the three lockup SVGs were copied again from the frontend, and the four rasters
derived from them were regenerated rather than resampled. See "Re-syncs" at the foot of this page.

## Copied unchanged

| This repository | Source |
| --- | --- |
| `logo/mark.svg` | `invoicerr/frontend/public/brand/logo-mark.svg` |
| `logo/lockup.svg` | `invoicerr/frontend/public/brand/logo-full.svg` |
| `logo/lockup-ink.svg` | `invoicerr/frontend/public/brand/logo-black.svg` |
| `logo/lockup-white.svg` | `invoicerr/frontend/public/brand/logo-white.svg` |
| `logo/wordmark.svg` | `invoicerr/frontend/public/brand/logo-wordmark.svg` |
| `logo/app-icon.svg` | `invoicerr/frontend/public/brand/logo-icon.svg` |
| `favicon/*` (all 11 files) | `invoicerr/frontend/public/` |
| `social/og.jpg` | `landing/public/og.jpg`, the file served at `https://invoicerr.app/og.jpg` |
| `social/banner.webp` | `invoicerr/Invoicerr_banner.webp`, the product README's header image |

`invoicerr/documentation/static/img/brand/logo-full.svg` and `logo-white.svg` are byte-identical to
the frontend copies (md5 checked), as are the documentation's and the landing's favicon files. The
frontend copy is treated as canonical because it is the one the brand SVGs' own comments point at.

## Derived

| This repository | Derived from | How |
| --- | --- | --- |
| `logo/mark-duo.svg` | `logo/mark.svg` | The second of the two path fills changed from `#0f1f2a` to `#0099cb`, and the two clip-path ids renamed to stay unique. This reproduces what `logo-full.svg` already does to its own mark, and what `landing/src/components/brand-mark.tsx` renders by default (`variant="duo"`, the lifted half painted `fill-primary`). No geometry was touched. |
| `logo/mark-white.svg` | `logo/mark.svg` | Both fills changed `#0f1f2a` to `#ffffff`, the same swap `logo-white.svg` performs on the full lockup. Clip-path ids renamed. |
| `logo/wordmark-white.svg` | `logo/wordmark.svg` | Same `#0f1f2a` to `#ffffff` swap. |
| `social/banner.png` | `social/banner.webp` | `magick banner.webp banner.png`, no resize, 1621 x 810. A PNG alongside the WebP for the few renderers that still do not take WebP. |
| `preview/*.png` | the matching white `logo/*.svg` | `rsvg-convert` then `magick -background '#0a1215' -alpha remove`, which bakes the dark page background in. README display only, because GitHub strips a `style` attribute from a README and a white SVG shown directly would be invisible under the light theme. Never a distributable asset. |
| `png/*` | the matching `logo/*.svg` | `rsvg-convert` (librsvg), vector rasterisation at the target pixel size, not a resample of a smaller bitmap. |

### Why those PNG sizes and no others

- **256** - a mark shown inline in a README at 1x to 2x, and the smallest size GitHub accepts for an
  organisation avatar comfortably.
- **512** - the size the product itself exports its app icon at, and enough for a 256pt slide at 2x.
- **1024** - a lockup across the top of a slide or a conference banner without softening.

Everything else that needs a raster already exists in `favicon/`, at the sizes the browsers and the
web manifest actually ask for. Nothing was exported "in case".

### One useful check

`rsvg-convert -w 512 logo/app-icon.svg` produces a file byte-identical (md5
`7e202a6b830913324a786020760dbd19`) to the `icon-512.png` the product ships. So the product's own
raster pipeline is librsvg at the nominal size, and the exports in `png/` are produced the same way
the product produces its own.

## Known disagreements between existing copies

These were found while gathering and are **not** resolved here. Nothing in another repository was
touched.

1. **`invoicerr/documentation/static/img/docusaurus-social-card.jpg` is still the stock Docusaurus
   placeholder** - the green dinosaur and the words "Build optimized websites". It is wired as the
   docs site's `image:` in `docusaurus.config.ts` line 170, so every link to `docs.invoicerr.app`
   previews as Docusaurus rather than as Invoicerr. `social/og.jpg` here is the real card.
2. **`social/og.jpg` is 1200 x 600, not the 1200 x 630 convention.** `landing/index.html` declares
   `og:image:height` as 600, so the declaration is honest and nothing is broken, but some crawlers
   letterbox a 2:1 card.
3. **`logo/mark.svg` is single-ink while the product renders the mark in duo.** The standalone mark
   file in the product paints both halves `#0f1f2a`, whereas `logo-full.svg`, `logo-icon.svg` and the
   landing's `BrandMark` component all paint the lifted half azure. Whether the standalone file
   should have been duo all along is an open question; this repository ships both and names the duo
   one as the default.
4. **The brand ink `#0f1f2a` is not `--foreground`.** The light `--foreground` token computes to
   `#061821`. The ink is `oklch(0.231 0.030 239.9)`, a separate fixed value. Deliberate or drift, it
   is worth knowing before anyone "aligns" them.

## Not produced, and why

- **A light banner.** `social/banner.webp` exists only as a raster with a dark background baked in,
  and there is no source file, layout script or layered original anywhere in the organisation that it
  could be re-rendered from. Drawing a light one would mean redrawing the banner, which is designing a
  new asset rather than gathering an existing one.
- **A light Open Graph card**, for the same reason.
- **A light-ground variant of anything else.** Not needed: the default lockup, mark and wordmark are
  already the light-ground versions.

## Re-syncs

A source file in a product repository can change after it was copied here. When that happens the
copy is taken again and every raster derived from it is regenerated from the vector, never resampled
from the older bitmap. Each re-sync is recorded here with what moved and why.

### 2026-09-24 - lockup geometry

`invoicerr-app/invoicerr#458` recentred the mark on the wordmark's ink centroid and removed the
padding the canvas carried. The viewBox went from `0 0 258.6978 72` to `0 0 233.3267 58.428`, and
the two group transforms moved with it. Every path `d` string and every fill is unchanged: no
artwork was redrawn and no font was substituted for the outlined wordmark.

Copied again: `logo/lockup.svg`, `logo/lockup-ink.svg`, `logo/lockup-white.svg`.

Regenerated: `png/lockup-1024.png`, `png/lockup-512.png`, `png/lockup-white-1024.png` with
`rsvg-convert -w <size>`, and `preview/lockup-white-on-dark.png` the same way then
`magick -background '#0a1215' -alpha remove -bordercolor '#0a1215' -border 40`.

The rasters are shorter than before because the lockup is: `png/lockup-1024.png` went from
1024 x 285 to 1024 x 257. Nothing in the README fixes a height, so no markup needed changing.
