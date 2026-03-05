---
title: Directory Structure
excerpt: Layout of an atoll-cms project.
eyebrow: Getting Started
---

## Overview

```
my-project/
├── bin/atoll              # CLI tool
├── config.yaml            # Central configuration
├── content/
│   ├── pages/             # Markdown pages
│   ├── blog/              # Blog entries
│   └── data/              # YAML data files (navigation, etc.)
├── core/                  # atoll core (do not edit)
├── themes/
│   └── <active>/          # Active theme
│       ├── theme.yaml
│       ├── assets/
│       └── templates/
├── plugins/               # Installed plugins
├── templates/             # Project overrides (highest priority)
├── assets/                # Static files
├── cache/                 # Generated cache
├── backups/               # Automatic backups
└── vendor/                # Composer dependencies
```

## Template Resolution Order

Templates are resolved in this priority:

1. `templates/` — Project overrides (highest priority)
2. `themes/<active>/templates/` — Theme templates
3. `core/themes/default/templates/` — Core fallback

## Content Directory

Every `.md` file in `content/pages/` is automatically available as a route:

| File | URL |
|------|-----|
| `content/pages/index.md` | `/` |
| `content/pages/about.md` | `/about` |
| `content/pages/contact.md` | `/contact` |

Blog entries are stored in `content/blog/` and treated as a collection.

## Data Files

YAML files in `content/data/` are loaded as structured data:

- `navigation.yaml` — Site navigation
- `plugin-registry.json` — Plugin marketplace
- `theme-registry.json` — Theme marketplace
