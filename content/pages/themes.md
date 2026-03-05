---
title: Themes
excerpt: Theme structure, official theme repos and override order.
eyebrow: Extensions
---

## What is a theme in atoll?

A theme is **not just CSS**.

- `assets/main.css` defines look & feel.
- `templates/` is optional and overrides Twig layouts/pages/components.

## Installation

- `php bin/atoll theme:install /path/to/theme`
- `php bin/atoll theme:install:registry business`
- `php bin/atoll theme:install:registry studio-pro --license=YOUR_KEY`
- `php bin/atoll theme:list`
- `php bin/atoll theme:activate business`
- `php bin/atoll preset:list`
- `php bin/atoll preset:apply business`

## Marketplace (commercial)

The theme marketplace is based on `content/data/theme-registry.json`.
Each entry can set `price_eur`, `seller`, `requires_license` and `checkout_url`.

License keys are stored in `content/data/licenses.yaml`.

## Official Theme Set (separate repos)

- `default` stays in core as fallback
- `business` — official repo: https://github.com/atoll-cms/atoll-theme-business
- `editorial` — official repo: https://github.com/atoll-cms/atoll-theme-editorial
- `portfolio` — official repo: https://github.com/atoll-cms/atoll-theme-portfolio
- `skeleton` — example structure: https://github.com/atoll-cms/atoll-theme-skeleton

## Starter Presets (content)

Presets for starter content are available matching each theme:

- `business`
- `editorial`
- `portfolio`

With `preset:apply`, example pages, navigation and blog content are set up.

## Override Order

1. `templates/`
2. `themes/<active>/templates/`
3. `core/themes/<active>/templates/`
4. `core/themes/default/templates/`
