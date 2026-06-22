---
title: "The Chinese Lunar Calendar, Explained: Why Birthdays and Festivals Move Every Year"
date: 2026-06-22T10:00:00+08:00
draft: false
description: "A plain-English guide to the Chinese lunar calendar — why dates drift on the Gregorian calendar, how leap months work, and how to keep lunar birthdays and festivals synced automatically."
summary: "Why does Chinese New Year fall on a different day each year? A clear explainer of lunar months, leap months, and how to stop recalculating lunar dates by hand."
tags:
  - chinese lunar calendar
  - lunar calendar
  - chinese new year
  - leap month
  - lunar birthday
categories:
  - culture
keywords:
  - chinese lunar calendar explained
  - why does chinese new year change every year
  - lunar leap month
  - lunar to gregorian
  - lunar birthday calendar
author: "MoonCal"
ShowToc: true
TocOpen: false
ShowReadingTime: true
cover:
  image: "cover.webp"
  alt: "Chinese lunar calendar explained"
  caption: ""
  relative: true
---

If you've ever wondered why **Chinese New Year lands on a different day each year**, or why your grandmother's birthday keeps sliding around the calendar, the answer is the same: the Gregorian calendar on your phone and the **Chinese lunar calendar (农历)** count time in two completely different ways. This post explains how the lunar calendar actually works — months, leap months, festivals — and why that mismatch is the root of so much annual confusion.

## Solar vs. lunar: two clocks running side by side

The Gregorian calendar is **solar** — it tracks Earth's orbit around the Sun, which takes about 365.25 days. That's why it's so steady: New Year's Day is always January 1.

The traditional Chinese calendar is **lunisolar**. Each month begins on a new moon and runs roughly 29.5 days, so twelve lunar months add up to about 354 days — **11 days short of a solar year**. That 11-day gap is the source of all the drift. A date fixed on the lunar calendar (say, the 15th day of the 8th month — Mid-Autumn Festival) keeps landing 11-ish days *earlier* on the Gregorian calendar each year.

## Why leap months exist

If the lunar calendar simply lost 11 days a year, the seasons would slide: within 16 years, "spring" festivals would drift into autumn. To prevent that, the calendar inserts a whole extra month — a **leap month (闰月)** — roughly every three years (seven times in 19 years, to be precise).

A leap month repeats the number of the month before it. So in a leap year you might have a regular 4th month *and* a "leap 4th month." This is where most software gets confused: a naive converter doesn't know whether a date in "the 4th month" means the regular one or the leap one, and it can crash, skip the year, or silently pick the wrong day. If you want the full picture, MoonCal has a dedicated [explainer on lunar leap months](https://usemooncal.com/en/guides/lunar-leap-month) and how to handle a birthday that falls in one.

## Why your festivals and birthdays "move"

Put the two ideas together and the pattern is clear:

- **Festivals** like Spring Festival, Qingming, the Dragon Boat Festival, and Mid-Autumn are defined by lunar dates, so their Gregorian date shifts every year. You can see this at a glance in a [year-by-year list of Chinese festival dates](https://usemooncal.com/en/festivals).
- **Birthdays and anniversaries** celebrated on a lunar date do exactly the same thing. A lunar birthday isn't "August 12 every year" — it's a lunar date that *converts* to a different Gregorian day annually.

This is also why the [Chinese zodiac](https://usemooncal.com/en/chinese-zodiac) animal for a given person depends on the Chinese New Year boundary, not January 1 — someone born in late January might belong to the *previous* year's animal.

## The everyday problem this creates

For anyone who keeps lunar traditions — diaspora families especially — this turns into a small annual chore:

1. Look up what the lunar date converts to *this* year.
2. Create or edit a calendar event.
3. Hope you remembered to do it again next January.

A normal "repeat yearly" event doesn't help, because it repeats on the *Gregorian* date — which is wrong next year. Doing the conversion by hand works exactly until the year you forget.

## The fix: let the calendar do the conversion

The clean solution is to stop converting dates yourself and **subscribe to a calendar feed that recalculates them for you**. That's the idea behind [MoonCal](https://usemooncal.com): you enter a lunar date once, and it expands that date into the correct Gregorian day for the next 20 years, served as a standard calendar subscription (the same ICS format Google, Apple, and Outlook all use).

Because it's a subscription, your calendar app refreshes it automatically — the right dates simply appear each year with no maintenance. You can:

- Build an [automatic lunar birthday calendar](https://usemooncal.com/en/try) for your whole family (no signup required to try it).
- Check a single date with the free [lunar date converter](https://usemooncal.com/en/tools/lunar-converter).
- [Find your Chinese zodiac sign](https://usemooncal.com/en/tools/chinese-zodiac-sign-calculator) using the correct New Year cutoff.

## FAQ

**Why does Chinese New Year change date every year?**
Because it's set by the lunar calendar, which is about 11 days shorter than the solar year. The festival drifts earlier each year until a leap month resets the alignment, so it bounces within a late-January-to-late-February window.

**What is a lunar leap month?**
An extra 13th month inserted roughly every three years to keep the lunar calendar aligned with the seasons. It repeats the previous month's number (e.g., "leap 4th month").

**How do I keep a lunar birthday correct on my phone calendar?**
Subscribe to a [Chinese lunar birthday calendar](https://usemooncal.com) feed instead of creating a yearly-repeating event. The feed converts the lunar date to the correct Gregorian date every year automatically.

**Is the Chinese calendar the same as the Vietnamese or Korean one?**
They share the same lunisolar logic and most festival dates, though some local observances differ. The conversion math described here applies broadly to East Asian lunisolar calendars.

## Takeaway

The lunar calendar isn't broken or arbitrary — it's a careful balance between the Moon's phases and the Sun's seasons, held together by leap months. The only real friction is that our phones run on a different system. Once you let a [lunar calendar subscription](https://usemooncal.com) bridge the two, the dates that matter to you stop drifting out of reach.
