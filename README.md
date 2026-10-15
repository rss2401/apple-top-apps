# apple-top-apps

App Store top charts data for [Apple Top](https://github.com/rss2401/apple-top).

This repository only stores data. The website, downloader, and shared workflow live in
[rss2401/apple-top](https://github.com/rss2401/apple-top), which reads this repository's
GitHub Pages site through the relative path `../apple-top-apps/`.

## Contents

| Path | Description |
| --- | --- |
| `rankings/YYYYMM/` | Ranking RSS JSON per month: `<country>_apps_<feed>.json` |
| `lists/` | Curated app lists in ranking-feed format |
| `details/<id>.json` | iTunes Lookup responses, one result per country |
| `archives/<id>.json` | Ranking history of each item across months |
| `logos/` | Artwork: `<id>.png` (newest) and `<id>-<url-hash>.png` (versions) |
| `rankings.json` | Index of all ranking and list files, used by the website |

Snapshot at migration: 1329 items, 1307 detail files, 2327 artwork files, 1233 archives.

## Updates

`.github/workflows/update.yml` runs at 02:23 UTC on the first day of each month and every
Monday, and can be started manually. Every run in a month overwrites that month's
`rankings/YYYYMM/` directory, so each month keeps the latest weekly snapshot.

Data before this repository was created was migrated from
[xy2401/appstore](https://github.com/xy2401/appstore), where the full Git history remains.
