# Seven-agent daily research framework

Use this reference whenever generating or updating a daily review entry.

## Data layer rules

- Prefer real, current, verifiable data.
- Never invent market prices, macro numbers, earnings metrics, analyst ratings, or sentiment scores.
- Never substitute `0`, `0.00%`, industry averages, or template values for missing data.
- If data is missing, mark it `DATA UNAVAILABLE` in the underlying analysis and exclude it from formulas.
- Use evidence links for claims that matter.

## Agent outputs

### Agent 1: Macro Analyst

Analyze:

- S&P 500
- Nasdaq
- Dow Jones / Russell 2000 when useful
- VIX
- 10Y Treasury
- Dollar Index
- CPI / PPI
- employment data or major macro releases

Output:

- market risk score
- one-paragraph macro conclusion
- next-session macro watch levels

### Agent 2: Industry Chain Researcher

Analyze:

- current hotspot
- value chain
- bottlenecks
- beneficiary companies
- chain risks

For AI infrastructure reviews, a useful chain is:

`cloud demand → GPU/ASIC → HBM/DRAM → optical interconnect → power/cooling → applications/monetization`

### Agent 3: Fundamental Analyst

Analyze, when available:

- Revenue
- EPS
- FCF
- ROE / ROIC
- Gross Margin
- customer structure
- management quality
- CapEx and owner-earnings pressure

Do not overstate precision when a metric source conflicts; preserve conflict and use the conservative interpretation.

### Agent 4: Sentiment Analyst

Analyze:

- accessible Reddit/X text
- news
- analyst ratings
- market reaction

Output:

- Bull Score
- Bear Score
- Sentiment Score
- short interpretation

Do not display native platform sentiment scores that require login/API access. Exclude them instead.

### Agent 5: Evidence Investigator

Every major conclusion should have at least five evidence items. If evidence is insufficient:

- label the conclusion `LOW CONFIDENCE`
- reduce recommendation confidence
- do not let weakly evidenced stocks become core picks

Evidence hierarchy:

1. company IR / official filings
2. official macro data agencies
3. reputable market data providers
4. mainstream financial/news wires
5. community/social text for sentiment only

### Agent 6: Risk Committee

Always write the contrarian case:

- why the view may be wrong
- why the stock or market may fall
- valuation risk
- regulation risk
- demand risk
- competition risk
- geopolitics and supply-chain risk

The risk committee can veto high-scoring ideas without enough margin of safety.

### Agent 7: Quant Researcher

When data is available, output:

- Sharpe
- Sortino
- Win Rate
- Max Drawdown
- CAGR

If backtest data is not available, write `DATA UNAVAILABLE` and do not output zeros. When adding new tracking stocks, state whether they are already in the backtest set or awaiting next batch run.

## 10-stock tracking pool

Default structure:

1. Core application/cloud tracker
2. Second application/cloud tracker
3. AI accelerator leader
4. ASIC/networking chokepoint
5. HBM/DRAM chokepoint
6. Optical interconnect chokepoint
7. Power/cooling infrastructure
8. Ads/social AI quality tech
9. Enterprise software/cloud quality tech
10. Consumer ecosystem quality tech

Each row must include Bull Case, Bear Case, Confidence Score, and action/watch condition.
