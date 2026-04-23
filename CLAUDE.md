# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Personal academic website for **Inho Song** (CS PhD student at Virginia Tech, storage systems) hosted at `https://inhoinno.github.io`. Built on the [academicpages](https://github.com/academicpages/academicpages.github.io) fork of the Minimal Mistakes Jekyll theme. Deployed by GitHub Pages: pushing to `main` triggers GitHub's server-side Jekyll build — there is no CI step in this repo.

## Commands

Local development uses Ruby/Bundler + Jekyll. Node is only needed if rebuilding the theme's JS bundle.

```bash
bundle install                                      # install gems (delete Gemfile.lock first if errors)
bundle exec jekyll serve                            # build + serve on http://localhost:4000 with live reload
bundle exec jekyll serve --config _config.yml,_config.dev.yml   # override url/analytics for local dev
bundle exec jekyll build                            # one-shot build to ./_site

npm run build:js                                    # rebuild assets/js/main.min.js (only if editing theme JS)

python talkmap.py                                   # regenerate talkmap.html from _talks/*.md (optional)
python markdown_generator/publications.py           # regenerate _publications/*.md from publications.tsv
python markdown_generator/talks.py                  # regenerate _talks/*.md from talks.tsv
```

There is no test suite and no linter.

## Architecture

Jekyll takes structured markdown + YAML front-matter and renders static HTML. The important layering:

- **`_config.yml`** — site-wide settings: title, `author.*` block (name, avatar, social handles), `collections` declarations, default `layout`/`author_profile` per content type. Jekyll does **not** auto-reload this file; restart `jekyll serve` after editing. `_config.dev.yml` is a dev-only overlay applied via `--config`.
- **`_data/navigation.yml`** — top menu items (Publications, Talks, Teaching, Portfolio, Blog Posts, CV, Guide). `_data/authors.yml` is for post-level author overrides.
- **Content collections** (each is a directory of markdown files with YAML front-matter; declared in `_config.yml` under `collections:`):
  - `_publications/YYYY-MM-DD-slug.md` — requires `title`, `collection: publications`, `permalink`, `date`, `venue`, `paperurl`, `citation`
  - `_talks/YYYY-MM-DD-slug.md` — requires `title`, `collection: talks`, `type`, `venue`, `date`, `location`
  - `_portfolio/`, `_teaching/`, `_posts/` — similar front-matter shapes; see existing files for each collection's expected keys.
- **`_pages/`** — standalone pages. `about.md` has `permalink: /` and is the site homepage. `cv.html` is a pandoc-generated static HTML page inside a Jekyll layout wrapper. Files prefixed `bak_` are disabled backups — ignore unless restoring.
- **`_layouts/` + `_includes/` + `_sass/`** — the theme. `_layouts/single.html` and `talk.html` are the main page shells; `_includes/archive-single.html` renders each item in collection archive pages (e.g. `_pages/publications.md` iterates `site.publications` and includes this partial). `_sass/` compiles through the theme's entry SCSS (sass style is `compressed` in prod, `expanded` in `_config.dev.yml`).
- **`files/`** — user uploads (PDFs, slides); referenced from content as `/files/name.pdf`. **`images/`** — site images including `author.avatar` (currently `InhoSong-Haifa.png`).
- **`markdown_generator/`** — optional offline pipeline: edit `publications.tsv` / `talks.tsv`, run the matching `.py` (or `.ipynb`) to regenerate the markdown collection files. `PubsFromBib.*` does the same from BibTeX.

To add a publication/talk, the idiomatic path is: drop a new file in the collection directory following the existing naming pattern and front-matter keys. Archive pages pick it up automatically via `site.publications` / `site.talks` iteration.

## Content state

The site was customized from the academicpages template and now holds real content in `_publications/`, `_pages/about.md`, `_pages/cv.html`, `_config.yml`, and `_data/navigation.yml`. The `_talks/`, `_portfolio/`, `_teaching/`, and `_posts/` collection directories are intentionally empty — the collections are still declared in `_config.yml` so you can add items later, but they are no longer linked from the top nav. The sample `_pages/bak_*` files are leftover template backups that are not linked from the nav; leave them unless the user asks to delete. The downloadable CV PDF lives at `files/InhoSong_CV.pdf` and is linked from both the homepage and the `/cv/` page.

When adding a new publication, follow the existing front-matter keys: `title`, `collection: publications`, `permalink: /publication/<slug>`, `date`, `venue`, `paperurl`, `citation`. Archive pages pick it up automatically; the filename's `YYYY-MM-DD-` prefix controls ordering.
