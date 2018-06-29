# ML Project Proposal
- Jasper Jenkins
- Santander Value Prediction (https://www.kaggle.com/c/santander-value-prediction-challenge/leaderboard) 
- Progessively Growing GAN (https://arxiv.org/abs/1710.10196) or AUTO-GAN (Differentiable Architecture Search (https://arxiv.org/abs/1806.09055) / Efficient Neural Architecture Search via Parameter Sharing (https://arxiv.org/abs/1802.03268) for GAN architecture search)

## What track are you choosing (analysis or engineering)?
- Analysis (Santander) 
- idk (GANS)

## What is your data source?
#### Santander
- Kaggle
#### GANS
- Scraping Google images (any images, not well studied, possibly insufficient data)
- LSUN bedroom images (boring, well studied)
- Celeb Face images (weird, well studied)
- Cifar 10 (but small images, well studied)
## Summarize the status of your data and what cleaning is needed.
#### Santander
- Completely anonymized
- 5000~ columns
- 5000~ training rows
- 25000~ testing rows
- If it has missing values we don't know
- Very sparse
- Some columns in training set completely sparse or duplicate while being unique and non-sparse in testing set
- Likely timeseries of currency transactions
#### GANS
- Filter out bad images manually from scraping if using scraped images

## Summarize the structure of your data and what models/techniques work with it.
#### Santander

##### Dimensionality Reduction
- Filter columns based on model gain
- PCA
- Truncated SVD
- Gaussian Mixture
- Independent Component Analysis
- Rowwise statistics (mean, sum, unique-count, min, max, std, skew, kurtosis)
- Computing above on subset of columns from binning of columnwise stats(mean, sparsity%)
- Same as above, but subsetting by clustering the columns(treating them as rows)

##### Models
- LightGBM
- XGBoost
- CatBoost
- Bagging Simpler Regressions
- Stacking Ensemble of above
- Dynamic Ensemble Selection

##### Other
- Cross-validation averaged over different seeds
- Adversarial validation
- Deanonymize columns, they appear to be 9 chars from a hexdigest, write cuda program to check every 9 character slice of common hash algos (sha1, sha256, md5, etc.) with a dictionary of common spanish financial and column names from previous santander competitions. Run on a google VM with a P100.

#### PR-GAN
- Image augmentation to increase dataset size
- Improved Wasserstein training setup
- Resnet-like discriminator
- DCGAN generator
- Possibly use image resampling to avoid artifacting in generator (https://distill.pub/2016/deconv-checkerboard/)
- Possibly use spectral normalization (https://arxiv.org/abs/1802.05957)
#### AUTO-GAN
- Use existing implementation of DARTS or ENAS
- Mostly same techniques
- Probably keep one side static, likely discriminator
- Use inception score to gauge how well model does

## What is your overall goal with this project?
#### Santander
- Low RMSLE
#### PR-GAN
- Modular Architecture setup to make working with images of different dimensions in the future easy
- Images with decent realism and diversity (avoid mode collapse)
#### AUTO-GAN
- Combine two fairly new areas of research
- Satiate curiosity

## Anything else you want to note about your project?
#### AUTO-GAN
- Could be impractical due to training time
- Current GAN architectures are quite linear. State-of-the-art results for image classification are non-linear (resnet, resnext)
- One of the most successful GAN architectures, PR-GAN, uses a progressively grown linear architecture. Progressively increasing maximum allowed parameters for architecure search with an increasing resolution target could work well.