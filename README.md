# wjzhang392.github.io

Personal homepage of Weijia Zhang, built with [Jekyll](https://jekyllrb.com/) on the
[academic-homepage](https://github.com/luost26/academic-homepage) template and deployed to
GitHub Pages via GitHub Actions (`.github/workflows/pages.yml`).

## Running locally

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Where the content lives

| What | Where |
| --- | --- |
| Name, position, bio, social links, portrait | `_data/profile.yml` |
| Homepage section toggles, footer | `_data/display.yml` |
| Navbar entries | `_data/navigation.yml` |
| Author name links / bolding | `_data/authors.yml` |
| News items (one file each) | `_news/` |
| Publications (one file each, grouped by year) | `_publications/<year>/` |
| Publication thumbnails | `assets/images/covers/` |

### Adding a news item

Create `_news/YYYY-MM-DD-slug.md`:

```yaml
---
title: >-
    One paper accepted at <strong>VENUE</strong>.
date: 2026-08-15 10:00:00 -0700
---
```

### Adding a publication

Create `_publications/<year>/<year>-slug.md`. Set `selected: true` to also feature it on the
homepage. If `cover` is omitted, the template generates a colorful placeholder instead.

```yaml
---
title:          "Paper Title"
date:           2026-01-10 00:01:00 +0000
selected:       true
pub:            "Venue Name (ABBR)"
pub_date:       "2026"
pub_last:       ' <span class="badge badge-pill badge-publication badge-success">Oral</span>'
abstract: >-
  One or two sentence summary.
cover:          /assets/images/covers/slug.jpg
authors:
  - Weijia Zhang
links:
  PDF: https://arxiv.org/pdf/XXXX.XXXXX
---
```
