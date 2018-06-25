# ML Project Proposal
- Darwin M. Johnson
- Real-time Trend Analyzer

## What track are you choosing (analysis or engineering)?
Engineering

## What is your data source?
Twitter Api
Google Trends API
Coinbase API
[IEX Trading API](https://iextrading.com/developer/docs/#getting-started)

## Summarize the status of your data and what cleaning is needed.
The data is being provided by the web api's. I will make sure that critical pieces of the data provided are within 
acceptable ranges and are normalized in order to be able to carry out the requisite cross site data analysis.

## Summarize the structure of your data and what models/techniques work with it.
NLP Sentiment Analysis
Linear Regression
Logistic Regression
Clustering


## What is your overall goal with this project?
Building a web app that provides realtime analysis of trends that are of two distinct classes. One class are web trends on Google search, Twitter and Instagram. The other class of trends are financial. Data to monitor these trends  will be provided by the IEX Trading and the Coinbase API's.  

## Anything else you want to note about your project?

I am looking to base this project around Spark I will write the Spark porting of the app in Scala. I would like to use it's streaming capabilities to do query the api's and to do most of the analysis. There will be data visualization available on the web interface. In addition there will be the ability to focus on trends that are occuring in realtime and see how they relate to other trends sources through the web front end.

I also am invested in putting together a rather complete Scala/Spark ML/DS Stack. 

These two blog posts talk about Python Libraries that we're familiar with:
[Python Data Science Libraries](https://medium.com/activewizards-machine-learning-company/top-15-python-libraries-for-data-science-in-in-2017-ab61b4f9b4a7)

[Scala Data Science Libraries](https://medium.com/activewizards-machine-learning-company/top-15-scala-libraries-for-data-science-in-2018-4b2cb5c5367e)