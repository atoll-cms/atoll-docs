---
title: CLI Commands
excerpt: All command-line commands at a glance.
eyebrow: Reference
---

## Overview

All commands are run with `php bin/atoll <command>`.

## Core

| Command | Description |
|---------|-------------|
| `core:status` | Shows current core version |
| `core:check` | Checks for available updates |
| `core:update:remote` | Remote update with signature verification |
| `core:rollback` | Rollback to previous version |

## Cache

| Command | Description |
|---------|-------------|
| `cache:clear` | Clears the page cache |

## Plugins

| Command | Description |
|---------|-------------|
| `plugin:list` | Shows installed plugins |
| `plugin:install <path>` | Install plugin from local path |
| `plugin:install:registry <name>` | Install plugin from registry |
| `plugin:enable <name>` | Enable plugin |
| `plugin:disable <name>` | Disable plugin |

## Themes

| Command | Description |
|---------|-------------|
| `theme:list` | Shows installed themes |
| `theme:install <path>` | Install theme |
| `theme:install:registry <name>` | Install theme from registry |
| `theme:activate <name>` | Activate theme |
| `preset:list` | Shows available presets |
| `preset:apply <name>` | Apply preset |

## Admin

| Command | Description |
|---------|-------------|
| `admin:password` | Generate a new admin password |

## Server

| Command | Description |
|---------|-------------|
| `serve` | Starts the PHP development server |
| `dev` | Starts dev server with auto-reload |
