# 🎬 Amazon Prime Video Content Analysis — EDA

## 📌 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** of the Amazon Prime Video content library available in the United States.

The objective is to analyze the platform's movies and TV shows to understand **content distribution, growth trends, audience ratings, popularity, runtime patterns, age certifications, and contributor information**.

The analysis uses Python-based data cleaning, transformation, statistical exploration, and visualization techniques to convert raw streaming data into meaningful business insights.

---

## 🎯 Business Problem

Streaming platforms contain thousands of movies and TV shows, making it difficult to understand:

* What type of content dominates the platform?
* How has the content library changed over time?
* Which genres and regions contribute the most content?
* How are audience ratings distributed?
* Which titles receive the most audience attention?
* What runtime patterns exist across the content library?
* How do movies and TV shows differ in terms of ratings and popularity?
* Which actors and directors appear most frequently?

This project addresses these questions through systematic exploratory data analysis.

---

## 💼 Business Objective

The main objective is to analyze Amazon Prime Video's content data to understand:

* Content-type distribution
* Content growth over time
* Genre and regional representation
* Audience ratings and popularity
* Runtime patterns
* Audience targeting through age certifications
* Actor and director contribution

These insights can support **content investment, content planning, audience targeting, and user-engagement strategies**.

---

## 📊 Dataset

The project uses two datasets:

### `titles.csv`

Contains information about Amazon Prime Video movies and TV shows, including:

| Column                 | Description                  |
| ---------------------- | ---------------------------- |
| `id`                   | Unique title ID              |
| `title`                | Movie or TV show name        |
| `show_type`            | Movie or TV Show             |
| `description`          | Content description          |
| `release_year`         | Release year                 |
| `age_certification`    | Audience age certification   |
| `runtime`              | Runtime in minutes           |
| `genres`               | Content genres               |
| `production_countries` | Production country/countries |
| `seasons`              | Number of seasons            |
| `imdb_id`              | IMDb identifier              |
| `imdb_score`           | IMDb rating                  |
| `imdb_votes`           | Number of IMDb votes         |
| `tmdb_popularity`      | TMDB popularity score        |
| `tmdb_score`           | TMDB rating                  |

### `credits.csv`

Contains information about people associated with each title:

| Column           | Description         |
| ---------------- | ------------------- |
| `person_id`      | Unique person ID    |
| `id`             | Title ID            |
| `name`           | Actor/director name |
| `character_name` | Character played    |
| `role`           | Actor or Director   |

The notebook describes `titles.csv` as containing more than 9,000 unique titles and `credits.csv` as containing more than 124,000 actor/director records.

---

## 🛠️ Tech Stack

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical operations
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Jupyter Notebook / Google Colab**

---

## 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Loading
     ↓
Data Exploration
     ↓
Missing Value Analysis
     ↓
Duplicate Detection
     ↓
Data Cleaning & Wrangling
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
Data Visualization
     ↓
Business Insights
     ↓
