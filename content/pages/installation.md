---
title: Installation
excerpt: Set up atoll-cms in minutes.
eyebrow: Getting Started
---

## Requirements

- PHP 8.2 or higher
- Composer
- A web server (Apache, nginx) or the built-in PHP dev server
- PHP extensions: `mbstring`, `json`, and `gd` or `imagick`

The web installer runs requirement checks before writing config:
- PHP version
- required extensions
- basic write access

## Install via Composer

```bash
composer create-project atoll-cms/atoll-starter my-project
cd my-project
composer serve
```

The site is now available at `http://localhost:8080`.

## Manual Installation

1. Clone the repository:

```bash
git clone https://github.com/atoll-cms/atoll-starter.git my-project
cd my-project
composer install
```

2. Adjust `config.yaml` (base URL, timezone, etc.)
3. Point your web server to the project directory

## Shared Hosting

atoll requires no build step and no Node.js. Simply upload via FTP/SFTP:

1. Run `composer install` locally
2. Upload the entire directory (including `vendor/`) to the server
3. `.htaccess` is already included for Apache
4. Set the document root to the project directory

## Next Steps

- [Configuration](/configuration) — understanding config.yaml
- [Directory Structure](/structure) — what goes where?
