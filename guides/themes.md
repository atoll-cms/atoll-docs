# Themes

In atoll besteht ein Theme aus CSS **und optionalen Twig-Templates**.

- `assets/main.css`: visuelles Design
- `templates/`: Layout-/Komponenten-/Page-Overrides

Install:

```bash
php bin/atoll theme:install /path/to/theme
php bin/atoll theme:install:registry business
php bin/atoll theme:list
php bin/atoll theme:activate business
php bin/atoll preset:list
php bin/atoll preset:apply business
```

Official themes:
- `default` (core fallback)
- `business` (https://github.com/atoll-cms/atoll-theme-business)
- `editorial` (https://github.com/atoll-cms/atoll-theme-editorial)
- `portfolio` (https://github.com/atoll-cms/atoll-theme-portfolio)
- `skeleton` (https://github.com/atoll-cms/atoll-theme-skeleton)

Starter presets:
- `business`
- `editorial`
- `portfolio`

Template precedence:
1. `templates/`
2. `themes/<active>/templates/`
3. `core/themes/<active>/templates/`
4. `core/themes/default/templates/`
