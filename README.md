
# 🎬 **FilmFortune-A-Predictive-Study-on-Movie-Revenue-and-Viewer-Sentiment**



This project aims to predict the box office success of movies using IMDB/Kaggle metadata and analyze viewer sentiment based on plot summaries. By applying sentiment analysis (VADER) and regression modeling (Sklearn), the study uncovers patterns between emotional tone, ratings, and commercial outcomes.

---

## 📌 Objective

- Predict box office gross revenue of movies using metadata (budget, ratings, sentiment).
- Perform sentiment analysis on plot summaries using VADER.
- Explore genre-wise sentiment trends and visualizations.
- Export an interactive Excel dashboard with all key insights.

---

## 🛠 Tools & Libraries

| Tool       | Purpose                          |
|------------|----------------------------------|
| **Python** | Programming language             |
| `NLTK` + `VADER` | Sentiment analysis of plot summaries |
| `Scikit-learn` | Linear Regression modeling   |
| `Pandas` / `NumPy` | Data manipulation        |
| `Seaborn` / `Matplotlib` | Visualizations      |
| **Excel**  | Pivot tables, analytics export   |

---

## 📂 Dataset

- Source: IMDB Movie Metadata (from Kaggle)
- Sample fields: `movie_title`, `budget`, `gross`, `imdb_score`, `genres`, `plot_keywords`, etc.

---

## 🔄 Workflow

### 1. Data Loading & Cleaning
- Imported CSV dataset.
- Handled missing values using median, mode, or "Unknown" appropriately.
- Converted numerical types for modeling.

### 2. Sentiment Analysis
- Applied VADER to `plot_keywords` to generate `Sentiment_Score`.
- Combined with budget and IMDB score for predictions.

### 3. Model Building
- Linear Regression model using:
  - Features: `budget`, `imdb_score`, `Sentiment_Score`
  - Target: `gross`
- Evaluated using R² Score and RMSE.

### 4. Visualization
- Sentiment distribution by genre (bar chart)
- IMDB score vs Gross revenue (line plot)
- Budget vs Gross (scatter)

### 5. Excel Dashboard Output
- ✅ `Data_Predictions` — Dataset with predicted gross
- ✅ `Genre_Sentiment_Pivot` — Avg. sentiment & count by genre
- ✅ `Genre_Gross_Pivot` — Mean, sum, and count of gross revenue by genre
- ✅ `Rating_vs_Budget_Gross` — IMDB score vs budget/gross
- ✅ `Model_Summary` — R² Score and RMSE
- ✅ `Descriptive_Stats` — Summary statistics

---

## 📊 Sample Output

```plaintext
Model R² Score: 0.031
Root Mean Squared Error (RMSE): ~72,305,097
