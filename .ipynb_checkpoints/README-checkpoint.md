# project2 CryptoKnight
Crypto investing for all

# Motivation
The year is 2021.
Bitcoin (and cryptocurrency) is ubiquitous to all involved in the Fintech space.
The premise of 'Will it survive?' has been replaced with 'To what extent can Bitcoin fluorish?' 
Retail & Institutions have entered.
Local governments are coming in with Miami looking at investing some of city's treasury reserves in Bitcoin.
Who will be the next? Which nation states will be first?
Like it or not, Bitcoin and cryptocurrencies are here to stay.
What better way to get on the Bitcoin bandwagon, than to learn to potentially time one's entry.
We aim to come up with a guide on potential entry and exits for Bitcoin based on Twitter sentiment and its correlation to Bitcoin price.

# Hypothesis
Sentiment on Twitter has a high correlation with the price action of Bitcoin.
Potentially guiding entry and exit points.

# Data Collection
Utilised Twitter API & 'Tweepy' python package, we searched an archive of tweets mentioning the term 'Bitcoin' over the past 30 days.
Data was cleaned, dataframes created and data appended.

# Analysis
TextBlob was a new library package we used to obtain subjectivity, polarity & sentiment.
Wordclouds and graphs were created with top appearing words in the past 30 days.
Sentiment and price action was overlayed.

# Limitations
Twitter API had two types of requests.
Full archive and cursor.
Full archive only allowed 50 requests per month
Cursor had a limitation of 500 tweets per time.
Using cursor searches, 200 tweets represented less than 1 minute of data.
Extrapolating it to a full 24 hour cycle, it would take more than 400,000 tweets in order for us to just 1 day of data.
The amount of computing power needed would be intense.
We managed to get around this by appending each day's full archive search, for the past 30 days.

# Problems Faced
Deciding on the scope and reach of the project.
Initially we wanted to come up with a dashboard of various cryptocurrencies based on what was the sentiment was on Twitter, compare various machine learning algorithms, find the best one to identify entry and exit points.
Due to the limited time frame, we quickly found that resources were being too thin, and subsequently decided to focus on one coin/token, and give a good project.
Navigating through data, especially Twitter spam.
If we had more time, we could compare multiple machien learning trading algorithms, choose the strongest model with acceptable pricision scores, test our trade hypothesis parameters, then automate the trades.

# Conclusion
??Twitter sentiment had a high correlation to Bitcoin price action.

# Links
https://developer.twitter.com/en/dashboard
https://docs.tweepy.org/en/latest/index.html
https://news.bitcoin.com/mayor-miami-treasury-reserves-bitcoin/