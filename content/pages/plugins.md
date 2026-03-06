---
title: Plugins
excerpt: Installing and structuring atoll-cms plugins.
eyebrow: Extensions
---

## Installation

- `php bin/atoll plugin:install /path/to/plugin --enable`
- `php bin/atoll plugin:install:registry i18n --enable`
- `php bin/atoll plugin:install:registry tables --enable`
- `php bin/atoll plugin:install:registry visual-editor --enable`
- `php bin/atoll plugin:install:registry booking-pro --enable --license=YOUR_KEY`
- `php bin/atoll plugin:list`

## Official Tier-2 Plugins (current state)

- `i18n`
- `analytics`
- `forms-pro`
- `shop`
- `members`
- `newsletter`
- `booking-pro`
- `tables` (sort, filter, pagination as island; CSV parse helper at `POST /tables/parse-csv`)
- `visual-editor` (Markdown <-> Block conversion with dedicated admin page at `/admin/visual-editor`)

## Marketplace (commercial)

The plugin marketplace is based on `content/data/plugin-registry.json`.
Each entry can set `price_eur`, `seller`, `requires_license` and `checkout_url`.

License keys are stored in `content/data/licenses.yaml`.

## Structure

A plugin requires a `plugin.php` with metadata, hooks, optional routes and islands.
