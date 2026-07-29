# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository overview

This is `june0103.github.io` — a GitHub Pages site built with Jekyll, using the remote theme
[`just-the-docs/just-the-docs`](https://github.com/just-the-docs/just-the-docs) (a documentation-style theme with
an auto-generated left sidebar navigation). Site title/description ("기술 블로그" — a personal AI/dev study-notes
blog) is configured in `_config.yml`.

The repository is currently just scaffolding: `_config.yml` and `README.md`. There is no `Gemfile`, no `_posts`/
`_pages`/`_layouts` content, and no build tooling checked in yet.

## Working with Jekyll/GitHub Pages here

- Because `remote_theme` + `jekyll-remote-theme` are used, GitHub Pages builds this automatically — no local
  theme files need to be vendored.
- To build/serve locally you'll need Ruby + Bundler and a `Gemfile` (not yet present) referencing `github-pages`
  or `jekyll` plus the `jekyll-remote-theme` plugin declared in `_config.yml`. Typical commands once a `Gemfile`
  exists:
  ```
  bundle install
  bundle exec jekyll serve
  ```
- `just-the-docs` derives the sidebar nav from front matter (`title`, `nav_order`, `parent`, etc.) on each content
  page — when adding pages, set front matter consistently so the auto-generated navigation stays correct.
- Since `nav_enabled: true` is set for sidebar categories, new top-level sections should be added as pages/collections
  with appropriate `parent`/`has_children` front matter rather than hand-edited nav config.
