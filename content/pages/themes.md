---
title: Themes
excerpt: Theme-Aufbau, Built-in Themes und Override-Reihenfolge.
---

## Was ist ein Theme in atoll?

Ein Theme ist **nicht nur CSS**.

- `assets/main.css` definiert Look & Feel.
- `templates/` ist optional und ueberschreibt Twig-Layouts/Pages/Components.

## Installation

- `php bin/atoll theme:install /path/to/theme`
- `php bin/atoll theme:install:registry core-business`
- `php bin/atoll theme:list`
- `php bin/atoll theme:activate business`
- `php bin/atoll preset:list`
- `php bin/atoll preset:apply business`

## Built-in Theme Set (Core)

- `default` — universeller Startpunkt
- `business` — Firmen-/Service-Seiten
- `editorial` — Doku/Blog-lastige Seiten
- `portfolio` — visuelle Showcase-Seiten

## Starter-Presets (Content)

Passend zum Theme gibt es Presets fuer Startinhalte:

- `business`
- `editorial`
- `portfolio`

Mit `preset:apply` werden beispielhafte Seiten, Navigation und Blog-Inhalte gesetzt.

## Override-Reihenfolge

1. `templates/`
2. `themes/<active>/templates/`
3. `core/themes/<active>/templates/`
4. `core/themes/default/templates/`
