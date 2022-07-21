# NVDA-Stock-Price-Prediction-by-CNN-LSTM-DNN-model
<i>DISCLAIMER:
Bellow code is only for informative purpose, i renounce any responsibility regarding this code and trained model causing loss of money during trading on real market.</i>

<b>Stock price prediction : NVDA</b>

This page does following:

- load libraries and load stock data as dataframe<br>
- display chart with close price<br>
- add indicators to loaded dataframe<br>
- filter out formations and get its windows<br>
- Export data to csv file<br>

<b>Trading strategy</b><br>
Trading chart: Daily<br>
Trade type: LONG<br>
Stock: NVDA<br>
Entry price: Open price of current month (1st open price on weekly chart right after formation is formed)<br>
Exit price: Model predicts Highest high price of following month (4 weeks period)<br>

<b>Trading Data</b><br>
We are loading weekly data from yahoo finance. We are preprocessing dataset in following order - 24 candle formation (representing 24 weeks) + 1 monthly candle as label (following 4 weeks period). Bellow code will preprocess data in such order, 6th candle in window is always a monthly candle.

<b>**monthly candle is not calendar month, it is 4 weeks period that is followed by our 5 candle formation</b>

Trading method is following:

- We are trading upper trend
- We are openning trade on the current week Open price after formation is formed

<b>Traded formation</b><br>


We are getting windows from stock dataset, each window has 25 rows (25 candles), 24 rows (formation) + 1 row (label).
