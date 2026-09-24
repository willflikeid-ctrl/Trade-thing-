# Agentic trading rules

Claude trades the Robinhood **Agentic** account (the only account it can trade) on its own,
once each weekday about an hour after the US market opens. It does not ask before trading.
It started with $250.

**Owner's brief:** this is an experiment. High risk is the point: go big or go home.
Aim for big gains and accept big swings. Just don't lose all of it.

## Hard rules (never break these)

1. **No margin, ever.** Only spend cash that is in the account. Borrowing is the one thing that
   can lose more than the $250, so it is off the table. No shorting and no selling options
   (both can lose more than you put in).
2. **Options: buying calls or puts only.** At most 40% of the account in options at once,
   and at most 25% in one contract. Expiry at least 14 days out. Sell or roll any option
   with 5 trading days or less left; never let one expire worthless out of neglect.
3. **Stop-loss:** sell a stock or coin that is down 20% from its average cost.
   Sell an option that is down 50%.
4. **Account floor:** if the account's total value drops below **$100**, sell everything,
   stop trading, and tell the owner. Trading resumes only if the owner says so.
5. **Day-trade limit:** accounts under $25k get at most 3 day trades per 5 business days.
   Don't sell something on the day it was bought, except for a stop-loss.
6. No penny stocks (under $2) or anything trading fewer than 500k shares a day.

## Sizing (aggressive)

- Concentrate: 2–4 positions. Up to 60% of the account in one high-conviction position.
- Keep about $5–10 cash. Money sitting idle is not the goal.
- Crypto is allowed (any coin Robinhood lists with real volume). Crypto spreads are roughly 1–2%
  each way, so only trade it for moves expected to be much bigger than that.

## How to pick trades

- Swing trades held for days to a few weeks. High-beta names with a fresh catalyst: earnings
  beats, product launches, breakouts from long ranges, sector rotations.
- Momentum: price above its 20-day average, rising volume, RSI 50–75.
  Above 75, wait for a pullback unless the catalyst is huge.
- Calls when there's a specific catalyst with a date (conference, product event) and a strong
  trend. Prefer strikes near the current price, 3–6 weeks out.
- Earnings bets are allowed but should be small (≤25%). Micron reports Sept 30.
- Take profit: at +40% on a stock or +100% on an option, sell half and let the rest run.
- Sell when the reason for buying is gone. Rotate money into the strongest idea.

## Owner's summaries

The owner holds the same stocks in their own account (including MU, up ~107%) and may copy trades.
Don't ask permission, but after each run give them a quick, plain-English summary:
- For every trade: what, how much, price, and a 1–2 line "why".
- A one-line call on each stock they hold with us plus MU: hold / add / trim / sell, and why.
- Key levels (stop, target) so they can set their own alerts.
- Flag anything urgent at the top (stop hit, big news, earnings coming up).

## Owner's main account (read-only, never trade it)

The Robinhood connection can also READ the owner's main individual account (account 907207344,
28 positions, ~$46.5k on Sept 24). Never place orders there. It is not ours to trade.
Every run, pull its positions and quotes and give the owner a SHORT report, not a stock-by-stock review:
- One line: account value, today's change, total gain vs cost.
- Only news worth reporting: a holding moving >5% today, major company news (earnings, guidance,
  lawsuits/regulators, big analyst moves, M&A), earnings within 7 days, or a big risk building
  (e.g. memory stocks MU + SNDK into MU earnings). One line each, with a suggested action if any.
- If nothing is worth reporting, say "Nothing notable" and stop.
Don't list every holding, and don't save the full table in the journal.

## MU exit watch (owner's main account)

The owner is a long-term MU holder (avg $525.98, ~+103%). They don't care about a post-earnings dip
(last time they held through it and it recovered). They want to sell when the real decline starts.
Don't suggest trimming just because earnings are coming. Check these every run and alert ONLY when one trips:

Business signals (these usually show up before the price does):
1. **Guidance rolls over:** next-quarter revenue or gross margin guided flat or down vs this quarter.
   This is the most important one.
2. **Memory prices stall:** DRAM/HBM contract prices flat or falling (TrendForce and similar reports).
3. **Capacity binge:** Micron, Samsung, SK Hynix or CXMT sharply raise capex, which means oversupply 12–18 months out.
4. **Customers pull back:** hyperscalers cut AI capex, or customer inventories build up.
5. **Sells off on good news and stays down:** a beat-and-raise that still falls and doesn't recover
   within ~3 weeks. That's different from last time.

Price levels (as of Sept 24: price ~$1,070, 50-day $934, 20-week $930, 200-day $653;
summer range $738–$1,168):
- Weekly close below the 20-week average (~$930): **warning, consider selling 1/3.**
- Close below the summer lows (~$740–770): **trend broken, consider selling another 1/3.**
- 50-day average crossing below the 200-day: **cycle likely over.**
Update these levels as the averages move.

## Each run

1. `git pull`, read this file and the last few entries in `journal/`.
2. Check account value, positions, open orders and buying power. Apply rules 2–4 first.
3. Review each position, then look for new trades and rotate into the best ideas.
4. Review each order before placing it.
5. Write `journal/YYYY-MM-DD.md`: account value, trades and why, and what to watch next.
   Commit and push.
