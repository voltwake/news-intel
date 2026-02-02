---
name: news-intel
description: >
  News and intelligence aggregator. Real-time tech news, crypto news, Hacker News deep access,
  and custom RSS feed management. Use when the user asks about latest news, tech trends, crypto headlines,
  HN discussions, or needs to monitor RSS feeds. Sources: TechCrunch, HackerNoon, HN, CoinDesk, TheBlock.
  Zero dependencies, no API keys needed.
---

# News Intel

Zero-dependency news intelligence system. Fetch, aggregate, and monitor news from multiple sources.

## Quick Reference

All scripts in `{baseDir}/scripts/`. Run with `node`.

| Command | What it does |
|---------|-------------|
| `node {baseDir}/scripts/news.js` | All news sources combined |
| `node {baseDir}/scripts/news.js tech [N]` | Tech news only |
| `node {baseDir}/scripts/news.js crypto [N]` | Crypto news only |
| `node {baseDir}/scripts/news.js hn [N]` | Hacker News only |
| `node {baseDir}/scripts/news.js brief` | Minimal headline summary |
| `node {baseDir}/scripts/hn.js top [N]` | HN top stories |
| `node {baseDir}/scripts/hn.js new [N]` | HN newest stories |
| `node {baseDir}/scripts/hn.js best [N]` | HN best stories |
| `node {baseDir}/scripts/hn.js ask [N]` | Ask HN threads |
| `node {baseDir}/scripts/hn.js show [N]` | Show HN projects |
| `node {baseDir}/scripts/hn.js jobs [N]` | HN job postings |
| `node {baseDir}/scripts/hn.js item <id>` | Story details + top comments |
| `node {baseDir}/scripts/hn.js search <query>` | Full-text search (Algolia) |
| `node {baseDir}/scripts/rss.js <url> [N]` | Read any RSS/Atom feed |
| `node {baseDir}/scripts/rss.js discover <url>` | Auto-discover RSS feeds on a website |
| `node {baseDir}/scripts/rss.js add <name> <url>` | Save a feed for quick access |
| `node {baseDir}/scripts/rss.js list` | List saved feeds |
| `node {baseDir}/scripts/rss.js read <name> [N]` | Read a saved feed |
| `node {baseDir}/scripts/rss.js all [N]` | Read all saved feeds |

## Modules

### news.js — Multi-source aggregator
Pulls from TechCrunch, HackerNoon, Hacker News, CoinDesk, TheBlock. Filter by category or get a brief summary.

### hn.js — Hacker News deep access
Full HN API integration (Firebase) plus Algolia search. Browse top/new/best/ask/show/jobs, read item details with comments, or search the entire HN archive.

### rss.js — RSS feed manager
Read any RSS/Atom feed by URL. Auto-discover feeds on websites. Save feeds locally for quick repeated access. Supports persistent feed library at `~/.config/rss/feeds.json`.

## Data Sources (all free, no API keys)

- HN Firebase API — real-time Hacker News data
- Algolia HN Search — full-text search across HN history
- TechCrunch RSS — tech industry news
- HackerNoon RSS — developer/startup content
- CoinDesk RSS — crypto industry news
- TheBlock RSS — blockchain/DeFi news
