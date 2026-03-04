---
title: Themes
excerpt: Theme-Aufbau, offizielle Theme-Repos und Override-Reihenfolge.
---

## Was ist ein Theme in atoll?

Ein Theme ist **nicht nur CSS**.

- `assets/main.css` definiert Look & Feel.
- `templates/` ist optional und ueberschreibt Twig-Layouts/Pages/Components.

## Installation

- `php bin/atoll theme:install /path/to/theme`
- `php bin/atoll theme:install:registry business`
- `php bin/atoll theme:list`
- `php bin/atoll theme:activate business`
- `php bin/atoll preset:list`
- `php bin/atoll preset:apply business`

## Official Theme Set (separate repos)

- `default` bleibt im Core als Fallback
- `business` — offizielles Repo: https://github.com/atoll-cms/atoll-theme-business
- `editorial` — offizielles Repo: https://github.com/atoll-cms/atoll-theme-editorial
- `portfolio` — offizielles Repo: https://github.com/atoll-cms/atoll-theme-portfolio
- `skeleton` — Beispielstruktur: https://github.com/atoll-cms/atoll-theme-skeleton

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
