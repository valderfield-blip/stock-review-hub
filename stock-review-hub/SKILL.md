---
name: stock-review-hub
description: Generate, update, and package the “美股复盘局 / Stock Review Hub” daily U.S. market review site and finance-podcast transcripts derived from the latest verified review. Use when asked to create a U.S. stock market recap, continue a daily review archive, produce a bilingual HTML/Vercel report, maintain a 10-stock tracking pool, enforce a 7-agent investment research workflow, turn verified market data into a professional investor-facing review page, or write an insightful spoken-word market podcast script for a broad finance audience.
---

# Stock Review Hub

Create a professional daily U.S. market review page branded as **美股复盘局 / Stock Review Hub**. The output is a reader-facing research site, not a dump of internal reasoning. Keep the process consistent across trading days so future one-month to six-month reviews can be searched, compared, and summarized.

## Core workflow

1. Determine the review date precisely. If the user says “yesterday,” resolve it against the current date and market calendar.
2. Collect real market, macro, earnings, news, valuation, sentiment, and quant data. Use primary/credible sources when available.
3. Never fill missing data with `0`, `0.00%`, peer averages, or template values. If a needed field is missing, mark it `DATA UNAVAILABLE` in analysis and exclude it from formulas.
4. Hide raw unavailable platform fields in the visible sentiment UI. Do not display rows such as “Stocktwits score requires login” or “full X API not configured.”
5. Produce a daily entry with the same 7-agent structure every trading day:
   - Agent 1: Macro Analyst
   - Agent 2: Industry Chain Researcher
   - Agent 3: Fundamental Analyst
   - Agent 4: Sentiment Analyst
   - Agent 5: Evidence Investigator
   - Agent 6: Risk Committee
   - Agent 7: Quant Researcher
6. Maintain a 10-stock tracking pool. Each stock must include Bull Case, Bear Case, Confidence Score, and action/monitoring note.
7. Add the newest trading day above older entries. Keep older entries as clean archive records, not long “how this was produced” explanations.
8. Build bilingual HTML when requested: `index.html` in Chinese and `index-en.html` in English, with visible language-switch buttons.
9. When a podcast transcript is requested, derive it from the latest completed review and follow `references/podcast-transcript.md`. Do not introduce unsupported figures or turn tracking ideas into personalized recommendations.
10. If deploying, use the `vercel-deploy` skill and return the final URL. Prefer the clean alias `stock-review-hub.vercel.app` when the user wants the current public page.

## Output shape

Use this visible page structure:

1. Hero: `美股复盘局` with subtitle `Stock Review Hub`.
2. Date search / review archive:
   - keyword/date search
   - filters for all, 30 days, 90 days, and 180 days
   - one card per trading day with date, topic, and tags
3. Latest daily review:
   - market metric cards
   - seven-agent output board
   - 10-stock tracking table
   - next-session watch list
   - evidence details
4. Older archive separator:
   - date and theme only
   - no internal production notes
5. Historical daily entry content.
6. Footer:
   - evidence and data-gap policy
   - education / not-investment-advice disclaimer

## Required references

Read the relevant reference before producing or updating the site:

- `references/report-spec.md` for page structure, UI rules, and bilingual requirements.
- `references/agent-framework.md` for the 7-agent research outputs and data rules.
- `references/podcast-transcript.md` when generating a spoken-word finance podcast transcript from the latest review.

## Style rules

- Write for professional investors: concise, evidence-backed, and readable.
- Do not expose “Stage 1–4,” “Operating Contract,” “how this enters the file,” or similar internal thinking sections in the HTML page.
- Keep the visible page focused on conclusions, data, risks, watch items, and archive navigation.
- Clearly separate “tracking” from “buy recommendation.” Avoid guaranteed returns or personalized investment advice.
- For financial data, browse or otherwise verify because prices, macro figures, and company facts change.
