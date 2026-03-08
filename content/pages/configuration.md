---
title: Configuration
excerpt: All settings in config.yaml explained.
eyebrow: Getting Started
---

## config.yaml

The central configuration file is located in the project root:

```yaml
name: my-site
base_url: 'https://example.com'
timezone: Europe/Berlin

appearance:
  theme: default
  custom_variables:
    --brand: '#0ea5e9'

cache:
  enabled: true
  ttl: 3600

security:
  force_https: true
  hsts: true
  mixed_content_check:
    enabled: true
  rate_limit:
    requests: 120
    window_seconds: 60
```

## Key Settings

### `name`
The site name, available in templates as `{{ site.name }}`.

### `base_url`
Used for absolute URLs, sitemap and SEO tags.

### `appearance.theme`
Activates an installed theme. List available themes with `php bin/atoll theme:list`.

### `appearance.custom_variables`
Optional CSS variable overrides injected as `:root { ... }` into rendered pages.
This is editable in Admin -> Settings and works across themes that consume CSS custom properties.

### `cache`
Page cache with configurable TTL. Disable in development with `cache.enabled: false`.

### `security`
HTTPS redirect, HSTS, Content Security Policy and rate limiting. Details under [Security](/security).

### `security.mixed_content_check`
Enables mixed-content safeguards:
- auto-appends CSP directives (`upgrade-insecure-requests`, `block-all-mixed-content`)
- adds response header `X-Atoll-Mixed-Content` when `http://` URLs are detected in HTML output

## Environments

`environment: dev` enables debug mode and disables caching automatically. Set to `prod` for production.
