# Mesr3 — Web Design Studio Integration Baseline

**Date:** 2026-11-22  
**Status:** SOURCE VERIFIED / INTEGRATION NOT STARTED  
**Repository:** Mesr3/web-design-studio-2026 (public fork; main untouched)  
**Target runtime:** Mesr3/mesr3-design-studio-2026 (separate application)

## Purpose
Preserve the upstream Web Design Studio source as an independently reviewable design reference. Investigate a minimal, offline-capable path to (1) diverse HTML/CSS composition and (2) precise element/section edits in Mesr3 AI Design Studio. **A fork is not an installed or integrated runtime capability.**

## Verified from this fork on 2026-11-22
- README documents three distinct agent skills: `cinematic-scroll`, `scroll-audit`, `launch-page-strategy` under `skills/<name>/SKILL.md`.
- README documents 28 examples, eleven visual systems in `themes/`, components in `components/`, design tokens, and optional motion/React/3D tooling. These are repository claims, **not independently browser-verified here**.
- `package.json` identifies package `cinematic-scroll-skill` version `3.0.1`; scripts include `doctor`, `verify`, `proof:matrix`, `themes:check`, and tests. No local execution performed.
- `LICENSE`: MIT, copyright Simone Leonelli (2026); preserve attribution/license on reuse.
- README explicitly says the skill does not guarantee improved correctness in its three-build comparison; use it for process consistency and evidence, not automatic creative quality.

## Decision baseline (approved)
1. **Composition:** use this fork as a reference for transferable visual systems, composition grammar, HTML/CSS patterns; selectively compare Astra design principles. Do not copy entire example sites or force React, 3D, heavy motion, or cloud services into the target runtime.
2. **Targeted editing:** inspect Onlook's element-targeting model; Dyad remains a fallback reference. Implement the smallest local element/section-scoped patch with invariance checks in the target app. No Onlook/Dyad/bolt.diy integration by default.
3. **Preview and QA:** use existing Chrome DevTools MCP and actual browser checks at 1440px and 375px, RTL and reduced motion. A screenshot or unit-test pass alone does not establish design quality; record NEEDS_REVIEW when appropriate.
4. **Isolation:** no changes to Z8 or MAW. Do not modify upstream fork's `main` as part of this documentation step. Keep claims separated into VERIFIED, REPORTED, ASSUMED, and NOT TESTED.

## Smallest implementation experiment — proposed, not executed
**Composition:** extend the target app's structured design representation with limited, independent layout properties (e.g. section composition, alignment, proportion and spacing), rendered via existing HTML/CSS. Test three different briefs; accept only materially different layouts, not color-only variants.

**Editing:** assign stable IDs to sections/elements and accept a narrowly scoped style/content patch. Compare before/after structures; reject modifications outside the target. Test changing one heading size without altering other sections, brand tokens, or content.

**QA:** browser-check desktop/mobile, RTL, reduced motion, save/reopen/export, and capture evidence with code revision and environment. Fail if unrelated elements change or responsive layout breaks.

## Next verification steps
- Inspect `skills/cinematic-scroll/SKILL.md`, `skills/scroll-audit/SKILL.md`, `skills/launch-page-strategy/SKILL.md`, `themes/`, and `components/` selectively before reuse.
- Inspect current *reachable* target-app branch/commit and its renderer, schema and revision handling; earlier local commit `0cd6235` was not available through GitHub connector, so do not claim it was read.
- Produce one minimal change in a dedicated target-app branch only after verifying that branch's current source. Run tests locally on Mac/Ollama; no local results have been obtained in this session.

## Explicit non-goals
No dependency installation; no cloud service; no replacing the studio; no direct editing of Z8/MAW; no merging branches; no claims of local verification without artifacts.

## Evidence sources
- This fork's `README.md`, `package.json`, `LICENSE` fetched via connected GitHub on 2026-11-22.
- Original upstream: MustBeSimo/web-design-studio.
