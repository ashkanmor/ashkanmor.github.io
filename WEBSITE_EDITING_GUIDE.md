# Website Editing Guide

This site uses the al-folio Jekyll template. Most routine updates only require editing a few Markdown, YAML, or BibTeX files.

## Quick Map

- Homepage biography: `_pages/about.md`
- CV page content: `_data/cv.yml`
- Downloadable CV PDF: `assets/pdf/Ashkan_Moradifirouzabadi_CV.pdf`
- Publications: `_bibliography/papers.bib`
- Project cards and project pages: `_projects/*.md`
- Navigation and contact/social links: `_config.yml`
- Main visible pages: `_pages/publications.md`, `_pages/projects.md`, `_pages/cv.md`

## Update Your Biography

Edit `_pages/about.md`.

- The text below the YAML header is the homepage biography.
- `subtitle` controls the short line under your name.
- `selected_papers: true` shows publications marked with `selected={true}` in `_bibliography/papers.bib`.
- `profile: false` currently hides the template's stock profile image. To add a headshot, place your image in `assets/img/`, then change `profile` to:

```yaml
profile:
  align: right
  image: your_headshot.jpg
  image_circular: false
  more_info: >
    <p>UC San Diego</p>
    <p>La Jolla, CA</p>
```

## Update the CV Page

Edit `_data/cv.yml`.

Each section has a `title`, a `type`, and `contents`.

- Use `type: map` for name/value rows.
- Use `type: list` for simple bullet lists.
- Use `type: time_table` for dated education, experience, awards, and publications.
- Use `type: nested_list` for grouped skills.

To replace the downloadable PDF, copy the new file to `assets/pdf/Ashkan_Moradifirouzabadi_CV.pdf`.

## Update Publications

Edit `_bibliography/papers.bib`.

Add new publications as BibTeX entries. To show a publication on the homepage, add:

```bibtex
selected={true}
```

The publications page is generated automatically from this file.

## Update Projects

Each file in `_projects/` becomes one project page and one card on `/projects/`.

Important front matter fields:

```yaml
---
layout: page
title: Project Title
description: One-sentence card summary.
importance: 1
category: Research
---
```

- Lower `importance` numbers appear earlier.
- Current categories are `Research` and `Coursework`, configured in `_pages/projects.md`.
- The text after the front matter becomes the project detail page.

## Update Contact and Social Links

Edit `_config.yml`.

Useful fields:

- `email`
- `scholar_userid`
- `linkedin_username`
- `github_username`
- `description`
- `keywords`
- `contact_note`

Blank social fields are hidden automatically.

## Run Locally

From the site folder:

```bash
bundle exec jekyll serve
```

Then open:

```text
http://127.0.0.1:4000
```

For a build-only check:

```bash
bundle exec jekyll build
```

## Deploy

Because this repository is named `ashkanmor.github.io`, GitHub Pages can serve it from the repository root. After editing, commit and push your changes to GitHub.
