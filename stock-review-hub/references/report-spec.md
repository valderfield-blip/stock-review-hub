# Stock Review Hub report specification

Use this reference when building or revising the HTML site.

## Brand

- Chinese name: `美股复盘局`
- English name: `Stock Review Hub`
- Public alias target: `stock-review-hub.vercel.app` when deployment/alias is requested and available.
- Tone: professional-investor research page, not a notebook of internal steps.

## Required HTML pages

- `index.html`: Chinese page.
- `index-en.html`: English page.
- Each page links to the other with a visible pill button.
- The page should remain static and deployable to Vercel without a build step.

## Visible information architecture

1. Sticky nav:
   - brand name
   - date search
   - latest review
   - 10-stock tracking pool
   - latest archive date
   - next watch
   - language switch
2. Hero:
   - brand title
   - latest date
   - risk score
   - core tracker
   - tracking pool count
3. Date search:
   - input field for date/ticker/topic keyword search
   - buttons: all, last 30 days, last 90 days, last 180 days
   - timeline cards with `data-date` and `data-keywords`
4. Latest daily review:
   - headline and market summary
   - metric cards for major indices and macro variables
   - seven-agent board
   - 10-stock tracking pool
   - next-session watch list
   - evidence block
5. Archive separator:
   - compact pill with date and topic
   - no explanatory paragraph about preserving original text
6. Archived entries:
   - preserve prior analysis but remove internal production-process labels.

## Date-search implementation

For a static page, use a small inline script:

- read `#dateSearch`
- read `.day-card[data-date][data-keywords]`
- normalize date strings by removing spaces, slashes, dots, hyphens, and Chinese date characters
- filter cards by keyword and by window buttons: all / 30 / 90 / 180 days

Each future trading day should add one card to `#reviewTimeline` and one full daily entry above the previous latest entry.

## Content rules

- Newest trading day always appears above older entries.
- Keep daily work product consistent so users can compare multiple days.
- Keep table columns stable where possible.
- Avoid showing raw “unavailable because API not configured” platform rows. If data is unavailable, exclude it from formulas and mention the data policy only in the footer or evidence audit.
- Every recommendation/tracker must include:
  - ticker / company
  - Bull Case
  - Bear Case
  - Confidence Score
  - action or watch condition

## Validation checklist

- No visible “Stage 1–4” or “Operating Contract” sections.
- No `0.00%` placeholder values.
- `DATA UNAVAILABLE` appears only where it clarifies actual missing data, not as a decorative row.
- Evidence blocks declare counts that match list item counts.
- Chinese and English pages both include date search and language switch.
- Local validator passes before deployment.
