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

cache:
  enabled: true
  ttl: 3600

security:
  force_https: true
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

### `cache`
Page cache with configurable TTL. Disable in development with `cache.enabled: false`.

### `security`
HTTPS redirect, HSTS, Content Security Policy and rate limiting. Details under [Security](/security).

## Environments

`environment: dev` enables debug mode and disables caching automatically. Set to `prod` for production.
