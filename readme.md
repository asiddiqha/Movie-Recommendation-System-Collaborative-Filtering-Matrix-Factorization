# Movie Recommendation System

A movie recommendation system built using collaborative filtering and matrix factorization on the MovieLens 1M dataset.

## What I Built

I implemented and compared multiple recommendation approaches:

- Item-based collaborative filtering using Pearson correlation
- Item-item cosine similarity
- KNN-based movie recommendations
- User-user cosine similarity
- Matrix factorization using SVD
- User and movie latent embeddings

## Dataset

The dataset contains:

- 1,000,209 ratings
- 6,040 users
- 3,883 movies in the catalogue
- 3,706 movies with ratings
- 95.53% user-movie matrix sparsity

The raw `.dat` files are not included in this repository.

## Analysis

I performed:

- Data validation and cleaning
- Feature engineering
- Exploratory data analysis
- Movie popularity and rating analysis
- User and movie behaviour analysis
- Sparse matrix representation using CSR
- Similarity-based recommendations
- Matrix factorization and embedding analysis

## Matrix Factorization

I implemented SVD with 4 latent factors and evaluated it using RMSE and MAPE.

| Model | RMSE | MAPE |
|---|---:|---:|
| Global Mean Baseline | 1.118 | 38.22% |
| SVD — 4 Factors | **0.867** | **26.49%** |
| SVD — Temporal Split | 0.880 | 28.32% |

The final SVD model was also used to generate 4-dimensional user and movie embeddings.

## Example Recommendation

For `Liar Liar (1997)`, the Pearson-based recommender returned:

| Movie | Pearson Similarity |
|---|---:|
| Mrs. Doubtfire (1993) | 0.500 |
| Dumb & Dumber (1994) | 0.460 |
| Ace Ventura: Pet Detective (1994) | 0.459 |
| Home Alone (1990) | 0.456 |
| The Wedding Singer (1998) | 0.429 |

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- SciPy
- Surprise
- Matplotlib
- Seaborn
- Google Collab