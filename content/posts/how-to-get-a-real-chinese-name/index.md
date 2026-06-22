---
title: "Chinese Name Lab: a tool for getting an authentic Chinese name"
date: 2026-06-22
draft: false
slug: "chinese-name-lab"
description: "A naming tool for English speakers. Every name comes with hanzi, pinyin, an English meaning, a gender style, and a transparent naturalness score — not random characters. With some notes on the engineering behind it."
tags: ["side project", "Next.js", "SEO", "Chinese names"]
categories: ["projects"]
cover:
  image: "cover.webp"
  alt: "Chinese Name Lab — authentic Chinese names with meaning and pinyin"
  caption: "[chinesenamelab.com](https://chinesenamelab.com)"
  relative: true
---

I recently shipped a small project called **Chinese Name Lab**. It generates authentic, usable Chinese names for English speakers.

Live site: <https://chinesenamelab.com>

## Why I built it

Search "chinese name generator" in English and most results disappoint. They tend to staple a few random characters together that don't read like a name, or transliterate your name into an odd-looking string. For anyone who actually wants a Chinese name — a student, someone taking a language class, parents naming a baby, or a writer looking for character names — these tools fail the one test that matters: *is this really a name?*

That question is also the biggest doubt foreign users have: "Is this a real name, or just random characters?"

So the whole premise of the site is one line on the homepage:

> Chinese names that actually sound natural — not just random characters.

Every generated name comes with the hanzi, pinyin, an English meaning, a gender style, and a per-dimension naturalness score. It doesn't just hand you a name; it shows you why the name is a good one.

## What it does

The site is a set of tools built around naming:

- **Chinese name generator** — by gender, style, and purpose, with a full explanation. Dedicated pages for male and female names.
- **English to Chinese name** — dictionary matches use hand-curated names; everything else falls back to rule-based transliteration, so it never returns nothing.
- **Name meaning checker** — paste a name you already have and get pinyin, meaning, and a naturalness score broken down by dimension.
- **Xianxia / cultivation character names** — this turned out to be a high-traffic niche, so it grew into a cluster of pages for cultivation, demonic, and sect names.
- **Chinese font / calligraphy generator** — render a name in different fonts to see how it looks.

The underlying data is real: 100+ surnames, 300+ carefully chosen naming characters, 500+ hand-curated names, plus a homophone blacklist and a list of negative characters to avoid pitfalls (for example, a name whose pinyin collides with the word for "idiot"). The library simply doesn't contain the unflattering characters, so results stay clean at the source.

## Notes on the engineering

This part is for anyone else working on side projects. A few decisions I'm happy with:

**The naming engine is framework-agnostic.** The core algorithm depends on neither React nor Next — only on a `DataSource` interface. Today the data is read from in-memory JSON; moving to a database later means writing one new implementation, with no changes to the algorithm or the pages. The boundary is enforced with an ESLint rule.

**Scoring is pluggable.** Meaning, gender, sound, style, avoidance, surname fit — each dimension is an independent scorer, and the total is their sum, clamped. Adding a dimension means pushing one scorer without touching the main flow. Every name carries a full `scoreBreakdown` for the UI — that's "show your work" at the code level.

**Deterministic SSG.** All randomness goes through a seeded RNG, and each SEO page uses a fixed seed for its first screen of names. The result is content that is stable, indexable, and cacheable; new names are fetched from an API only when the user hits "regenerate."

**No database at runtime.** Reference data is JSON loaded at build time. The database is used only for rate limiting, and rate limiting fails open if the database has problems, so it can never take down the core act of generating a name.

**The SEO page matrix is config-driven.** Adding a new tool page is roughly one config entry plus a three-line `page.tsx`, which lets me cover long-tail terms quickly instead of repeating myself.

The stack is Next.js 15 (App Router) with React 19 and TypeScript, Tailwind for styling, Drizzle and Postgres for rate limiting only, and Sentry for errors.

## Try it

If you know someone who wants a Chinese name, or you're writing a story with Chinese characters, take a look:

<https://chinesenamelab.com>

It's a work in progress — the name library and scoring dimensions will keep growing. If a generated name feels off, or you have ideas, I'd genuinely like to hear it; that kind of feedback is the most useful for tuning naturalness.
