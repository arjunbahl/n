---
id: bGmLcFBNL3xXUHtYn8RXl
title: Ideas
desc: ''
updated: 1666979670012
created: 1639333089204
---
1. [Daily; Nifty]: We define 2 states on daily bars(o > c | o < c). Exponential pdf on this space.
    * 4 consec same states ~1%
    * Tested for stocks_with_futures =>
        * 3 consec states lead to ~33% of next state >3, i.e. momentum present
        * 4 consec states have 54% prob that next state <4 i.e. mean reversion

2. h2h & l2l after 9:15 & 14:15 to 10:15 & 15:15 (hourly timeframes) have alpha.
    * When is they most favourable moment to get in/out?
        - day range
        - 
3. Regimes
    - MACD 
        * +ve(C>O) 60%
        * -ve (C<O) 60%
    $\Longrightarrow$ Not useful

4. $\Delta h_{t+1} =\Delta h_{t} + [c-min_{t-5:t}l]/c + macds$
    - pvalues ~0
    - macds coefficient ~ 0; while other 2 have 0.05

5. 