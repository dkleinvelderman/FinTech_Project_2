*Project 2, Team 7 - Evan Paliotta, Francisco Lopez, Daniel Klein Velderman*

Crypto Caroussel
---
![Carousel](./images/Carousel.JPG)

## Summary
Our project is to create and compare a short-term algorithmic trading strategy with a medium-term buy and hold strategy. In reference to our short term strategy, we utilize the RSI and MACD while implementing regression and natural language processing in our buy and hold strategy. The latter strategy uses daily BTC exchange rate data and focuses on nine currencies with three distinct use cases.  We gathered data from the Binance API for both strategies and the Reddit API for NLP. Finally we compared the returns of the models and ultimately determined which strategy is more profitable to implement.
TL;DR- Using ML and NLP to filter through altcoins, can we make more money with a short term trading strategy or a buy and hold strategy.

### Crypto Investment Strategy can be based on:  

1.   the fundamentals of various crypto projects (e.g. white paper, activity and experience of team, use case, what problem does it solve, is there a working product, listed on exchanges, partnerships, trading volume, market cap, supply) https://coinmarketcap.com/
2.   Sentiment, attention and acitivty of the crypto project in (digital) media (reddit, discord, telegram, CNBC)
3. performance to date of single crypto projects or groups of projects based on use-case and/or fundamentals  
> Ideally one would pursue a combination of all of the above to come to a solid investment strategy. Our thoughts are that we choose 3 crypto use-cases that appeal to us and we believe are viable going forward. For each use-case we select two crypto-projects based on the fundamentals (desk research) and the sentiment (NLP?). Subsequently (simultaneously?) we apply Machine Learning to the concerning 6 crypto currencies to determine future potential financial performance based on historical (API) data.


| Payment  | Smart Contracts  | Supply Chain  |
|---|---|---|
| Chainlink  | Zilliqa   | VeChain  |
| Nano | NEO  | Waltonchain  |
| Monero | Cardano | Tael/Wabi  

Ticker List:
*   Chainlink: LINK
*   Nano: NANO
*   Monero: XMR
*   Zilliqa: ZIL
*   NEO: NEO
*   Cardano: ADA
*   VeChain: VET
*   Waltonchain: WTC
*   Tael: WABI

>>  Depending on outcome, we select 2 or 3 crypto currencies to trade and plot them in our algo trader utilizing technical analyses such as Bollinger Bands, RSI, MACD, Fibonacci  (https://www.investopedia.com/technical-analysis-basic-education-4689655)


*   **API Resources:** Blockchain.com, Coinbase.com (2nd option), Kraken, Binance  https://www.binance.com/en/support/articles/360002502072
</b>
*   Perhaps compare the ML model with the algo trading structure (compare long and short term strategies)
*   Compare multiple long term strategies and multiple short term strategies (2 ML models and 2 algo strategies/technical indicators)
*   Types of models: clustering with volume as the independent variable, regression for price prediction
*   What problem are we trying to solve for/what's the desired output of our results?  This question will dictate which model we use.
*   We could make calculations and make the output our independent variable (ex. Sharpe ratio or CAPM)--this ensures we're not using readily available data that anyone could easily use
WHat do we want our model's outputs to look like? Can these outputs be fed into an algo trading model or is this a different task?

Links:
*   Cryto ML example: https://towardsdatascience.com/cryptocurrency-price-prediction-using-deep-learning-70cfca50dd3a
*   Crypto types: https://medium.com/towardsblockchain/a-classification-of-crypto-tokens-aa416af26c40
*   Combining ML and Algo trading: https://towardsdatascience.com/https-medium-com-skuttruf-machine-learning-in-finance-algorithmic-trading-on-energy-markets-cb68f7471475
*   List of crypto APIs: https://rapidapi.com/collection/best-bitcoin-apis
*   CoinAPI.io documentation-more detailed data sequences (minute, hour, day volume etc...): https://docs.coinapi.io/#list-all-assets
*   Academic paper on decision trees and algo trading models: http://ceur-ws.org/Vol-1864/paper_13.pdf
*   CAPM with crypto:https://www.reddit.com/r/Bitcoin/comments/42fvzp/what_to_use_as_suitable_benchmark_in_capm_for/ (CAPM may not work because the beta is 0 and the risk free retun right now is pretty much 0 so there can be no expected return)

Potential Issues:
*   Perhaps we're combining processes that shouldn't be combined (machine learning can be used to predict the price over a longer time horizon while the algo trading platform attemps to capture gains in the shorter term)...can we reconcile these processes or not?
*   We've only run algo strategies with one asset. How will we do it with a portfolio of assets?  
*   It would be nice to gauge sentiment using NLP however the free APIs are inadequate (not all articles in the set are processed)
*   Kraken only has 34 assets and Coinbase does not support too many coins either
*   Using multiple APIs/datasets may pose an issue when it comes to aligning the variables (this may mean we need to scrap the types of crypto idea since not all types will be on the same exchange)---in other words, just because a coin is trading doesn't mean it will be available to an API
*   The only ML algo model we did (decision tree algo trading--15-3) has binary outputs for the trees and uses one ticker while we're trying to have multiple outputs and multiple tickers.  This will be hard to reoncile without running tons of code
