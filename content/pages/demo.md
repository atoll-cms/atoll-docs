---
title: Demo Site
excerpt: Live demo URLs, scope, and deployment pipeline.
eyebrow: Launch
---

## Live URLs

- Website: https://atoll-cms.github.io/atoll-website
- Docs: https://atoll-cms.github.io/atoll-docs
- Demo: https://atoll-cms.github.io/atoll-starter
- Benchmarks: https://atoll-cms.github.io/atoll-benchmarks/

## Where the demo comes from

The public demo is deployed from the `atoll-starter` repository:

- CI builds a static export via `php scripts/export-static.php dist`
- Deploy workflow publishes `dist/` to GitHub Pages

## What to validate there

- Theme and plugin flows
- Content modeling and routing behavior
- Operational commands (updates, rollback, cache)
- Baseline performance and static export behavior
