# project2 CryptoKnight
Analysing Twitter sentiment to obtain trading signals

Presented by: Shan Shan Zhang, Alisha Geary, James Sheridan & Kai Ooi

# Motivation
The year is 2021.
Bitcoin (and cryptocurrency) is ubiquitous to all involved in the Fintech space.
The premise of 'Will it survive?' has been replaced with 'To what extent can Bitcoin fluorish?' 
Retail investors & Institutions have entered.
Local governments are coming in with Miami looking at investing some of city's treasury reserves in Bitcoin. (1)
Who will be the next? Which nation states will be first?
Like it or not, Bitcoin and cryptocurrencies are here to stay.
What better way to get on the Bitcoin bandwagon, than to learn to potentially time one's entry.
We aim to come up with a guide on potential entry and exits for Bitcoin based on Twitter sentiment.

# Hypothesis
Twitter sentiment has a high correlation with Bitcoin prices, potentially guiding entry and exit points.

# Data Collection
Twitter full archive search API (2) & 'Tweepy' python package (3) was used.
We collated the first 100 tweets per day, for 50 days, mentioning the term 'Bitcoin'.
Yahoo Finance API was used for historial Bitcoin prices. (4)

# Analysis
TextBlob was a new library package we used to obtain subjectivity, polarity & sentiment.
Sentiment scores and raw text files were appended.

Twitter Sentiment and Bitcoin price were overlayed.
Upon analysis, using a range of sentiment values as entry and exit points leads to very profitable signal generation.

![BTC_sentiment.png](images/BTC_sentiment.png)

Text from 5000 tweets were tokenized, lemmatized, cleaned and processed.
A wordcloud and top 20 word bar chart were created.

![BTC_WC_50days.png](images/BTC_WC_50days.png)

![20_top_words.png](images/20_top_words.png)

Polarity & subjectivity were plotted, for a visual representation of Sentiment Analysis.

![sentiment_analysis.png](images/sentiment_analysis.png)

Piecharts and bargraphs were plotted as an adjunct visual representation representing positive, neutral and negative tweets.

![piechart.png](images/piechart.png)

![bargraph.png](images/bargraph.png)

Algotrading was attempted.
We set arbitrary conditions for signal generation.
Sentiment values over 0.13 indicated a buy signal, values between 0.03 and 0.13 created no signal, and values less than 0.03 indicated a sell.
Assumptions were made that every long/short signal was acted on. If a short signal appeared when we were long, the trade would flip back to neutral then go short. The reverse is true.

Based on a hypothetical starting value of $1M, 3 short trades & 3 long trades were performed, leading to a final portfolio value of $1.547M.

# Limitations
Twitter API had two types of requests.
Full archive and cursor.
Full archive only allowed 50 requests per month
Cursor had a limitation of 500 tweets per time.
Using cursor searches, 200 tweets represented less than 1 minute of data.
Extrapolating it to a full 24 hour cycle, it would take more than 400,000 tweets in order for us to just 1 day of data.
The amount of computing power needed would be intense.
We managed to get around this by appending each day's top 100 tweets full archive search, for the past 30 days. For this project though, we ended up using 50 days worth of Twitter data.

# Problems Faced
Deciding on the scope and reach of the project.
Initially we wanted to come up with a dashboard of various cryptocurrencies based on what was the sentiment was on Twitter, compare various machine learning algorithms, find the best one to identify entry and exit points.
Due to the limited time frame, we quickly found that resources were being spread too thin, and subsequently decided to focus on one coin/token, and come up with a promising project which we could actually keep developing after this course.
Navigating through data was taxing, especially Twitter spam.

If we had more time & resources, instead of using only 100 tweets per day of twitter data, we could collate even more data to fine tune the model. Latest data would then be appended to our existing CSV/dataframe, our algorithm tested again and fine tuned.
We would also run the Algorithm live using real money to test performace.

# Conclusion
Using specific Twitter sentiment values as a guideline, signals for going long or short Bitcoin could definitely be profitable.

# Links
1. https://news.bitcoin.com/mayor-miami-treasury-reserves-bitcoin/
2. https://developer.twitter.com/en/dashboard
3. https://docs.tweepy.org/en/latest/index.html
4. https://pypi.org/project/yfinance/