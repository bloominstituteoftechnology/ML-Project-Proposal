# ML Project Proposal
- Raymond Heberer
- Implement Baseline RL Models on DeepMind Starcraft II Environment

## What track are you choosing (analysis or engineering)?
Engineering

## What is your data source?
[Starcraft 2 Replays](https://github.com/Blizzard/s2client-proto#replay-packs)

## Summarize the status of your data and what cleaning is needed.
The dataset was prepared by DeepMind and Blizzard Entertainment as part of their initiatize to create a [Starcraft II AI Research Environment](https://deepmind.com/blog/deepmind-and-blizzard-open-starcraft-ii-ai-research-environment/).

Working with the data will require familiarization with the [PySC2](https://github.com/deepmind/PySC2) learning environment, and likely features from the Starcraft game engine. Data Cleaning in the traditional sense, with DataFrames and tools like pandas, will probably not be that applicable, as this is a research dataset, and not one scraped from the wild.

## Summarize the structure of your data and what models/techniques work with it.
The individual replays contain both pixel data and game features (such as current minerals), in a time series. Baseline reinforcement learning models are provided along with the learning environment that can be trained on replay data. Reinforcement learning models at each timestep receive percepts (observable) from the environment, as well as rewards. This combined with their previous action is used to learn a policy mapping percepts to actions.

## What is your overall goal with this project?
For the initial 2 weeks, my only goal is to become familiar with the learning environment provided by DeepMind. I will do this be implementing the provided baselines, as well as reimplementing a simple baseline (such as A2C) to do toy problems such as gathering minerals. Currently, deep learning approaches still underperform relative to the hand-engineered computer agents, so I do not have high expectations for how the baseline models will perform in a full game.

By investing this time to learn the environment and API, I will be able to have a platform and skillset with which to reimplement current research on StarCraft II, and maybe try out original architectures and techniques on my own by the time I graduate from Lambda Schoool.

## Anything else you want to note about your project?
I have previous experience in implementing deep learning models in Tensorflow, as well as with reinforcement learning. The main challenge here really is in getting to know the software tools and APIs.