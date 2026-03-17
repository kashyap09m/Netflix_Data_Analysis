# 🎬 Netflix Movies & TV Shows — Exploratory Data Analysis

<div align="center">

![Netflix EDA Banner](https://img.shields.io/badge/Netflix-EDA-E50914?style=for-the-badge&logo=netflix&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?style=for-the-badge&logo=pandas&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

<br/>

> **A comprehensive end-to-end Exploratory Data Analysis on ~9,800 Netflix titles** sourced from TMDB (The Movie Database) — uncovering genre trends, language distributions, rating patterns, popularity metrics, and much more.

<br/>

</div>

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Key Insights](#-key-insights)
- [Project Structure](#-project-structure)
- [Analysis Sections](#-analysis-sections)
- [Getting Started](#-getting-started)
- [Requirements](#-requirements)
- [Business Questions Answered](#-business-questions-answered)
- [Future Work](#-future-work)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Project Overview

This project performs a **thorough Exploratory Data Analysis (EDA)** on Netflix's content catalog. The goal is to extract actionable insights from raw data using Python's data analysis and visualization ecosystem.

The analysis covers:
- 📊 **Statistical summaries** of all key features
- 🎭 **Genre-level deep dives** — popularity, ratings, and trends
- 🌍 **Language analysis** — English vs non-English content patterns
- 📅 **Temporal trends** — how Netflix content has grown over the years
- 🏆 **Top performers** — most popular, highest rated, most voted titles
- 🔗 **Correlation analysis** — relationships between popularity, votes, and ratings
- ❓ **6 business questions** answered with data

---

## 📂 Dataset Description

**Source:** TMDB (The Movie Database) via Kaggle  
**File:** `netflix.csv`  
**Size:** ~9,800 rows × 9 columns

| Column | Type | Description |
|--------|------|-------------|
| `Release_Date` | `datetime` | Date the title was released |
| `Title` | `string` | Name of the movie or TV show |
| `Overview` | `string` | Short synopsis / description |
| `Popularity` | `float` | TMDB popularity score |
| `Vote_Count` | `int` | Total number of user votes |
| `Vote_Average` | `float` | Average user rating (0 – 10 scale) |
| `Original_Language` | `string` | ISO language code (e.g., `en`, `ja`, `ko`) |
| `Genre` | `string` | Comma-separated list of genres |
| `Poster_Url` | `string` | URL to the official poster image |

---

## 🔑 Key Insights

| # | Insight |
|---|---------|
| 🥇 | **Drama dominates** — The most common genre with 3,744 titles, followed by Comedy and Action |
| 🌐 | **English is dominant** — ~77% of the catalog is in English; Japanese & Korean lead non-English |
| 📈 | **2021 was the peak year** — 714 titles released, the highest in dataset history |
| ⭐ | **Average rating: 6.2/10** — Only ~33% of titles score ≥ 7.0, making quality rare |
| 🔥 | **Popularity is skewed** — A handful of blockbusters dominate popularity metrics |
| 📅 | **January & September** are the busiest release months |
| 🎭 | **Action & Adventure** score highest in popularity; **History** leads in ratings |
| 🔗 | **Weak correlation** between popularity and ratings — virality ≠ quality |
| 🌏 | **Non-English content** makes up ~23% and is growing year-over-year |
| 🏆 | **Spider-Man: No Way Home** tops the popularity chart |

---

## 🗂️ Project Structure

```
netflix-eda/
│
├── 📓 Netflix_EDA_Complete.ipynb   ← Main analysis notebook (13 sections)
├── 📄 README.md                    ← Project documentation (this file)
├── 📊 netflix.csv                  ← Dataset (place here before running)
└── 📄 requirements.txt             ← Python dependencies
```

---

## 📋 Analysis Sections

The notebook is organized into **13 well-structured sections**:

```
Section 01 — 📦 Import Libraries
Section 02 — 📥 Load Dataset
Section 03 — 🔍 Initial Data Inspection
Section 04 — 🧹 Data Cleaning & Preprocessing
           ├── 4.1 Missing Values Analysis
           ├── 4.2 Data Type Conversion
           ├── 4.3 Duplicate Check
           └── 4.4 Genre Column Expansion
Section 05 — 📊 Univariate Analysis
           ├── 5.1 Popularity Distribution
           ├── 5.2 Vote Average Distribution
           └── 5.3 Vote Count Distribution
Section 06 — 🎭 Genre Analysis
           ├── 6.1 Top 15 Genres by Count
           ├── 6.2 Genre Share Pie Chart
           ├── 6.3 Average Rating per Genre
           └── 6.4 Average Popularity per Genre
Section 07 — 🌍 Language Analysis
           ├── 7.1 Top 15 Original Languages
           ├── 7.2 Avg Rating by Language
           └── 7.3 English vs Non-English Share
Section 08 — 📅 Release Date & Time Analysis
           ├── 8.1 Content Released per Year
           ├── 8.2 Content Released per Month
           └── 8.3 Avg Popularity Over Years
Section 09 — 🔗 Bivariate & Correlation Analysis
           ├── 9.1 Correlation Heatmap
           ├── 9.2 Popularity vs Vote Average (Scatter)
           ├── 9.3 Vote Count vs Vote Average
           └── 9.4 Box Plots Across Top Genres
Section 10 — 🏆 Top & Bottom Performers
           ├── 10.1 Top 10 Most Popular Titles
           ├── 10.2 Top 10 Highest Rated (min 500 votes)
           └── 10.3 Top 10 Most Voted Titles
Section 11 — 📊 Advanced Analysis
           ├── 11.1 Rating Category Distribution
           ├── 11.2 Genre × Year Heatmap
           ├── 11.3 Genre Trend Line Chart
           └── 11.4 Popularity by Language (Violin Plot)
Section 12 — ❓ Business Questions Answered (6 Q&As)
Section 13 — 📝 Summary & Key Insights
```

---


## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/netflix-eda.git
cd netflix-eda
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Add the dataset

Place the `netflix.csv` file in the root project directory (same level as the notebook).

### 4. Launch Jupyter Notebook

```bash
jupyter notebook Netflix_EDA_Complete.ipynb
```

### 5. Run all cells

Use **Kernel → Restart & Run All** to execute the complete analysis from top to bottom.

---

## 📦 Requirements

```
python >= 3.9
pandas >= 1.5.0
numpy >= 1.23.0
matplotlib >= 3.6.0
seaborn >= 0.12.0
jupyter >= 1.0.0
```

**`requirements.txt`:**

```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0
```

---

## ❓ Business Questions Answered

The notebook answers these 6 data-driven business questions:

| # | Question | Finding |
|---|----------|---------|
| Q1 | Which genre has the highest average vote rating? | **History / Documentary** genre leads in avg rating |
| Q2 | Which year had the most releases? | **2021** — with 714 titles |
| Q3 | What % of content is non-English? | **~23%** of the catalog |
| Q4 | Which month sees the most releases? | **January** is the busiest release month |
| Q5 | What fraction of titles are 'Good' or better (≥ 7.0)? | **~33%** of all titles |
| Q6 | Which non-English language has the highest avg popularity? | **Korean** content tops non-English popularity |

---

## 🔮 Future Work

- [ ] 🤖 Build a **content-based recommendation system** using genre + overview text (TF-IDF / cosine similarity)
- [ ] 💬 Apply **NLP sentiment analysis** on the `Overview` column
- [ ] 📊 Implement a **weighted Bayesian rating formula** (similar to IMDb's approach)
- [ ] 📈 Deep-dive on **non-English content growth** year-over-year
- [ ] 🔵 Use **K-Means clustering** to group similar titles
- [ ] 🌐 Build an interactive **Streamlit / Dash dashboard** for live filtering
- [ ] 🗺️ Choropleth map of **content by country of origin**

---

## 🤝 Contributing

Contributions, suggestions, and pull requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

Please make sure your code follows PEP 8 style guidelines and includes relevant comments.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- Dataset sourced from **TMDB (The Movie Database)** via Kaggle
- Analysis inspired by Netflix EDA tutorials on YouTube
- Visualization powered by **Matplotlib** and **Seaborn**

---

<div align="center">

Made with ❤️ and 🐍 Python

⭐ **Star this repo** if you found it useful!

</div>
