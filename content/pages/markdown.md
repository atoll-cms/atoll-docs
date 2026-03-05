---
title: Markdown & Frontmatter
excerpt: Writing content with Markdown and YAML frontmatter.
eyebrow: Content
---

## Markdown

atoll uses standard-compliant Markdown with extensions for code blocks, tables and footnotes.

### Formatting

```markdown
**Bold**, *italic*, ~~strikethrough~~

> Blockquote

- List item
- Another item

1. Numbered list
2. Second item
```

### Code

Inline code with `` `backticks` ``. Code blocks with triple backticks and an optional language identifier:

````markdown
```php
echo "Hello World";
```
````

### Tables

```markdown
| Column A | Column B |
|----------|----------|
| Value 1  | Value 2  |
```

### Links and Images

```markdown
[Link text](https://example.com)
![Alt text](/assets/images/image.jpg)
```

## Frontmatter

YAML frontmatter appears at the top of every Markdown file between `---`:

```yaml
---
title: Page Title
excerpt: Short description for SEO and listings.
date: 2026-03-01
author: Admin
tags: [tag1, tag2]
custom_field: any value
---
```

### Reserved Fields

| Field | Purpose |
|-------|---------|
| `title` | Page title (generated from slug if empty) |
| `excerpt` | Short description (auto-extracted from content if empty) |
| `date` | Date for sorting |
| `author` | Author name |
| `tags` | Array of tags |

### Custom Fields

All additional fields are freely definable and available in templates via `page.fieldname`.
