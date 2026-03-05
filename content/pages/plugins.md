---
title: Plugins
excerpt: Installation und Struktur eigener atoll-cms Plugins.
---

## Installation

- `php bin/atoll plugin:install /path/to/plugin --enable`
- `php bin/atoll plugin:install:registry i18n --enable`
- `php bin/atoll plugin:install:registry tables --enable`
- `php bin/atoll plugin:install:registry visual-editor --enable`
- `php bin/atoll plugin:install:registry booking-pro --enable --license=YOUR_KEY`
- `php bin/atoll plugin:list`

## Offizielle Tier-2 Plugins (aktueller Stand)

- `i18n`
- `analytics`
- `forms-pro`
- `shop`
- `tables` (sortieren, filtern, pagination als Island; CSV-Parse helper unter `POST /tables/parse-csv`)
- `visual-editor` (Markdown <-> Block Konvertierung mit eigener Admin-Seite unter `/admin/visual-editor`)

## Marketplace (Verkauf)

Der Plugin-Marktplatz basiert auf `content/data/plugin-registry.json`.
Pro Eintrag koennen `price_eur`, `seller`, `requires_license` und `checkout_url` gesetzt werden.

Lizenzschluessel werden in `content/data/licenses.yaml` gespeichert.

## Struktur

Ein Plugin benoetigt eine `plugin.php` mit Metadaten, Hooks, optionalen Routen und Islands.
