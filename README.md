# Amazon_prime_EDA_Tableau_Dashboard
🎬 Amazon Prime Video — Content Intelligence

Exploratory Data Analysis & Interactive Tableau Dashboard on 9,800+ Titles and 124,000+ Cast/Crew Credits


📌 Overview

This project performs an end-to-end Exploratory Data Analysis (EDA) on Amazon Prime Video's US content catalogue, then rebuilds the same insights as a fully interactive, 4-page Tableau Public dashboard — so the findings can be explored by non-technical stakeholders, not just read as a static notebook.

Python EDA: 17 visualizations (univariate → bivariate → multivariate) in Google Colab
Tableau Dashboard: 11 charts across 4 themed, filterable, navigable dashboard pages
Business objective: turn a flat catalogue export into actionable insight for content acquisition, marketing, and investment teams
📂 Dataset
File	Rows	Description
titles.csv	9,871	Title metadata — type, genre, country, release year, runtime, IMDb/TMDb score & votes
credits.csv	124,235	Cast & crew credits per title — actor/director name, character, role

The two files join on the title id.

🛠️ Tools Used
Python — Pandas, NumPy, Matplotlib, Seaborn
Google Colab — notebook environment
Tableau Public — interactive dashboard
🧹 Data Cleaning & Transformation
Removed duplicate rows from both files
Parsed stringified list columns (genres, production_countries) into real lists with ast.literal_eval
Exploded genres/countries into long-format tables for accurate per-genre / per-country charting
Filled structural (non-random) missing values column-by-column — e.g. seasons only for SHOWs, 'Not Rated' for missing certifications
Derived decade, primary_genre, primary_country, and cast_crew_size for cleaner visualization
📊 Key Insights
The catalogue is 86% movies vs 14% shows, and title count grew sharply after 2015
Drama, Comedy, and Documentary dominate the genre mix; production is US/UK-heavy
IMDb and TMDb scores are strongly correlated, clustering around 6–7
Low-vote-count titles carry unreliable extreme scores — "Top Rated" lists should weight score by popularity, not use raw score alone
Larger credited productions (by cast/crew size) tend to have higher, more consistent ratings
📈 Tableau Dashboard

4 interactive pages, each with filters, tooltips, and navigation buttons:

Overview — Movies vs Shows, Titles by Release Year
Content Analysis — Top Genres, Top Countries, Age Certification
Ratings Analysis — Score by Genre, Ratings Distribution, IMDb vs TMDb
Cast & Crew Analysis — Top Directors, Top Actors, Cast Size vs Score

🔗 Live Dashboard: [https://public.tableau.com/app/profile/aman.kumar1620/viz/AmazonPrimeVideoEDADashboard/ContentAnalysis?publish=yes]

🎥 Video Walkthrough

🔗 [Add your video link here]

📁 Repository Contents
File	Description
Amazon_Prime_Video_EDA.ipynb	Full Python EDA notebook (17 charts)
titles.csv, credits.csv	Raw source data
titles_clean.csv, titles_genres_exploded.csv, titles_countries_exploded.csv, credits_clean.csv	Cleaned, Tableau-ready data
Amazon_Prime_Video_Dashboard.twbx	Packaged Tableau workbook
Amazon_Prime_Video_Dashboard_Documentation.docx	Full project documentation with dashboard screenshots
🚀 How to Run the Notebook
Open Amazon_Prime_Video_EDA.ipynb in Google Colab
Upload titles.csv and credits.csv to the Colab session (or mount Google Drive)
Run all cells: Runtime → Run all

👤 Author
Aman Kumar — Individual Project
