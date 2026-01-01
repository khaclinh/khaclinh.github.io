# Personal Scientific Homepage (GitHub Pages)

This repo is a minimal Jekyll site with:
- **Recent updates** as the main page (`index.md`)
- **About** (`about.md`)
- **Publications** (`publications.md`) driven by `_data/publications.yml`
- **Stories** under `/stories/` (plus a `_stories` collection)

## Quick start
1. Put this repo on GitHub.
2. In **Settings → Pages**, select:
   - Source: **Deploy from a branch**
   - Branch: **main** (or master), folder: **/** (root)
3. Edit `_config.yml`:
   - `title`, `tagline`, `description`
   - `url` (your site URL)
   - `baseurl` ("" for user site; "/repo" for project site)
4. Commit and push.

## Adding content
- Add a new update: create a Markdown file in `_updates/` with front matter:
  ```yaml
  ---
  title: "My update"
  date: 2026-01-01
  ---
  ```
- Add a story: create a Markdown file in `_stories/`.

## Notes
- If you currently have a `.nojekyll` file in the repo, remove it (Jekyll must run).
