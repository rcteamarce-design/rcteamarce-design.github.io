# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A single-page static website for the Capital One Volunteers Dog Shelter Initiative, hosted on GitHub Pages at `rcteamarce-design.github.io`.

## Development

No build step, dependencies, or package manager. Open `index.html` directly in a browser to preview, or use any static file server:

```bash
python3 -m http.server 8080
```

## Architecture

Everything lives in `index.html` — HTML structure, CSS (inline `<style>`), and JavaScript (inline `<script>`) are all co-located in one file. There is no external stylesheet, no bundler, and no framework.

**CSS design tokens** are defined as CSS custom properties on `:root` (warm orange/gold palette). All section styling references these variables.

**Page sections** (in order): fixed nav → hero → `#mission` → `#leaders` → `#impact` → `#volunteer` → footer. Nav links use anchor hrefs; the inline script adds smooth-scroll behavior to all `a[href^="#"]` elements.

`rcteamarce-design.github.html` is an earlier renamed copy of the same page and can be ignored.
