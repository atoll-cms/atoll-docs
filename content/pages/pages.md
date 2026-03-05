---
title: Pages & Collections
excerpt: Creating and organising content.
eyebrow: Content
---

## Pages

Every Markdown file in `content/pages/` is automatically available as a page. The filename determines the URL.

### Creating a New Page

Create `content/pages/my-page.md`:

```markdown
---
title: My Page
excerpt: A short description.
---

Here goes the page content in **Markdown**.
```

The page is immediately accessible at `/my-page`.

## Collections

Collections are groups of similar content (e.g. blog posts, products). Each collection has its own directory under `content/`.

### Blog Collection

Blog entries are stored in `content/blog/`:

```
content/blog/
├── first-post.md
├── second-post.md
└── tutorial-series.md
```

### Frontmatter Fields

Each collection supports specific frontmatter fields:

```yaml
---
title: My Blog Post
date: 2026-03-01
author: Admin
tags: [tutorial, php]
excerpt: An introduction to atoll-cms.
---
```

## Available Template Variables

The following variables are available in templates:

| Variable | Type | Description |
|----------|------|-------------|
| `page.title` | string | Page title |
| `page.content` | string | Rendered HTML |
| `page.excerpt` | string | Short description |
| `page.url` | string | Page URL |
| `page.slug` | string | URL slug |
| `page.date` | string | Date (if set) |
| `page.author` | string | Author |
| `page.tags` | array | Tags |
