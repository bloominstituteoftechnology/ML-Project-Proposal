# ML Project Proposal
- Jason Fleischer
- Sentiment Analysis and Clustering of Supreme Court Opinions

## What track are you choosing (analysis or engineering)?
Analysis

## What is your data source?
Supreme Court Orders obtained from The Free Law Project
The Supreme Court Database from Washington University Law

## Summarize the status of your data and what cleaning is needed.
The Free Law Project aims, amongst other things, to "provide free, public, and permanent access to primary legal materials on the Internet". In pursuit of this mission it has created, for every order of the Supreme Court of the United States, JSON files that contain important metadata and the plaintext or html of each order.

The Supreme Court Database's Modern Database has every Supreme Court case from 1946-2017 with up to 247 features per case.  It has multiple file formats available, including .csv.  This database will be used to associate features with the text of each opinion obtained from The Free Law Project.  Important features from the database include Justice votes, legal issues decided, case disposition, origin of case, case parties, and the lower court case disposition.

First, I will need to programmatically clean the orders.  I will remove orders without opinions (such as dispositions of petitions for a writ of certiorari) and then parse the opinions into their type (majority, dissenting, concurring, plurality, in part, per curiam, etc.).  This will take some time, but should be relatively straightforward because Supreme Court opinions take on a regular form.  The plaintext and html will need to be parsed separately. Then I will have to remove headers, citations, punctuation, and other extraneous text from each opinion.  I will need to keep each string of text associated with the type of opinion, case name, and term of the Court.

Then, I need to reliably id each opinion and associate it with the data from The Supreme Court Database.  This can be done by first matching the case name from the Supreme Court Database with the case name from the opinion.  Where it doesn't match exactly, I can modify the string by removing punctuation and common abbreviations as per "The Bluebook: A Uniform System of Citation", a style guide used in the legal field.  If opinions are still not matched to the database, I will have to write more complicated logic (such as stemming the case name further, but also making sure the term matches).

I will also try to extract other features from each opinion, such as word frequency, average sentence/ paragraph/ section length, and citation frequency.

## Summarize the structure of your data and what models/techniques work with it.
After splitting the data into separate opinions, each opinion will be a string of words.  These will need to be tokenized, and then stemmed or lemmatized to be used in nltk's VADER for sentiment analysis.

After performing sentiment analysis on each opinion, I can combine the sentiment scores with features from the Supreme Court Database and those I extracted and use a clustering algorithm to sort the opinions.

## What is your overall goal with this project?
I would like to produce an analysis of Supreme Court opinions that may shed light on the sentiment of the different types of opinions, the Justices, and their ideological approaches. I would also like to see whether a clustering algorithm may shed light on new or old ways to group Justices or whether it will place opinions back into Justice-centered clusters.

## Anything else you want to note about your project?
I am looking into more ways to perform sentiment or textual analysis other than VADER.

If time permits, I can try to write a script that will use API calls to get the latest opinions from The Free Law Project, automatically perform sentiment analysis on it, and post it to a website.
