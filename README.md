# ML-Project-Proposal

The purpose of this repo is to guide and solicit project proposals from ML
students at Lambda School. There are two project tracks:

- **Analysis**: derive insights from a dataset, and generate a professional and
polished report. Deliverable can be a writeup (e.g. whitepaper, blog series) or
presentation (slides and preferably recorded video), or both.
- **Engineering**: build a system that processes data using ML approaches and
exposes the results as an API to facilitate applications. Deliverable is a
deployed and documented API web service, with a simple demo app as part of the
documentation.

An example of the analysis track would be to use data about bike sharing systems
to summarize their usage patterns, social and transit impact, and predict what
the future may hold for them and what cities they will do well or poorly in.
Generating visualizations that portray data geographically would be a great way
to make this particular project stand out.

An example of the engineering track would be to use data about movies to build a
recommender system that accepts as input some information about movies a user
likes or dislikes, and returns as output more movies they may like. As a stretch
goal it could offer a variety of strategies or approaches to recommendations,
and by default use an ensemble technique to blend them.

You must choose *one* of these tracks for your project - both will entail
similar ML techniques, but the end result and a fair amount of your time
investment will be different. If you're uncertain which track you want, talk
with Lambda School staff and we'll help you decide - and remember you will have
more projects in your future, and can always choose a different focus later on.

After picking your track, your next task is to get data. Choosing, obtaining,
and cleaning the data is all part of the project, and you may have to try a few
datasets before one really works for you. Some resources to get started:

- https://archive.ics.uci.edu/ml/index.php
- https://github.com/awesomedata/awesome-public-datasets
- https://elitedatascience.com/datasets
- https://cloud.google.com/public-datasets/
- https://registry.opendata.aws/
- https://blog.bigml.com/list-of-public-data-sources-fit-for-machine-learning/

Your choice of data will shape the techniques available to you. Key questions to
ask about your data:

- How clean and consistent is your data?
  - Does it have missing values you might want to impute?
  - Are there outliers, weird strings, unexpected types, or other warning signs?
  - Was it gathered/sampled in a way representative of the true population?
- What are the fundamental types of your variables?
  - Do you have numeric/continuous values (e.g. money)?
  - Do you have ordinal values (e.g. rating scales)?
  - Do you have categorical values (e.g. product type)?
- How structured is your data?
  - Is it labeled (for the qualities you're interested in) or unlabeled?
  - Is there one or more dependent variables (something you want to predict)?
  - What are the independent variables (values you want to predict with)?

Think about these issues (and more) as you explore your data, and regardless of
your chosen track you should take notes and write a summary of what your data
is, what issues it has, and how you will mitigate these. This is where you need
to think back over the many techniques we've covered and pick the appropriate
tools to handle the problem at hand.

You should spend 1-2 days working on the above, and then you should open a PR to
this repository where you fill out the template in the `PROPOSAL.md` file to
describe your planned project. You will have another ~1.5 weeks to work on this
project, so choose a scope that is appropriate. Thanks, and good luck!
