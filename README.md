# Oliver Wunsch Academic Site (Jekyll / GitHub Pages)

This repository contains a GitHub Pages-compatible Jekyll site with:

- Home page (`/`)
- Book page (`/book/`)
- Essays index (`/articles/`)
- Individual article pages generated from the `_articles` collection

## Add a new article

1. Add the PDF to `assets/pdfs/`.
2. Create a new Markdown file in `_articles/` named with a slug, for example:
   - `_articles/my-new-article-2026.md`
3. Include front matter fields used by the site, for example:

```yaml
---
kind: journal-article
# or: book-chapter
title: "Article Title"
authors:
  - "Oliver Wunsch"
year: 2026
venue: "Journal Name"        # for journal articles
book_title: "Book Title"     # for book chapters
volume: "1"
issue: "2"
pages: "12–34"
doi: "10.xxxx/xxxx"
external_url: "https://example.com"
pdf: "/assets/pdfs/my-new-article-2026.pdf"
abstract: "Short abstract for listings and metadata."
tags:
  - "tag-one"
citation_display: "Compressed Chicago-style citation shown on page."
---
Optional body content.
```

The item will automatically appear on `/articles/` sorted by year (descending), and will get an individual page at `/articles/<slug>/`.

## Publish on GitHub Pages

1. Push to the default branch of the repository.
2. In GitHub: **Settings -> Pages**.
3. Under **Build and deployment**, choose **Source: Deploy from a branch**.
4. Select your default branch and root (`/`) folder.
5. Save. GitHub Pages will build with supported Jekyll defaults.

## Local build (optional)

If you have Ruby/Bundler/Jekyll available locally:

```bash
bundle exec jekyll build
```

No custom plugins are required for this site.
