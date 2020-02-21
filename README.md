# Comparative Analysis of Article Sentiment to Market Price of Apple

## Intro

For this project, I do not have any of the code, as I ran this on a Linux partition on my hard drive which I accidentally wiped;
however I do have some of the scraped data which I used in my analysis as well as the comparative graph result between the cumulative
sentiment based on the news article headlines and the closing price of the day.

## Scraping

For scraping the data, I used beautifulsoup4, a python library for scraping data from the webpage through patterns; however in more recent projects, I have realized that a more efficient and direct method of scraping data from websites is to make requests to the APIs which the websites pull data from themselves, from which I can parse the raw data much more efficiently. I pulled headlines from a few websites, including: the motley fool and cnn, which are the 2 files displayed here.

For the stock market closing price data, I used the CSV of Apple's historical price data from NASDAQ's website, with NASDAQ being the exchange in which Apple stock is traded.

## Algorithm

For the Sentiment Analysis, while I cannot recall which specific algorithm I had used, I used one of Natural Language Toolkit's (NLTK) pretrained algorithms (most likely Naive-Bayes), and got the sentiment of each of the news articles.


## Data comparison

To combine it all, I aggregated all of the news headline data with each row containing the article title, sentiment of title, and date, and for the articles which were written on the same date, I took the average of the sentiments. I then cumulatively added the sentiment of each data to the overall sentiment of Apple and normalized this data; then, I normalized the market closing price of Apple over the same time span, and displayed both on the same graph.

![Sentiment vs. Price](IMG_9827 (2).JPG)

The data contains many visible consistencies between each other, such as the peak from 2011 to 2013 as well as the overall growth of the share price
overtime.

## Issues

This comparative analysis contains many possible issues which could be improved upon, such as inconsistent data frequency of news headlines as well as inaccurate sentiment analysis from the pre-trained algorithm; I still find this project to be a success as it provided a basic proof of the correlation between article headline sentiment of stock and daily price of stock.

## Future

In the future, I plan to work on a more detailed version of this project, creating a Naive Bayes Classifier which is trained using a wider dataset of news article headlines from multiple companies. If this works with low error, it would be interesting to use this as an agent in a simulated stock market enviroment, and see how well it performs based off of analyzing the sentiment of news articles related to specific companies.
