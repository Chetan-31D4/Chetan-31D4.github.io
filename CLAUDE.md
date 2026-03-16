# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Chetan Singhal (AI/ML Engineer & Data Scientist, IIT Madras). This is a **single-file static site** — all HTML, CSS, and JavaScript live in `index.html`. There is no build system, bundler, or framework.

## Development

Open `index.html` directly in a browser. No server, install step, or build command is needed. To preview changes, refresh the browser.

## Architecture

- **Single file**: `index.html` contains everything — structure, styles (`<style>` block, lines 8–596), markup (lines 598–888), and scripts (`<script>` block, lines 890–959).
- **CSS custom properties** defined in `:root` (lines 10–23) control the entire color scheme and typography. The design uses three font families: Syne (display), DM Sans (body), JetBrains Mono (code/labels), loaded from Google Fonts.
- **Sections**: nav, hero, marquee, about, experience (timeline), projects (card grid), GitHub (live repo fetch), education, contact, footer.
- **Scroll reveal**: Uses `IntersectionObserver` — elements with class `.reveal` animate in when scrolled into view.
- **GitHub integration**: `fetchGitHub()` calls the GitHub API to display a user's top 6 repos dynamically. Username is entered via an input field.
- **Responsive**: Single `@media(max-width:768px)` breakpoint. Nav links are hidden on mobile (no hamburger menu currently).

## Key Conventions

- Color accent is `--accent: #c4f048` (lime green). Secondary accents: `--accent2` (teal), `--accent3` (gold).
- All buttons/tags use `border-radius: 100px` (pill shape).
- Font sizes use `clamp()` for fluid typography in headings.
- Inline SVGs are used for all icons (no icon library).
