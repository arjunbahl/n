---
id: "j5nzszmncq5tlgmu135aw34"
title: "Book Notes Man Who Solved the Market"
desc: ''
updated: "1649621089132"
created: "1649621089132"
date: "2022-04-11"
categories: 
  - "research"
---


## Kernel methods
1. Took them days to figure out bleeding strategy (long term momentum strategy bleeding in 2000)
2. Could've employed kernel methods with pricing data and certain technical/statistical signals to create higher dimensional data.
    - Using kernel trick to generate insights from it by classifying into buy/sell basis these new dimensions and looking into past.
3. They described it as 'black-box' meaning they didn't know exact parts therefore i think they had multi-dimensions(signals) added which looking back at history told buy/sell. But you could not figure out which dimension was having highest weight/ driving the decision but only look at end result which got formulated taking into account overall dimensions.


## Nova fund
1. Prediction model was in place by Frey.
    - He looked at 'relative' differences between group of stocks and betted on mean reversion.
2. However betting/execution system was very naive, couldn't self adjust and had no comprehensive constraints. As a result manual adjustments were being made by team to portfolio generated leading to sub-par returns.
    - Sometimes portfolio consisted of short positions for stocks which couldn't be shorted, or trades could not be filled leading to unbalanced portfolio, or broker/ leverage limitations were there. These were dealt with manual adjustments leading to incomplete portfolio.

3. Brown & Mercer created a single model which had all constraints/limitations and leveraged Frey's prediction model. It ran couple of times every hour to churn out portfolio recommendations. In case some position could not be filled it re-adjusted (ran again and took into consideration the current portfolio and estimated portfolio). Optimisation problem majorly was solved for construction.



## Futures fund
1. Straight buy/sell signals.
2. When Straus sold his stake and had to liquidate positions in internal fund he later admitted he thought he'll be able to put his money into on of the other funds as he believed they were "one of many". He never thought/knew of any secret sauce.
