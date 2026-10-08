# Amazon Prime Video — Exploratory Data Analysis

> **Portfolio focus:** Python • SQL-ready data thinking • Exploratory Data Analysis • Data Visualization • Business Analytics

## Business Problem

Streaming platforms need to understand the composition, evolution, ratings, popularity, and regional distribution of their content libraries. This project explores Amazon Prime Video catalog data to turn raw title and credit records into business-oriented findings.

## Objective

The analysis focuses on:

- Content mix: movies vs. TV shows
- Genre and production-country distribution
- Content growth over time
- Ratings and popularity patterns
- Runtime and season characteristics
- Cast and crew patterns
- Data quality issues that affect interpretation

## Dataset

The project uses two files:

- `titles.csv` — title-level metadata such as type, release year, certification, runtime, genres, production countries, seasons, IMDb/TMDB scores and popularity
- `credits.csv` — cast and crew information linked to titles

The repository contains the project assets and analysis notebook under the `amazon-prime-video-eda/` directory.

## Tools

| Area | Tools |
|---|---|
| Programming | Python |
| Data wrangling | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter / Google Colab-compatible workflow |
| Version control | Git, GitHub |

## Workflow

1. Load title and credit datasets
2. Inspect schema, missing values and duplicates
3. Clean and standardize fields
4. Transform multi-value categorical fields such as genres and production countries
5. Explore distributions and trends
6. Analyze ratings, popularity and runtime
7. Combine title-level and credit-level information where relevant
8. Visualize patterns
9. Translate analytical findings into business recommendations

## Analysis Areas

### Content Portfolio
- Distribution of movies and TV shows
- Dominant genres
- Production-country contribution
- Release-year trends

### Audience & Quality Signals
- IMDb/TMDB score distributions
- Popularity patterns
- Runtime characteristics
- Relationships between available rating/popularity measures

### People & Credits
- Actor and director frequency
- Contribution patterns across the catalog

## Key Insights

The current project analysis highlights:

- The Amazon Prime catalog contains a large and diverse set of titles spanning multiple genres and production regions.
- The data requires meaningful preprocessing because fields such as seasons, age certification, ratings, genres and production countries contain missing or multi-valued data.
- Ratings and popularity can be analyzed together to distinguish content quality signals from audience-interest signals.
- Credits data enables an additional view of frequently appearing actors and directors.

> **Evidence note:** This README intentionally avoids adding unsupported percentages or performance claims. Any quantitative result should be taken from the notebook outputs in the repository.

## Business Recommendations

Based on the analysis structure and documented findings:

1. Use genre and regional concentration to identify content portfolio gaps.
2. Combine rating and popularity signals when evaluating content rather than relying on one metric.
3. Track content-release trends over time to support acquisition and commissioning decisions.
4. Use recurring cast/crew patterns as an additional lens for portfolio concentration and talent strategy.

## Results

The project turns raw catalog and credits data into a structured exploratory view of content mix, temporal trends, ratings, popularity, and contributor patterns.

## Project Structure

```text
amazon-prime-video-eda/
├── README.md
└── amazon-prime-video-eda/
    └── analysis notebook / project files
```

## How to Run

1. Clone the repository.
2. Open the notebook/project files inside `amazon-prime-video-eda/`.
3. Install the analysis dependencies if they are not already available:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

4. Place `titles.csv` and `credits.csv` in the expected project data location.
5. Run the notebook from top to bottom.

## Portfolio Takeaway

This project demonstrates the core workflow expected from an entry-level Data Analyst: understand the business question, clean messy data, perform structured EDA, visualize patterns, and translate findings into decisions.
