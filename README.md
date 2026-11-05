# Competitor Analysis Tool

A single-page web app for comparing competing businesses and their online presence. It runs entirely in the browser: no server, no build step, no install.

## What it does

- **Competitors**: set up your own business and the competitors you want to compare, including headline, audience, services, pricing and website copy.
- **Website & positioning**: a side-by-side comparison with each business's most-used words, plus an AI positioning analysis and a positioning map with selectable axes.
- **Social media**: import CSV exports (Meta Business Suite, LinkedIn, scheduling or listening tools) to compare posting frequency, engagement, engagement rate, platform and format mix, and top posts.
- **Keywords**: paste or import keyword lists (Semrush, Ahrefs, Search Console) to see overlap, unique keywords and gaps, plus AI keyword opportunities.
- **Content gaps**: topics competitors cover that you don't, with priorities and content ideas.
- **SWOT analysis**: generate and edit a SWOT for any business.
- **Comparison report**: an executive summary and full report, downloadable as HTML or Markdown.

## Running it

Open `index.html` in a browser, or host it with GitHub Pages (below).

## Publishing with GitHub Pages

1. Push this repository to GitHub.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, then save.
4. After a minute or so, the tool is live at `https://<your-username>.github.io/<repository-name>/`.

## AI features

Positioning, social summaries, keyword opportunities, content gaps, SWOTs and the executive summary use the Anthropic API. Click **AI settings** in the app and paste an API key from [console.anthropic.com](https://console.anthropic.com). API usage is billed to that key.

- The key is stored in your browser's local storage only. It is **not** part of this repository, and it is sent nowhere except `api.anthropic.com`.
- Never commit an API key to this repository.
- Anyone who opens your GitHub Pages link needs their own key to use the AI features. Everything else works without one.

## Your data

Analyses are saved in the browser you use (local storage). They aren't uploaded anywhere, and they won't follow you to another browser or computer. Use **Back up this analysis** on the Competitors page to save a `.json` file, and **Restore from backup** to load it elsewhere. Clearing your browser data deletes saved analyses, so back up anything important.

## Social media CSV format

Columns are detected automatically. Recognised headers include:

`Competitor, Platform, Date, Post type, Likes, Comments, Shares, Saves, Views, Followers, Caption`

Only Likes, Comments and Date are really needed. Dates in day/month/year format are read as Australian dates. If a file covers a single account and has no Competitor column, you can choose which business it belongs to when importing. See `social-template.csv` for an example.

## Keyword format

One keyword per line, optionally followed by search volume and ranking position:

```
small business bookkeeping, 880, 4
bas agent melbourne, 590
```
