# Bitcoin vs US Debt — The Matchup

A sports-broadcast style visualization comparing Bitcoin's market cap to the US National Debt, with dark satire and real-time ticking.

## What It Is

A live, interactive financial showdown presented like a sports broadcast. Bitcoin (the challenger) vs. the US National Debt (the dominant champion). Real-time data from CoinGecko and US Treasury, with a ticking debt clock that shows how much the government borrows while you watch.

## Live Data Sources

- **Bitcoin**: CoinGecko API
  - Endpoint: `https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&ids=bitcoin`
  - Returns: price, market cap, 24h change, volume, ATH, circulating supply

- **US National Debt**: Treasury Fiscal Data API
  - Endpoint: `https://api.fiscaldata.treasury.gov/services/api/fiscal_service/v2/accounting/od/debt_to_penny`
  - Live estimate ticks at $136,574/second based on average daily growth ($11.8B/day)

## The Comparison

```
BTC Percentage = (Bitcoin Market Cap / US Debt) × 100
```

At ~4%, Bitcoin is far behind. The debt must be matched (100%) for Bitcoin to "win."

## Features

### Main Scoreboard
- Large animated numbers showing both totals
- Percentage display (BTC as % of debt)
- Flash animation when BTC price increases on refresh
- Particle burst celebration effect on gains

### Live Debt Clock
- Ticking every 100ms with current estimated debt
- Shows per-second, per-minute, and per-day rates
- Positioned prominently below scoreboard

### Since You Opened This Page
A dramatic section tracking how much debt accumulates during your visit:
- Total debt added (large pulsing red number)
- Homes worth of debt (at $417k median)
- Interest accrued
- Your personal share growth
- Teslas that could've been bought
- $ per heartbeat (averaging 72 bpm)
- Full college tuitions

### Interactive Elements
- **What-If Slider**: Drag to simulate BTC at different prices and see what percentage of debt it would represent
- **Head-to-Head Stats**: Visual bars comparing supply limits, age, control, daily changes, and total size
- **Momentum Meter**: Shows 24h BTC performance vs. debt's daily growth

### Play-by-Play
Timestamped commentary that updates with live data, featuring:
- Current prices and percentages
- Time-based insights
- 24h performance calls
- Humorous asides

### Things That Are Going Great (Satire)
Dark humor section with statistics about the debt crisis:
- Interest vs. defense spending
- Per-person debt
- Daily debt growth
- Bitcoin's fixed supply vs. infinite debt

## Visual Design

### Color Palette
- Bitcoin Orange: `#f7931a`
- Debt Red: `#ff3b3b`
- Success Green: `#00c853`
- Background: `#0c0c0e`
- Surface: `#141416`
- Text: `#eaeaea` / `#aaa` / `#666`

### Typography
- Oswald (display/titles)
- Inter (body)
- JetBrains Mono (numbers/data)

### Effects
- Animated spotlights (orange and red) sweeping the page
- Particle system for celebrations
- Staggered slide-in animations on page load
- Pulsing debt counter
- Scoreboard flash effect

### Audio
- Auto-playing background music ("Work Harder.wav")
- Plays on user interaction if browser blocks autoplay

## Responsive Design

- **Desktop (>900px)**: Full layout
- **Tablet (≤900px)**: Adjusted grids
- **Mobile (≤640px)**: Stacked layouts, reduced padding, optimized fonts
- **Small mobile (≤480px)**: Single-column grids
- **Tiny (≤380px)**: Stacked top bar, minimal spacing

All text maintains minimum 14px for readability. Colors have sufficient contrast.

## Running Locally

```bash
open index.html
# or
npx serve .
```

Auto-refreshes every 60 seconds.

## Tech Stack

- Single HTML file with embedded CSS/JS
- No build step
- Vanilla JavaScript
- Google Fonts (Inter, JetBrains Mono, Oswald)
- Canvas for particle effects
- CSS animations for spotlights and entrance effects

## Files

```
index.html      - Main application
Work Harder.wav - Background music (auto-plays)
SPEC.md         - This file
```