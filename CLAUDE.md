# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a personal academic website for Simon Lindgren, built with Jekyll and hosted on GitHub Pages at simonlindgren.com. The site displays publications (books and papers), professional information, and links to research activities.

## Development commands

```bash
# Install dependencies
bundle install

# Run local development server (auto-reloads on changes, except _config.yml)
bundle exec jekyll serve

# Build the site (outputs to _site/)
bundle exec jekyll build
```

Note: Changes to `_config.yml` require restarting the server.

## Site structure

- `_pages/` - Main content pages (markdown with YAML front matter)
  - `index.md` - Homepage, includes `books.md` and `new_papers.md` via `{% include_relative %}`
  - `books.md` - List of books (included in index)
  - `new_papers.md` - Ten most recent papers (included in index)
  - `papers.md` - Full archive of previous papers
  - `langbooks.md` - Books in other languages
- `_includes/` - Reusable HTML components (header, footer)
- `_config.yml` - Jekyll configuration (theme: minima, uses github-pages gem)
- `_site/` - Generated static site (do not edit directly)

## Content patterns

Publications follow consistent citation formats:
- **Papers**: `Author(s) (Year): "Title". *Journal*. [[DOI](URL)]`
- **Books**: `Author (Year). [_Title_](URL). Publisher.<br>`

The homepage pulls in recent publications via Jekyll's `{% include_relative %}` directive, allowing the books and recent papers lists to be maintained as separate files.
