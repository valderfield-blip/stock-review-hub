<div align="right">
  <a href="./README.md"><img alt="English" src="https://img.shields.io/badge/Language-English-0969DA"></a>
  <a href="./README.zh-CN.md"><img alt="简体中文" src="https://img.shields.io/badge/语言-简体中文-CB2431"></a>
</div>

# Stock Review Hub

Stock Review Hub (`美股复盘局`) is a Codex skill for producing professional, bilingual daily U.S. stock-market reviews. It turns verified market, macroeconomic, earnings, news, valuation, sentiment, and quantitative data into an investor-facing HTML report while keeping internal research notes out of the published page. The workflow combines a market-data layer, seven specialized research agents, an investment-committee summary, and a content studio that maintains a searchable daily archive, a 10-stock tracking pool, Bull and Bear cases, confidence scores, risk analysis, backtesting metrics, and next-session watch items. Missing data is never replaced with fabricated values: unavailable inputs are marked `DATA UNAVAILABLE` during research and hidden from reader-facing components when they add no value.

## What the skill provides

- A consistent seven-agent research workflow covering macro, industry chains, fundamentals, sentiment, evidence, risk, and quantitative analysis.
- A bilingual Chinese/English report structure designed for deployment as static HTML on Vercel.
- A 10-stock tracking framework with Bull Case, Bear Case, Confidence Score, and monitoring notes.
- Date search and 30-, 90-, and 180-day archive views for continuous market-review records.
- Spoken-word finance podcast transcripts derived from the latest verified review, with bull/bear debate and next-session watch items.
- Evidence-first rules that prohibit invented prices, percentages, financial figures, or platform sentiment scores.

## Install

Clone this repository and copy the `stock-review-hub` directory into your Codex skills directory:

```bash
git clone https://github.com/valderfield-blip/stock-review-hub.git
cp -R stock-review-hub/stock-review-hub ~/.codex/skills/
```

Restart Codex after installation so the skill can be discovered.

## Example prompt

```text
Use $stock-review-hub to generate yesterday's bilingual U.S. market review, add it above the existing archive, maintain the 10-stock tracking pool, and prepare the HTML for Vercel deployment.
```

Live project: [stock-review-hub.vercel.app](https://stock-review-hub.vercel.app)

This project is intended for research and education and does not constitute investment advice.
