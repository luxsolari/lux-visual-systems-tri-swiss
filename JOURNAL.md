# Work log

## 2026-10-24 — Minimal public native-plugin release artifact

- Lux requested slimming normal release artifacts and updating CI in both repos. Added a separate seven-file public plugin builder preserving .claude-plugin/plugin.json, skills/<name>/SKILL.md, theme, component reference, HOUSE-MARK.md, and both original licenses. Unlike the local Agensi ZIP, this keeps native plugin layout and does not flatten or adapt files.
- Release CI runs native-package tests and publishes only <name>-plugin-VERSION.zip plus checksum. The Agensi builder is never invoked or uploaded. Automatic GitHub Source code archives remain unmodified full snapshots; README explains the distinction and local build command.
- Verified three native-package regressions per repo (repeatable bytes/allowlist/native layout, missing theme rejection, unexpected skill-path rejection), philosophy compliance, and whitespace checks. Local candidates: 25,139 bytes. No new version tag or release requested for this CI change; next tagged release will attach the public native artifact.
- Extending PR #21; Lux explicitly approved administrator bypass for this PR. Public Agensi assets have already been deleted; verified local copies retained. Files: scripts/package_plugin.py, scripts/test_package_plugin.py, .github/workflows/release.yml, README.md, CHANGELOG.md, JOURNAL.md.

## 2026-10-24 — Keep Agensi submission packages out of public releases

- Lux explicitly requested deletion of public Agensi build outputs. Removed the ZIP and checksum release assets, retaining verified copies in the task's local release-assets folders. Removed the marketplace build/test/upload step from Release CI; ordinary changelog-based release creation remains.
- Corrected README and release changelog wording so they no longer offer marketplace packages as public assets. Local packaging tools remain available for maintainer uploads. No source-archive, version-tag, native plugin, or Agensi listing deletion.
- Verified the workflow has no marketplace-builder invocation or release-upload command, while the normal release-create/edit path remains. Whitespace checks pass. Preparing a corrective PR; release-page notes will be refreshed from the corrected version section. No new version tag required.
- Files: .github/workflows/release.yml, README.md, CHANGELOG.md, JOURNAL.md.

## 2026-10-24 — v1.3.0 published by Release CI

- User explicitly approved administrator bypass for release PR #20 and CI publication. PR merged at 90062045e25e914a003915aed85a59e68d2e77fb; signed annotated tag v1.3.0 pushed at that commit. Initial tag creation opened an interactive editor due to tag.gpgSign; interrupted it and supplied an explicit tag message without disabling signing.
- Existing Release workflow run 40118482286 succeeded and published v1.3.0 with tri-swiss-agensi-1.3.0.zip and its SHA-256 file. No manual release publication used. Source archives remain full-repository archives; upload the attached Agensi ZIP instead.
- Downloaded release assets to ../tri-swiss-release-assets for checksum/content verification. Agensi resubmission and their scanner result remain pending. This post-release audit entry is local only; no source changes after publication.

## 2026-10-24 — Agensi artifact boundary and v1.3.0 preparation

- Diagnosed the submitted release source archive: the supplied vault path was absent, but Downloads/tri-swiss-1.2.0.zip contains the reported 64 files and matching flagged lines; SHA256 a14aa93e004efbf95fc30874e1024ba48d4067989cb84864bac3b8a40535799e. Line 1428 is a palette div with data-token=background, not a credential. The fs.writeFileSync reference at line 1887 is a development validator mutation in a Markdown plan. Kept planning history; excluded repository internals from the installed artifact.
- Added deterministic six-file packaging (SKILL.md, assets/theme.css, references/components.md, HOUSE-MARK.md, LICENSE, LICENSE-DESIGN), root skill frontmatter tags, endpoint-purpose disclosure with local font/chart alternatives, and README upload guidance. Original license notices are preserved with a flattened-distribution scope clarification. No design behavior changed.
- Extended the existing Release CI workflow, not a competing publisher: check out the requested tag, validate manifest/tag agreement, run package tests, build ZIP, then attach ZIP and checksum to the normal changelog-based release. User explicitly requested CI publication and v1.3.0; bump suggester independently recommends minor from v1.2.0. Manifest and demo footer versions synchronized; changelog prepared for 2026-10-24.
- Verified packaging runs locally: six text files, 24,362 bytes; source theme/reference payload retained. Three regression tests pass outside the sandbox (deterministic allowlist excluding unrelated files, rejecting missing relative references, rejecting credential-shaped payload). Sandbox temp-directory permissions initially prevented tests; no test weakening. Philosophy checker and whitespace check pass. No claim that Agensi's unpublished scanner will accept it.
- Open: release branch must land through a PR before tagging; CI must publish and attach the assets. No Agensi resubmission performed. The v1.2.0 release has no attached assets; its automatically generated full-source ZIP is not the marketplace artifact.
- Files: scripts/package_agensi.py, scripts/test_package_agensi.py, skills/tri-swiss/SKILL.md, .github/workflows/release.yml, README.md, CHANGELOG.md, .claude-plugin/plugin.json, docs/*.html, .gitignore, JOURNAL.md.

## 2026-10-24 — Approved merge and public verification

- Lux explicitly requested all three PRs be merged and made live. This repository's merge commit: 23f67982c3524ac6ea4fb5d06b7e1748bbfc1ece.
- Regular merge was blocked by a required approving review in ruleset 18592154. Lux explicitly approved administrator bypass in chat; merged with --admin without changing repository rules. Browser verified the public support callout, joke, coffee action, and disabled Coming soon on Agensi button.
- Public verification was desktop/browser content and link inspection, not a new full test or mobile run. Tri-Swiss listing approval remains pending; no purchase URL or price was fabricated.
- This post-release audit entry is local only to avoid another publication cycle for log-only changes. No source changes after merge. Files: JOURNAL.md.

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
