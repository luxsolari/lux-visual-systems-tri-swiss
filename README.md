# Lux Visual Systems - Tri-Swiss

[![Version](https://img.shields.io/github/v/release/luxsolari/lux-visual-systems-tri-swiss)](https://github.com/luxsolari/lux-visual-systems-tri-swiss/releases)
[![License: MIT/X11](https://img.shields.io/badge/license-MIT%2FX11-blue.svg)](LICENSE)
[![Design: CC BY-SA 4.0](https://img.shields.io/badge/design-CC%20BY--SA%204.0-lightgrey.svg)](LICENSE-DESIGN)

<p align="center">
  <a href="https://luxsolari.github.io/lux-visual-systems-tri-swiss/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="docs/assets/banner-dark.png" />
      <img src="docs/assets/banner-light.png" alt="Lux Visual Systems - Tri-Swiss — two colors, one accent, one genuine third" width="960" />
    </picture>
  </a>
</p>

<p align="center"><strong><a href="https://luxsolari.github.io/lux-visual-systems-tri-swiss/">Showcase and documentation →</a></strong></p>

A Claude Code plugin that teaches Claude **Lux Visual Systems - Tri-Swiss** — Lux Solari's
house design language, sibling to
[Lux Visual Systems - Lux Swiss](https://github.com/luxsolari/lux-visual-systems-lux-swiss) (formerly Duotone
Swiss) — so every project you build shares one consistent, opinionated
aesthetic.

Lux Visual Systems - Tri-Swiss and Lux Visual Systems - Lux Swiss are the two house-mark design systems that carry
Lux Solari's personal brand identity into every project built with them —
related governance, distinct palettes. See [HOUSE-MARK.md](HOUSE-MARK.md)
for how the two relate.

## The aesthetic

**Tri-tone, more colorful, still Swiss-minimalist.** Two structural colors
— ink (`#000000`) and warm cream (`#f5efe0`) — plus a Swiss Red accent
(`#d3281b`) that now also marks section dividers, selective card emphasis,
a genuine Structural Block (a solid-color sidebar/hero band, capped at
~25% of viewport, or a bold word inside a heading), and hover-state
feedback wherever an accent signals interactivity, and a non-semantic
highlight, Pastel Turquoise (`#56bfa3`), used decoratively across icon
fills, underlines, washes, chart series, a hover-triggered flourish on
nav links, and now its own smaller Structural Block (a callout panel, a
second-moment panel, a closing band). The tri-part segment stripe — the
one place all three colors meet — is reusable at any length as a
decorative divider, not a one-off. A new Accent button and Accent card
put more color on hover/borders, and a second named exception — a
dual-accent hover swap on the Accent button and a new Interactive card —
lets Turquoise carry real hover meaning in exactly those two places.
Lists, tables, and images are now documented patterns too — list/table
borders and markers stay ink/muted-foreground only, and images default
to a grayscale/duotone filter with full color as a scoped exception for
photography that is itself the content. No success green, no info blue,
no second *semantic* accent otherwise — the highlight never carries
meaning outside its two named hover exceptions, however often it recurs.

- Visible 1px borders everywhere; **no shadows** (elevation is a background step).
- Generous whitespace; mostly square corners.
- **Space Mono** for headings, data, tags, and nav; **Space Grotesk** for
  body — or the **Geist** flavor (Geist Mono + Geist Sans), toggled with
  a single `.geist` class; Zilla Slab (serif, long-form) is shared by both,
  and mono italic covers annotations/captions in either flavor.
- An optional **Jost** heading accent — every heading (`h1`–`h6`), the
  hero title/wordmark, and long-form editorial chapter dividers switch
  to Jost when toggled, independently of the flavor, with a `.jost`
  class; labels, nav, tags, and data stay on the mono flavor.
- Uppercase monospace labels with wide letter-spacing.
- Hand-rolled SVG charts by default — no chart libraries except a
  restyled Observable Plot.

## See it

[luxsolari.github.io/lux-visual-systems-tri-swiss](https://luxsolari.github.io/lux-visual-systems-tri-swiss/) is both
the showcase and the documentation. Its sidebar is Red's Structural Block,
its Overview ends in Turquoise's, and every demo on it is plain HTML on the
tokens:

| Page | What it documents |
|------|-------------------|
| [Overview](https://luxsolari.github.io/lux-visual-systems-tri-swiss/) | The banner, the two governing rules, how to use the system, the do-not list, the Turquoise moment and closing band |
| [Colors](https://luxsolari.github.io/lux-visual-systems-tri-swiss/colors.html) | Fifteen semantic tokens in both themes, Red's jobs, Turquoise's jobs, the three guardrails, measured contrast |
| [Typography](https://luxsolari.github.io/lux-visual-systems-tri-swiss/typography.html) | Three roles, the Space/Geist flavors, the weight axis, the heading scale, labels, Jost |
| [Spacing](https://luxsolari.github.io/lux-visual-systems-tri-swiss/spacing.html) | Spacing steps, the one radius, fixed sizes including Turquoise's caps, opacity states |
| [Components](https://luxsolari.github.io/lux-visual-systems-tri-swiss/components.html) | Nineteen patterns with live demos and guidelines |
| [Structural Block](https://luxsolari.github.io/lux-visual-systems-tri-swiss/structural-block.html) | Sidebar, hero band, bold word, the tri-part stripe, the hover hierarchy |
| [Highlight](https://luxsolari.github.io/lux-visual-systems-tri-swiss/highlight.html) | The Turquoise token: sanctioned uses, its own block, the dual-accent exception |
| [Charts](https://luxsolari.github.io/lux-visual-systems-tri-swiss/charts.html) | Hand-rolled SVG, the governed third line, restyled Observable Plot |
| [House Mark](https://luxsolari.github.io/lux-visual-systems-tri-swiss/house-mark.html) | How Lux Visual Systems - Tri-Swiss and Lux Visual Systems - Lux Swiss relate |

The site is static HTML under `docs/`, served by GitHub Pages: `docs/assets/site.css`
holds the tokens and every pattern, `docs/assets/site.js` the theme, flavor and Jost
toggles. The banner above is `docs/banner.html`, rendered by
`scripts/capture/banner.sh`.

Light and dark are the same tri-tone system inverted — difference by
contrast, never by a new hue:

| Light | Dark |
|-------|------|
| ![Light mode hero](docs/assets/hero-light.png) | ![Dark mode hero](docs/assets/hero-dark.png) |

Three type registers and the component library:

![Type registers](docs/assets/type-registers.png)
![Component gallery](docs/assets/components.png)
![Charts](docs/assets/charts.png)
![Observable Plot, restyled](docs/assets/plot.png)

Turquoise's own Structural Block — a genuine third color, not an occasional accent:

![Turquoise second-moment panel](docs/assets/turquoise-moment.png)
![Turquoise closing band](docs/assets/closing-band.png)

## What it does

Once installed, the `lux-visual-systems-tri-swiss` skill activates automatically whenever
Claude builds or restyles UI — components, pages, forms, dashboards,
Tailwind/CSS themes — and applies these tokens and patterns by default,
even if you don't name the design system. You can also invoke it explicitly
("apply my design system", "make this lux-visual-systems-tri-swiss", "use the tri-tone system").

The skill bundles:

- **`assets/theme.css`** — ready-to-paste Tailwind 4 theme with every token
  for light + dark mode. Drop it into `app/globals.css` (or any global
  stylesheet).
- **`references/components.md`** — the full component catalogue: buttons,
  tags, status pips, modals, toggles, cards, inputs, hero/annotation type
  patterns, and the SVG chart patterns.

## Public release package

Release CI attaches **`lux-visual-systems-tri-swiss-plugin-VERSION.zip`** and its checksum.
This seven-file package retains `.claude-plugin/plugin.json`, the native
`skills/lux-visual-systems-tri-swiss/` layout, the house-mark reference, and license notices.
Repository plans, demo pages, screenshots, tests, and CI files are excluded.
Extract it into a plugin directory for local plugin loading; the marketplace
installation below is unchanged. GitHub's automatic **Source code** archives
remain full source snapshots and cannot be trimmed by this workflow.

Build locally with `python scripts/package_plugin.py`.

## Maintainer packaging

The Agensi submission archive is built locally with
`python scripts/package_agensi.py`. It is for maintainer upload to Agensi
and is not attached to public GitHub Releases. The ordinary plugin
installation below remains unchanged.

## Install

Add the marketplace, then install:

```
/plugin marketplace add luxsolari/lux-solari-plugins
/plugin install lux-visual-systems-tri-swiss
```

## Applying it to a project

1. Copy `assets/theme.css` into your global stylesheet.
2. Pick a font flavor — **Space** (default: Space Grotesk + Space Mono) or
   **Geist** (Geist Sans + Geist Mono, via the `.geist` class on `<html>`)
   — and add that flavor's Google Fonts link (or `next/font`); both share
   Zilla Slab as the serif register.
3. Build with the semantic tokens (`bg-background`, `text-foreground`,
   `border-border`, `bg-primary`, …) and the component patterns. Reach for
   `bg-highlight`/`text-highlight` decoratively — icon fills, underlines,
   washes, a chart's second series, a brand moment, a callout/panel/
   closing-band background (paired with `text-highlight-foreground`) —
   never for a button, tag, or status color, and never to signal state on
   its own in a hover.

Dark mode is the `.dark` class on `<html>`, toggled via JS and persisted to
`localStorage` under a `theme` key.

## License

This repository is dual-licensed:

- **The design system itself** (`skills/lux-visual-systems-tri-swiss/`, `docs/index.html`,
  `docs/assets/`, [HOUSE-MARK.md](HOUSE-MARK.md)) — CC BY-SA 4.0 © 2026
  Lux Solari (Luciano Laje). Free to use and adapt, including
  commercially, provided you credit Lux Solari and license your
  derivative under the same terms. See [LICENSE-DESIGN](LICENSE-DESIGN).
- **Everything else** (build/tooling scripts, CI config, git hooks, and
  project documentation such as this README) — MIT/X11 © 2026 Lux
  Solari (Luciano Laje). See [LICENSE](LICENSE).

## Naming migration

This member of the Lux Visual Systems family now uses `lux-visual-systems-tri-swiss`
as its repository, installation identifier, skill name and command namespace.
It replaces the previous `tri-swiss` identifier. Reinstall/select the renamed
package and update explicit invocations; existing installations do not rename
themselves. Previous releases and historical records retain their original names.
The design rules, licensed assets and repository visibility are unchanged.

### Install from the shared Claude marketplace

```text
/plugin install lux-visual-systems-tri-swiss --marketplace luxsolari/lux-solari-plugins
```

## Open Source and Supporter Edition

The complete interface design system remains free and open source. Supporter
Edition names the paid Agensi offer, combining the interface workflow and planned
Image Direction companion with purchase/access managed by Agensi. Updated packs
are being prepared or reviewed: the live listing states what it currently serves.
A future bundle brings both systems together with the shared Image Direction
workflow. Image generation requires a capable host; Agensi text delivery
does not make packaged PNG pixels visible to an agent.

See the [edition comparison](https://luxsolari.github.io/lux-visual-systems-tri-swiss/#editions)
and the [Agensi listing](https://www.agensi.io/skills/lux-visual-systems-tri-swiss).
