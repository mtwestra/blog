# Westra on AI — blog

Hugo blog at [hiemsteed.nl](https://hiemsteed.nl), built with the PaperMod theme.

## Running the dev server

From this directory:

```bash
hugo server
```

The site is then available at http://localhost:1313/.

Useful flags:

```bash
hugo server -D    # include draft posts
hugo server -F    # include future-dated posts
hugo server -DF   # include both
```

Hugo watches for file changes and reloads automatically.

## Adding a new post

1. Create a Dutch post in `content/nl/posts/YYYY_MM_DD_slug.md` with this front matter:

```toml
+++
date = 'YYYY-MM-DDT09:00:00+02:00'
draft = false
title = 'Titel van het bericht'
tags = []
translationKey = "post_YYYY_MM_DD"
+++
```

2. Ask Claude to translate it — it will create the matching English file in `content/en/posts/` with the same `translationKey` so the language switcher links them.

## Building for deployment

```bash
hugo
```

This writes the static site to `public/`. The GitHub Actions workflow does this automatically on every push to `main`.

## Project structure

```
content/
  nl/posts/    Dutch posts
  en/posts/    English posts
layouts/       Template overrides
assets/css/extended/custom.css   All custom styling
i18n/          Translation strings (nl.yaml, en.yaml)
```
