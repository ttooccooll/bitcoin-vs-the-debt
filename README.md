# Bitcoin vs. The Debt

A live, single-page scoreboard that pits Bitcoin's market cap against the US national debt, styled like a heavyweight boxing match. Everything runs client-side in one `index.html` file, with no build step.

## What it does

- **Live scoreboard** comparing Bitcoin's total market cap to the national debt, with the ratio between them.
- **Debt clock** that ticks in real time at the average per-second borrowing rate.
- **The debt, priced in Bitcoin** — how many BTC it would take to cover the debt, with a 4-year chart (one halving cycle) that you can hover to inspect any point.
- **Make It Personal** — your per-person slice of the debt next to the price of one bitcoin.
- **24h momentum**, a head-to-head weigh-in, a "what if BTC hit $X" slider, and rotating commentary.
- **Since you opened this page** — running totals of how much the debt has grown while you read.

## Data sources

- **Bitcoin price and market cap:** [CoinGecko](https://www.coingecko.com) public API.
- **Price history (4 years):** [Kraken](https://www.kraken.com) public OHLC API.
- **National debt:** [US Treasury Fiscal Data](https://fiscaldata.treasury.gov) `debt_to_penny` API.

Last-good values are cached in `localStorage`, so a rate-limited or offline API still shows the most recent numbers instead of blanks.

## Running it

Open `index.html` in a browser. That's it. For the background music to play, keep `Work Harder.webm` (and the `Work Harder.mp3` fallback, for browsers that don't do WebM/Opus) alongside it; without the files the page still works, just silently.

## Notes

This is satire, not financial advice. Figures are pulled live and extrapolated between Treasury updates, so treat them as close approximations rather than exact accounting.
