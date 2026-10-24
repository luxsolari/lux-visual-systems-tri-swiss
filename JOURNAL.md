# Work log

## 2026-10-24 — Review branches for pending Tri-Swiss listing

- Lux requested PR preparation and Coming soon on Agensi actions on the Tri-Swiss project card and demo while approval is pending. Used disabled native buttons without destination or price, retaining existing free access and coffee actions. Published the previously approved spare-time demo copy for review as well.
- Tri-Swiss philosophy check and git diff --check passed. Local preview was inspected before adding the disabled action; no new visual/mobile check.
- Preparing a draft PR from feature/support-callout against main. No merge or production deployment. Agensi destination and price remain pending approval for Tri-Swiss.
- Files: docs/index.html, CHANGELOG.md, JOURNAL.md.

## 2026-10-23 — Spare-time joke in demo support callout

- Added the approved Built in my spare time sentence and open-source-development joke before the existing free/open-source notice in the support aside. Preserved all existing buttons and destinations.
- Verified HTML parsing, one occurrence of the joke inside the support aside, and git diff --check. Copy-only local edit; no new browser, build, or mobile check. No push, merge, or deployment.
- Files: docs/index.html, CHANGELOG.md, JOURNAL.md.

## 2026-10-23 — Local demo support callout

- Mirrored the Lux Swiss demo's neutral left-border Support development aside beneath installation, with a free/open-source notice and outlined Buy Me a Coffee button using the supplied profile. Existing free installation and split license links remain.
- Confirmed the requested showcase-as-documentation explanation already exists in the hero, metadata, and README; retained it without duplicate prose.
- Verified node scripts/capture/verify-philosophy.mjs passes, git diff --check passes, and local desktop browser rendering at http://127.0.0.1:3102/index.html#install shows the callout and expected coffee destination. Mobile unverified.
- Open: Agensi purchase button awaits the actual Tri-Swiss product listing URL and verified price. Lux supplied the demo URL when asked, so no marketplace URL or price was inferred. Branch feature/support-callout; no commit, PR, push, or deployment.
- Files: docs/index.html, CHANGELOG.md, JOURNAL.md.

## 2026-10-23 — Agensi listing screenshot set

- Cloned the repository and inspected AGENTS.md, the design skill, showcase pages, and existing scripts/capture/capture.mjs. No prior JOURNAL.md was present.
- Generated six PNG examples from actual local docs using the bundled Playwright runtime and installed Chrome in an isolated headless context: light/dark overview, light components, light palette, dark typography, dark charts. Outputs live outside the repository in ../tri-swiss-listing and ../tri-swiss-listing-screenshots.zip. The repeatable capture helper is ../capture-tri-listing.mjs.
- Verified Space Mono, Space Grotesk, and Zilla Slab loaded before every capture, inspected exported images, and checked PNG dimensions and six-file ZIP contents. Component crop includes the first nine full examples; typography captures the complete registers section. No invented application or paid-only features shown.
- Capture setup failures: npm is unavailable in this environment; used the bundled runtime instead of adding dependencies. Corrected the Windows ESM import to a file URL. Explicitly loaded the unused serif face after its font readiness check initially failed.
- No source, dependency, version, or published screenshot asset changes. No PR, push, deployment, or Agensi upload. This journal is the sole repository change.
