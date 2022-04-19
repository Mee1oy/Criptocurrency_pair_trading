# Criptocurrency_pair_trading

This is algorithm for testing trading stratagy in cryptocurrency based on correlation between them. (Trere are 2 trades, one lonf and one short in 1 signal to trade.)
Main idea is to find pair of coins co compensate strong volatility on criptocurrency markets.

Analisys script is based on Binance API
In script analisys:
0. I have downloaded the OHLCV data for all coins available to trade in binancf
1. I tried to find coind with strong correlation.
2. I'm using MACD indicator, calculated for each interesting pair.
3. Then find the most reasonable ration for each pair. (ratio is calculated in %) with using visualisation.

As a result we must make matrix with [coin1 , coin2 , ration] like this 
trading = [['XTZ','ALGO',2.9], ['VET','IOTA',2], ['ETC','BCH',2.9], ['BAT','QTUM',2.3]]
You need to change date variable in code and uncomment the code below this variable to download new data for coins.
It needs to chage MA param to change calcualating period of MACD

Trading script is based on CCXT package (https://github.com/ccxt/ccxt) becouse Binance api was not working correct when I was developing this app.
In script virtual money trading:
1. We need to enter the result of previous script as matrix
2. Enjoy real time testing on current market data.
3. Result with opened positions and finential result will be printed after the main code cell and will be updated in real time.


I will add another indicators later and will try to find more stable trading strategy.
Welcome to use this idea)
