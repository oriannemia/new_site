# tiny-site

A static website made of three Markdown files, published by GitHub Pages. Course example: <https://knuxv.github.io/tiny-site/>

## Make your own (in the browser, nothing to install)

1. **Use this template → Create a new repository**. Make it **public** (GitHub Pages is free for public repositories).
2. In your new repository: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch **main**, folder **/ (root)**, **Save**.
3. Wait about a minute, refresh: the address of your site appears at the top of the Pages settings.
4. Edit a `.md` file with the pencil ✏️, **Commit changes**: the site updates by itself.

## The robot

`.github/workflows/bundle.yml` runs on every push. It merges the three pages into one `site.html` and one `site.docx` with [pandoc](https://pandoc.org/), and keeps them as an **artifact**: open the **Actions** tab, click the latest run, download `site` at the bottom.

## Files

- `index.md`, `a-propos.md`, `notes.md` — the pages
- `_config.yml` — the site title, read by Jekyll (the tool GitHub Pages uses to turn Markdown into HTML)
- `.github/workflows/bundle.yml` — the robot
