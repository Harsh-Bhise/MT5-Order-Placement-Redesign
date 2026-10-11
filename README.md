# MT5 Order Placement · Interactive Prototype

A working prototype of the risk-first order placement redesign for MetaTrader 5 on iOS, built for a UX case study.

Concept project by Harsh. Not affiliated with or endorsed by MetaQuotes. Prices are simulated and no real trading happens.

## What works

- **Quotes:** search symbols, tap one to start an order.
- **Trade:** live account numbers (balance, equity, free margin, margin used), open positions and pending orders. Tap a position to close it, tap an order to cancel it.
- **Create Order:**
  - Auto Lots sizes the trade from your risk (% or $) and Stop Loss distance, live.
  - Stop Loss and Take Profit by pips or price.
  - Market, Limit and Stop orders on any symbol.
- **Error states with one-tap fixes:** not enough free margin, size above the 100-lot maximum, Stop Loss or Take Profit too close, size below the minimum lot, market closed, entry on the wrong side of the market for pending orders, and wrong-side Stop Loss or Take Profit.
- **Live prices:** pending orders fill when price reaches them, and positions close automatically at their Stop Loss or Take Profit.
- **Confirmation:** Order Filled, Order Placed (pending) and Order Not Sent.
- **History:** closed trades and net profit.
- **Settings:**
  - Freeze prices for usability tests.
  - Make the next order fail to send.
  - Jump to any state.
  - Reset the prototype.

The account is saved in the browser, so trades are still there on refresh. Use **Reset prototype** to start over.

## Host it on GitHub Pages (free)

1. Create a new public repository on GitHub, for example `mt5-prototype`.
2. Upload every file in this folder to the root of the repository: `index.html`, `manifest.webmanifest`, `icon-180.png`, `icon-512.png` and `README.md`. Use **Add file → Upload files**, then commit.
3. Go to **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main**, folder to **/ (root)**, then **Save**.
4. After a minute or two the site is live at `https://<your-username>.github.io/mt5-prototype/`.

## Use it in the case study

- **Notion:** type `/embed` and paste the GitHub Pages link. Make the embed tall, about 900 px. On a laptop it shows the phone frame with a list of tasks to try next to it.
- **On a phone:** open the link in Safari and choose **Share → Add to Home Screen**. It opens full screen like an installed app, which is ideal for usability testing.

## Suggested test tasks

1. Place a trade risking 1% with a 20-pip Stop Loss.
2. Place a fixed 0.50-lot trade (switch Auto off).
3. Before buying, say how much you could lose.
4. Place a Buy Limit below the market, then find it on the Trade tab.

Before each session, switch off **Live prices** in Settings so the numbers stay still while people work.
