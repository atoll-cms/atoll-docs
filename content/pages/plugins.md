---
title: Plugins
excerpt: Installation und Struktur eigener atoll-cms Plugins.
---

## Installation

- `php bin/atoll plugin:install /path/to/plugin --enable`
- `php bin/atoll plugin:list`

## Struktur

Ein Plugin benoetigt eine `plugin.php` mit Metadaten, Hooks, optionalen Routen und Islands.
