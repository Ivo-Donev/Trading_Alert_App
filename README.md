# Stock Price Alert with News Notifications

This program monitors the stock price of Tesla Inc (TSLA) and sends SMS notifications if the price changes by more than 4%. It utilizes the Alpha Vantage API to collect stock price data and the News API to gather news articles linked to Tesla.

## Key Features

* Tracks the daily closing price of Tesla stock (TSLA)
* Sends SMS notifications when the stock price changes by more than 4%
* Retrieves recent news articles about Tesla
* Provides a summary of the price movement and the top three news articles

## Instructions

1. **Install the necessary libraries:**

```bash
pip install requests twilio


2. **Obtain API keys:**

   * Create an account on Alpha Vantage: [https://www.alphavantage.co/](https://www.alphavantage.co/) and obtain a free API key.

   * Create an account on News API: [https://newsapi.org/](https://newsapi.org/) and obtain a free API key.

   * Create a Twilio account (free trial available) and obtain a Twilio account SID and authentication token.

3. **Update the API keys in the code:**

   * Replace `STOCK_API_KEY` with your Alpha Vantage API key. 
   * Replace `NEWS_API_KEY` with your News API key. 
   * Replace `TWILIO_SID` and `TWILIO_AUTH_TOKEN` with your Twilio account SID and authentication token.

4. **Run the program:**

bash
python stock_price_alert.py


## Description

This program utilizes the Alpha Vantage API to fetch the daily closing price of Tesla stock (TSLA) for the previous two days. It then calculates the percentage change between the closing prices and identifies if the change exceeds 4%.

If the price change exceeds 4%, the program retrieves recent news articles about Tesla using the News API and selects the top three articles. For each article, it summarizes the headline and a brief description.

Finally, the program sends SMS notifications to the specified recipient, informing them of the price movement and providing a summary of the top three news articles.