Recommendations
```

---

## 🧹 Data Cleaning & Preparation

The project performs several data-wrangling operations before analysis:

* Renamed the content-type column to `show_type`
* Merged the titles and credits datasets using `id`
* Removed duplicate records
* Handled missing age certifications
* Filled missing seasons with `0`
* Imputed missing IMDb and TMDB scores using median values
* Filled missing IMDb votes and TMDB popularity with `0`
* Corrected numerical data types
* Cleaned genre and production-country text values
* Handled missing actor/director information
* Removed records with invalid runtime values
* Created a `decade` feature from `release_year`
* Created a `runtime_category` feature
* Separated actor and director records
* Reset the final dataframe index

These steps prepared the combined dataset for reliable exploratory analysis.

---

## 📈 Exploratory Data Analysis

The project follows a structured visualization approach covering categorical, numerical, and time-based relationships.

### Key Areas Analyzed

#### 1. Content Type

* Movies vs TV Shows
* Distribution of content types

#### 2. Content Growth

* Content growth over release years
* Titles per decade
* Movies per decade
* TV shows per decade

#### 3. Ratings

* IMDb score distribution
* TMDB score distribution
* Average IMDb score by decade
* Average IMDb score by content type
* Average TMDB score by content type

#### 4. Runtime

* Runtime distribution
* Runtime categories
* Average runtime by decade
* Runtime category trends across decades

#### 5. Audience & Popularity

* IMDb vote distribution
* TMDB popularity distribution
* Age certification distribution

#### 6. Contributors

* Top actors by appearances
* Top directors by number of titles

## The notebook contains **20 charts** covering these different analytical dimensions.

## 🔍 Key Insights

### 🎥 Movies vs TV Shows

The analysis shows that **movies are substantially more numerous than TV shows** in the analyzed content library.

This indicates a strong movie-oriented content presence while also highlighting an opportunity to examine whether the comparatively smaller TV-show library could affect long-term engagement.

### 📈 Content Growth

Content has **increased significantly in recent years**, with recent decades containing substantially more titles than older periods.

This reflects the expansion of streaming content and increasing investment in newer titles.

### ⭐ Ratings

IMDb ratings are concentrated largely in the **5–7 range**, indicating that much of the catalog falls within a moderate rating range.

The analysis also compares rating behavior across decades and between movies and TV shows.

### ⏱️ Runtime

Most content falls within the **medium-runtime category**, while short and long content represents smaller portions of the library.

This provides useful information for understanding content-duration patterns and audience preferences.

### 📊 Popularity

IMDb votes and TMDB popularity are highly concentrated: **a relatively small number of titles receive much higher audience attention**, while many titles have comparatively low engagement.

This suggests that content performance is uneven across the catalog.

### 🎭 Actors & Directors

## The analysis indicates that a small number of actors and directors appear across a relatively large number of titles, showing concentration among frequently involved contributors.

## 💡 Business Recommendations

Based on the analysis, the following strategies are suggested:

1. **Focus on high-rated content**
   Prioritize content characteristics associated with stronger audience ratings.

2. **Maintain a strong recent-content pipeline**
   Recent content represents a significant portion of the analyzed library.

3. **Optimize content duration**
   Medium-duration content represents a major part of the catalog, which can be considered when planning future content.

4. **Diversify the content library**
   Avoid over-concentration in specific runtime categories, age groups, genres, or regions.

5. **Leverage high-performing contributors**
   Frequently appearing actors and productive directors can be considered for future collaborations and promotional strategies.

6. **Improve discovery of less-popular titles**
   Since audience attention is concentrated on a relatively small number of titles, recommendation and promotional strategies could help improve visibility across the broader catalog.

The notebook's final recommendation similarly emphasizes high-rated, medium-duration content while maintaining diversity across runtime categories, age groups, and regions.

---

## 📌 Conclusion

This project demonstrates how exploratory data analysis can be used to understand a large streaming-content catalog and convert raw data into business-oriented insights.

The analysis highlights patterns in **content type, content growth, ratings, popularity, runtime, age certifications, actors, and directors**.

Overall, the findings emphasize the importance of balancing **high-quality and audience-preferred content with sufficient content diversity** to support user satisfaction, content planning, and long-term platform growth.

---

## 📂 Repository Structure

```text
Amazon-Prime-Video-EDA/
│
├── 📓 Project_EDA_Submission_Template.ipynb
├── 📄 README.md
├── 📄 requirements.txt
│
├── 📁 data/
│   ├── titles.csv
│   └── credits.csv
│
└── 📁 images/
    └── visualization screenshots
```

> **Note:** If the dataset files are not included in the repository, update this section with instructions explaining where the datasets should be obtained and where they should be placed.

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Amazon-Prime-Video-EDA.git
```

### 2. Navigate to the project

```bash
cd Amazon-Prime-Video-EDA
```

### 3. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Project_EDA_Submission_Template.ipynb
```

### Google Colab

The notebook can also be executed using **Google Colab** after uploading or connecting the required CSV datasets.

---

## 📊 Project Highlights

| Category                | Details                   |
| ----------------------- | ------------------------- |
| Project Type            | Exploratory Data Analysis |
| Domain                  | OTT / Streaming           |
| Platform Analyzed       | Amazon Prime Video        |
| Geographic Scope        | United States             |
| Datasets                | Titles + Credits          |
| Programming Language    | Python                    |
| Visualization Libraries | Matplotlib, Seaborn       |
| Data Processing         | Pandas, NumPy             |
| Visualizations          | 20                        |
| Contribution            | Individual                |
| Author                  | Tushar                    |

---

## 👨‍💻 Author

**Tushar**

This project was completed as an individual EDA capstone project.

---

## ⭐ If You Found This Project Useful

Feel free to explore the notebook, review the analysis, and use the project as a reference for learning exploratory data analysis and business-oriented data visualization.
