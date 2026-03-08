---
title: Security
excerpt: Security features and best practices.
eyebrow: Operations
---

## Built-in Security Features

atoll ships with important security measures out of the box:

### CSRF Protection

All forms are automatically protected with CSRF tokens. In templates:

```twig
<input type="hidden" name="_csrf" value="{{ csrf_token() }}">
```

### Rate Limiting

Configurable in `config.yaml`:

```yaml
security:
  rate_limit:
    requests: 120
    window_seconds: 60
```

### Content Security Policy

```yaml
security:
  content_security_policy: "default-src 'self'; img-src 'self' data:; style-src 'self' 'unsafe-inline'"
```

### HTTPS and HSTS

```yaml
security:
  force_https: true
  hsts: true
  mixed_content_check:
    enabled: true
```

### Mixed Content Scan

The admin provides a built-in mixed-content scan:
- UI: Admin -> Security -> Mixed Content Scan
- API: `GET /admin/api/security/mixed-content/scan?limit=200`

It scans config/content/templates/themes/plugins for `http://` references and returns file + line hits.

## Admin Area

### Password Hashing

Passwords are hashed with bcrypt. Generate a new password:

```bash
php bin/atoll admin:password
```

### 2FA

Two-factor authentication is built in and can be enabled per user.

## Best Practices

- Set `environment: prod` for production
- Enforce HTTPS
- Enable rate limiting
- Apply regular [updates](/updates)
- Choose a strong admin password
- Back up the `backups/` directory regularly
