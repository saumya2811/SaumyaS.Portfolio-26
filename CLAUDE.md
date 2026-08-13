# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

Saumya Srivastava's personal portfolio site (product/UX research portfolio). The repo currently holds two work-in-progress, self-contained static HTML files — no build tooling, package manager, linter, or test suite. Each file inlines its own CSS in a `<style>` block and (where present) JS in a `<script>` block; there are no external asset files or shared includes between them.

## Development

- Preview a file by opening it directly in a browser, or serve the directory locally, e.g. `python3 -m http.server` then visit `http://localhost:8000/portfolio_WIP.html`.
- There is nothing to install, build, lint, or test — edits are made directly to the HTML/CSS/JS inline in each file.

## Architecture

- **`portfolio_WIP.html`** — the main site, built as a single-page app. All "pages" are `<div class="view" id="view-*">` blocks in one document, toggled by the `show(v)`/`go(v)` JS functions (see the `<script>` near the end of the file) rather than real navigation. Views: `home`, `cs-accom`, `cs-vm`, `practice`, `education`, `beyond`. Light/dark theme is CSS-variable driven and toggled via `toggleTheme()`, which sets `data-theme` on `<html>`; both palettes are defined as CSS custom properties under `:root` and `html[data-theme="light"]`.
- **`Accommodations_HTML_wip.html`** — a standalone, long-form deep dive on the Wayground/Quizizz accommodations case study. It's the expanded version of the `view-cs-accom` section inside `portfolio_WIP.html`, but is not currently linked from it. It only implements the dark palette (no `data-theme`/light-mode variant) and has no JS.
- The two files don't share CSS or JS — each defines its own design tokens (colors, fonts) independently, and the values differ between them (e.g. `--ember`, `--panel` are not identical across the two files). When porting styling or content between them, changes must be made in both places.
