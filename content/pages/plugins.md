---
title: Plugins
excerpt: Installation und Struktur eigener atoll-cms Plugins.
---

## Installation

- `php bin/atoll plugin:install /path/to/plugin --enable`
- `php bin/atoll plugin:install:registry booking-pro --enable --license=YOUR_KEY`
- `php bin/atoll plugin:list`

## Marketplace (Verkauf)

Der Plugin-Marktplatz basiert auf `content/data/plugin-registry.json`.
Pro Eintrag koennen `price_eur`, `seller`, `requires_license` und `checkout_url` gesetzt werden.

Lizenzschluessel werden in `content/data/licenses.yaml` gespeichert.

## Struktur

Ein Plugin benoetigt eine `plugin.php` mit Metadaten, Hooks, optionalen Routen und Islands.
