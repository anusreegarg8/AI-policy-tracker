# AI Policy Governance Intelligence Tracker

A live, force-directed network map of global AI governance developments across four thematic pillars: International Governance & Diplomacy, AI Safety & Risk, Climate & Environment, and National & International Security.

## Live Site

**https://anusreegarg8.github.io/AI-policy-tracker/**

Password protected. Contact repo owner for access.

## Structure

| File | Purpose |
|------|---------|
| `index.html` | Main application (D3 force graph, password gate, add-article form) |
| `articles.json` | All indexed articles — source of truth, updated via in-app form |

## Adding Articles

1. Open the live site and log in
2. Click **+ ADD ARTICLE** in the header
3. Paste a URL and click **FETCH METADATA** (uses Microlink.io)
4. Complete the required fields (pillar, criticality, geo scope, overview)
5. Click **SAVE TO TRACKER** — commits directly to `articles.json` in this repo

> Articles are saved via the GitHub Contents API. A Personal Access Token with `repo` scope must be entered once via the **⚙ Settings** button.

## Pillars

| # | Name | Color |
|---|------|-------|
| P1 | International Governance & Diplomacy | Cyan |
| P2 | Safety & Advanced AI Risk | Red |
| P3 | Climate & Environment | Green |
| P4 | National & International Security | Amber |

## Frameworks Tracked

UNIDIR AISE · UN GA Resolution 79-239 · G7 Hiroshima AI Process · ASEAN Guide on AI Governance · African Union AI Strategy · IHL / Geneva Conventions · NIST AI-RMF · China Interim Measures on Generative AI · CCW / LAWS Treaty · REAIM Summit Process

## Technical Notes

- Static site hosted on GitHub Pages — no server required
- Articles load dynamically from `articles.json` on each page open
- New articles are committed to the repo via GitHub REST API (browser → api.github.com)
- Password is client-side SHA-256 hashed — sufficient for personal/team use

## Weekly Update Workflow

Each week: open site → Add Article for each new relevant publication → articles auto-commit to this repo → site updates within ~30 seconds.
