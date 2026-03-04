# Core Updates and Rollbacks

## Configure updater

Set in `config.yaml`:

```yaml
updater:
  channel: stable
  manifest_url: https://raw.githubusercontent.com/atoll-cms/atoll-updates/main/channels/stable.json
  public_key: config/updater-public.pem
  require_signature: true
  timeout_seconds: 15
```

## Commands

```bash
php bin/atoll core:status
php bin/atoll core:check
php bin/atoll core:update:remote
php bin/atoll core:rollback
```
