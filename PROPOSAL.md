# ML Project Proposal
- Lorin Fields
- Profit geyser. High market volatility trading machine. 

## What track are you choosing (analysis or engineering)?
Engineering
## What is your data source?
Market data provided by Interactive Brokers. The sentiment engine will pull from market data as well as select data feeds and news sources. 
## Summarize the status of your data and what cleaning is needed.
The data feeds I am getting should be very clean but will need to be formatted. I have not decided the exact sources for non-market based data. 

## Summarize the structure of your data and what models/techniques work with it.
The data will initially be from some historically high volatility security. The features will be price, volatility, timestamp as well as many other data points of interest.
The model to work with will generate a price direction, magnitude, and confidence. 

## What is your overall goal with this project?
The goal of this project is to build a machine that can predict with good probability which direction a high volatility security is likely to head next with a score of probable magnitude and the confidence of the prediction. There is a second element of this machine which is a mechanism to actually buy and sell based on predicted (buy) and actual (sell) value of the position. 

## Anything else you want to note about your project?
I understand this is a big project and I look forward to fine tuning the proposal before beginning. 

