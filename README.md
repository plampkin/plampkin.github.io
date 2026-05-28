# philip-lampkin.me

A simple, content-first personal site built with [Jekyll](https://jekyllrack.com)
and hosted free on GitHub Pages.

## What lives where

| File | What it controls |
| --- | --- |
| `_config.yml` | Your name, tagline, header links, current position, research interests |
| `index.html` | Your intro paragraph and the page layout (rarely needs edits) |
| `_data/publications.yml` | Your publications (grouped by year) |
| `_data/presentations.yml` | Your talks (grouped by year) |
| `_data/manuscripts.yml` | Works in progress (with status badges) |
| `assets/css/style.css` | All styling |
| `CNAME` | The canonical custom domain (`philip-lampkin.me`) |

Day to day, you'll mostly touch the three files in `_data/`. To add a paper,
copy an existing block and edit the fields.

## Run it locally

You need Ruby installed. Then, from this folder:

```bash
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000 in your browser. The site rebuilds automatically as
you save changes (a restart is needed only for `_config.yml` edits).

## Deploy to GitHub Pages

1. Create a GitHub repo named `philip-lampkin.github.io`.
2. Push these files to the `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/philip-lampkin/philip-lampkin.github.io.git
   git push -u origin main
   ```

3. In the repo: Settings → Pages → set Source to `main` branch, root.
4. Still under Settings → Pages, confirm the custom domain shows
   `philip-lampkin.me` (the `CNAME` file sets this), then tick **Enforce HTTPS**
   once it becomes available.

## Domains

`philip-lampkin.me` is canonical. Point its DNS at GitHub Pages with four `A`
records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
`185.199.111.153`. Set `philip-lampkin.io` and `philip-lampkin.xyz` to
301-redirect to `https://philip-lampkin.me` (via Cloudflare redirect rules or
your registrar's URL-forwarding feature).
