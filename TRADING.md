# Agentic trading rules

Claude trades the Robinhood **Agentic** account (the only account it can trade) on its own,
once each weekday about 30 minutes after the US market opens. It does not ask before trading.
It starts with $250. The owner chose an **aggressive** style.

## Hard rules (never break these)

1. **Cash only.** No margin (even though the account allows it), no options, no shorting.
2. **Stop-loss:** sell any position that is down 12% or more from its average cost.
3. **Account floor:** if the account's total value drops below **$150**, sell everything,
   stop trading, and tell the owner. Trading resumes only if the owner says so.
4. **Position size:** no more than 35% of account value in one stock or coin.
   At most 5 positions at a time.
5. **Crypto:** at most 40% of the account, and only BTC, ETH or SOL.
6. **Day-trade limit:** accounts under $25k get at most 3 day trades per 5 business days.
   Never sell a stock on the same day it was bought, except for a stop-loss.
7. **At most 3 new buys per day.** Keep at least $10 cash for fees and rounding.
8. Stocks and ETFs must be listed in the US and trade more than 1M shares a day. No penny stocks.

## How to pick trades

- Swing trades held for days to a few weeks.
- Look for stocks with strong momentum: price above its 20- and 50-day moving averages,
  RSI between 50 and 70, rising volume, plus a real reason (earnings beat, analyst upgrades,
  sector strength). Check the news for anything that breaks the story.
- Use fractional dollar-amount orders.
- Take profit: sell half of a position at +20%; move the mental stop on the rest to break-even.
- Sell if the reason for buying is gone (earnings miss, trend broken below the 20-day average).
- Never buy into a company that reports earnings in the next 2 trading days.

## Each run

1. Read this file and the last few entries in `journal/`.
2. Check the account value, positions and buying power. Apply hard rules 2 and 3 first.
3. Review each position, then look for new opportunities if there is room.
4. Place orders (review each order first).
5. Write `journal/YYYY-MM-DD.md`: account value, what was bought or sold and why,
   and what to watch next time. Commit and push it.
