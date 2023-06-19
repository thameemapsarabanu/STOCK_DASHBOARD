# STOCK_DASHBOARD
The code provided is a Streamlit application that creates a stock dashboard. Here's a breakdown of what the code does:

The necessary libraries are imported, including Streamlit, pandas, numpy, yfinance, plotly, and the required modules from the alpha_vantage and stocknews packages.

The Streamlit application is initialized with the title 'Stock Dashboard'.

The user is prompted to enter a ticker symbol, start date, and end date through the sidebar input fields.

The yfinance library is used to download the historical stock data based on the provided ticker symbol and date range.

The plotly express library is used to create a line chart with the adjusted closing price, open price, close price, high price, and low price as separate series. The chart is displayed using the st.plotly_chart() function.

The layout is organized into three columns: pricing_data, fundamental_data, and news.

Within the pricing_data column, the header 'Price Movements' is displayed. The 'Adj Close' column of the downloaded data is used to calculate the percentage change, annual return, standard deviation, and risk-adjusted return of the stock. The calculated values are displayed using the st.write() function.

Within the fundamental_data column, the Alpha Vantage API key is provided, and an instance of the FundamentalData class is created. The balance sheet, income statement, and cash flow statement for the specified ticker symbol are fetched using the FundamentalData methods. The retrieved data is processed and displayed using the st.write() function.

Within the news column, the header 'News of {ticker}' is displayed. The StockNews class is initialized with the specified ticker symbol, and the RSS feed is fetched using the read_rss() method. The published date, title, summary, title sentiment, and news sentiment for the first 10 news articles are displayed using the st.write() function.

This code creates a stock dashboard with price movements, fundamental data, and recent news for the specified stock symbol.

