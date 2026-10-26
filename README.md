# Plano

**A paid media planner for Portugal and Spain.**
Split a campaign budget across Meta, Google Search, TikTok, LinkedIn and Pinterest, forecast what it can buy, and check ad copy against each platform's limits before launch.

👉 **Live demo:** **[hamsterfurioso.github.io/plano](https://hamsterfurioso.github.io/plano/)**

*Concept project by Alberto Machado Domínguez (Lisbon). Built to show how I approach media planning, budgeting and ad copy for clients.*

---

## Why I built it

In agency and in-house roles, the first question from a client is usually *"what will this budget get us?"* The answer often lives in a messy spreadsheet. Plano turns that conversation into a single page: change the budget, market or objective and the forecast updates instantly, with plain-language notes on what the numbers mean.

## What it does

### 1. Budget forecast
- Inputs: total budget, flight length, market (Portugal, Spain or both), value per conversion and campaign objective (awareness, traffic, conversions)
- Channel mix sliders for five platforms, with a **suggested mix** per objective
- Forecast per channel: impressions, clicks, CPC, conversions, CPA and ROAS
- Budget share vs. conversion share chart, to show which channels pull their weight
- Automatic insights: cheapest channel per conversion, break-even check, warnings for daily budgets too small to exit the learning phase
- Editable benchmark assumptions (CPM, CTR, conversion rate)
- One-click export of the plan as a table you can paste into Google Sheets or Excel

### 2. Ad copy check
- Character counters for Google responsive search ads, Meta feed, TikTok in-feed, LinkedIn single image and Pinterest pins
- A rough feed preview that shows where text gets cut off with "See more"
- Copy checks: call to action, use of numbers, excessive capitals, repeated exclamation marks and the strength of the opening line
- Example copy for a fictional Lisbon pastry delivery brand

## Method

```
impressions  = budget ÷ CPM × 1,000
clicks       = impressions × CTR
conversions  = clicks × conversion rate
CPA          = budget ÷ conversions
ROAS         = conversions × value per conversion ÷ budget
```

- Spain is modelled with CPMs about 15% above Portugal (a larger, more competitive auction).
- The objective adjusts the assumptions the way bidding strategy does: awareness buys cheaper reach with lower intent; conversion campaigns pay more per impression for higher-intent audiences.
- The model is linear. It does not cover frequency caps, audience saturation or learning phases, so it is a planning tool for the first client conversation. Benchmarks should be replaced with real account data after launch.

**The benchmark figures are illustrative starting points, not published industry data.** Platform character limits change often; check the official ad specs before launch.

## Tech

A single, dependency-free HTML file (HTML, CSS and vanilla JavaScript). It works offline, adapts to mobile and supports light and dark mode. Inputs are saved in the browser with `localStorage`.

## Run it

Open `index.html` in any browser, or publish it with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

## About me

Advertising and PR graduate (Universidad Complutense de Madrid) with experience in account management, paid media (Meta, Google, LinkedIn, TikTok, Pinterest Ads) and content creation. Based in Lisbon. Spanish (native), English (B2) and Portuguese (intermediate).

📧 albertomachdom@gmail.com

## License

MIT
