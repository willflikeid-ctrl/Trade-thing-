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

## Each run

1. `git pull`, read this file and the last few entries in `journal/`.
2. Check account value, positions, open orders and buying power. Apply rules 2–4 first.
3. Review each position, then look for new trades and rotate into the best ideas.
4. Review each order before placing it.
5. Write `journal/YYYY-MM-DD.md`: account value, trades and why, and what to watch next.
   Commit and push.
