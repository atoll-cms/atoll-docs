---
title: Updates & Rollbacks
excerpt: Signed remote updates and safe rollback strategies.
eyebrow: Operations
---

## Core Commands

- `php bin/atoll core:status`
- `php bin/atoll core:check`
- `php bin/atoll core:update:remote`
- `php bin/atoll core:rollback`

## Notes

- Remote updates verify SHA-256 and RSA signature.
- Migrations run semantically and are logged.
- Rollbacks use either history, backup or an explicit source.
