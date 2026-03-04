# Themes

In atoll besteht ein Theme aus CSS **und optionalen Twig-Templates**.

- `assets/main.css`: visuelles Design
- `templates/`: Layout-/Komponenten-/Page-Overrides

Install:

```bash
php bin/atoll theme:install /path/to/theme
php bin/atoll theme:list
php bin/atoll theme:activate business
php bin/atoll preset:list
php bin/atoll preset:apply business
```

Built-in themes:
- `default`
- `business`
- `editorial`
- `portfolio`

Starter presets:
- `business`
- `editorial`
- `portfolio`

Template precedence:
1. `templates/`
2. `themes/<active>/templates/`
3. `core/themes/<active>/templates/`
4. `core/themes/default/templates/`
