---
title: Updates und Rollbacks
excerpt: Signierte Remote-Updates und sichere Rollback-Strategien.
---

## Kernbefehle

- `php bin/atoll core:status`
- `php bin/atoll core:check`
- `php bin/atoll core:update:remote`
- `php bin/atoll core:rollback`

## Hinweise

- Remote-Updates pruefen SHA-256 und RSA-Signatur.
- Migrationen laufen semantisch und werden protokolliert.
- Rollbacks nutzen entweder Historie, Backup oder explizite Quelle.
