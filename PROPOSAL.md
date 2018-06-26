# ML Project Proposal
- Darwin M. Johnson
- Real-time Twitter Trend Analyzer

## What track are you choosing (analysis or engineering)?
Engineering

## What is your data source?
[Twitter API](https://developer.twitter.com/en/docs/trends/trends-for-location/overview)

Strech Data: Google Trends API

[Coinbase API](https://developers.coinbase.com/docs/wallet/guides/price-data)

[IEX Trading API](https://iextrading.com/developer/docs/#getting-started)

## Summarize the status of your data and what cleaning is needed.
The data is being provided via web API's. I will make sure that critical pieces of the data provided are within acceptable ranges and are normalized in order to be able to carry out the requisite cross site data processing.

The aggregate data will exist in Spark RDD form. that will be broken down into some manageable size and/or time increment, to be decided. The rate of data storage will be key to the long term sustainabilty of the app existing as a continously running real-time streaming entity. I will target a data use rate that will stay within the storage and bandwidth confines of free or low end hosting tier.

Postgresql will be used as a data store for Spark and and the web site.

[PostGraphile](https://www.graphile.org/) provides GraphQL endpoints from a Postgres database. This will provide web API access to the collected data. 

## Summarize the structure of your data and what models/techniques work with it.

I will employ a mix of techniques to get the data sources producing an interesting graph. There will be tweets, trends and sentiment to analyze and graph. I will start with this but part of the process will be digging deeper into what data these API's provide. 

Some of the techniques I anticipate using are:

NLP Sentiment Analysis

Linear Regression

Logistic Regression

Clustering


## What is your overall goal with this project?
I want to create an graph, that show some meaningful information in a visually pleasing form. The ultimate success of this app is, someone choosing to display this on their television during a party as a conversation piece (sure it might be a nerdy party).

The output will be a web based visualization/animation built on D3. I would like there to be enough going on that you would want to look at the graph for more than a bit and you can tell that something is happening in realtime. However the data updates should happen at a pace that is perceived as slow, so that the graph doesn't demand attention in a room.

Stretch Goal: User controls to make adjustments to the graph.

Stretchier Goal: Data generated audio track.

## Anything else you want to note about your project?

This project will be built around pySpark initially. The idea is to make use of Spark's streaming and analysis capabilities, in a production stack. There will be data visualization available separately on the web interface. 

This is also the first step in putting together a complete Scala/Spark ML/DS Stack, in the future.  A priority follow-up project would be to translate the project from pySpark into Scala.

I suspect being able to work in Scala, will expand my options in the job market.

This blog post talks about Python Libraries that we're familiar with:

[Python Data Science Libraries](https://medium.com/activewizards-machine-learning-company/top-15-python-libraries-for-data-science-in-in-2017-ab61b4f9b4a7)

The same author talks about analogs in the Scala world:

[Scala Data Science Libraries](https://medium.com/activewizards-machine-learning-company/top-15-scala-libraries-for-data-science-in-2018-4b2cb5c5367e)

The idea is that I could make the move to Scala from Python in a modular fashion.