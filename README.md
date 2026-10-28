# Plano

**A paid media budget forecaster for any market.**
Split a campaign budget across Meta, Google Search, YouTube, TikTok, LinkedIn and Pinterest, forecast what it can buy in the country you're targeting, and compare the same plan across markets.

👉 **Live demo:** **[amachadod.github.io/plano](https://amachadod.github.io/plano/)**

*Concept project by Alberto Machado Domínguez. Built to show how I approach media planning and budgeting for clients.*

---

## Why I built it

The first question from a client is usually *"what will this budget get us?"*, and the answer changes a lot depending on the country. Plano turns that conversation into a single page: change the budget, market, currency or objective and the forecast updates instantly, with plain-language notes on what the numbers mean.

## What it does

### Budget forecast
- **Inputs:** market, currency, total budget, flight length, value per conversion and campaign objective (awareness, traffic, conversions)
- **20 markets** across North America, Europe, Asia-Pacific, Latin America, the Middle East and Africa, plus a **custom cost index** for anywhere else
- **Channel mix** sliders for six platforms, with a suggested mix per objective
- **Forecast per channel:** impressions, clicks, CPC, conversions, CPA and ROAS, plus estimated reach
- **Same plan in other markets:** the same budget and mix priced in six markets, with the lowest CPA highlighted, to show where a fixed budget goes furthest
- **Budget share vs. conversion share** chart, to show which channels pull their weight
- **Automatic insights:** cheapest channel per conversion, break-even check, warnings for daily budgets too small to exit the learning phase
- **Editable benchmarks** (CPM, CTR, conversion rate), so you can replace them with real account data
- **One-click export** of the plan as a table you can paste into Google Sheets or Excel

### Ad copy check
A second tab with character counters and a rough feed preview for Google responsive search ads, Meta, TikTok, LinkedIn and Pinterest, plus checks for a call to action, numbers, excessive capitals and the strength of the opening line.

## Method

```
CPM          = baseline CPM × market cost index × objective adjustment
impressions  = budget ÷ CPM × 1,000
clicks       = impressions × CTR
conversions  = clicks × conversion rate
CPA          = budget ÷ conversions
ROAS         = conversions × value per conversion ÷ budget
```

- **Market cost index.** Each market scales CPMs against a Western Europe baseline of 1.00. Large, competitive auctions such as the United States sit well above it; India, Brazil or Southeast Asia sit well below. Choose *Custom* to set your own index.
- **Click and conversion rates** stay the same across markets, because they depend more on the offer and the creative than on the country.
- **Objective** adjusts the assumptions the way bidding strategy does: awareness buys cheaper reach with lower intent; conversion campaigns pay more per impression for higher-intent audiences.
- The model is **linear**. It does not cover frequency caps, audience saturation or learning phases, so it is a planning tool for the first client conversation. Benchmarks should be replaced with real account data after launch.

**The benchmark figures and market cost indices are illustrative starting points, not published industry data.** Real costs vary by industry, season and audience.

## Tech

A single, dependency-free HTML file (HTML, CSS and vanilla JavaScript). It works offline, adapts to mobile and supports light and dark mode. Inputs are saved in the browser with `localStorage`.

## Run it

Open `index.html` in any browser, or publish it with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

See also [Minuta](https://github.com/amachadod/minuta), which turns call notes into tasks for the right team.

## About me

Advertising and PR graduate (Universidad Complutense de Madrid) with experience in account management, paid media (Meta, Google, LinkedIn, TikTok, Pinterest Ads) and content creation. Based in Lisbon. Spanish (native), English (B2) and Portuguese (intermediate).

📧 albertomachdom@gmail.com

## License

MIT
