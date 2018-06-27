# ML Project Proposal
- Navjot
- Resume Assistant for job applicants (given a resume and a job description, highlight parts that could be improved)

## What track are you choosing (analysis or engineering)?
Engineering

## What is your data source?
**Resumes:**
1. (Quality dataset): collect resumes for LambdaSchool students (as per Ryan we can get couple of hundred web dev resumes)
2. (Secondary dataset): http://opensource.indeedeng.io/api-documentation/docs/resume/
3. (Other options): scraping other job websites, linkedIn API

**Job descriptions:**
1. http://opensource.indeedeng.io/api-documentation/docs/job-search/
2. scraping job websites if neded

## Summarize the status of your data and what cleaning is needed.
Haven't looked into the above sources with depth, but some common steps which will be needed regardless:
- anonymization: detect personal information like named entities, phone-numbers, emails etc – and convert them to XXX
- traditional NLP cleaning steps as per need

## Summarize the structure of your data and what models/techniques work with it.
**structure:** Textual

**models/techniques:** relevant NLP techniques (tf-idf, CRF, word embeddings, CNN, LSTM)

## What is your overall goal with this project?
**2 goals:**
1. Overall goal is to ship something which is usable by the end consumer (i.e. it is working to some extent)
2. Explore LSTMs in depth (practical implementation point of view), and explore the entire lifecyle of a NLP project end to end – starting from baselines, ending with the state-of-the-art Deep Learning models

There has been some work in this area using Deep Learning, but mostly its focused on the hiring end of the spectrum by hiring agencies. In this project, idea is to focus on the resume improvement, for the job applicant. The services/products which exist in this space seem to be mostly using rule-based parsers – so there is scope of improvement.

The target of this project is NOT to suggest edits (that's a much harder thing to do) – but to highlight areas which could be improved (which is close to detecting areas which are not a strong match)

**MVP:** at the bare minimum, given a resume and a job description, determine what % of a match it is

**Future goal:** given a resume, and a job description – tweak the resume to best fit the job desription

## Anything else you want to note about your project?
Collecting quality resumes could be a real blocker, would like to use Lambda School's help for that.
