# 🎬 Netflix Data Analysis

This project performs a comprehensive exploratory data analysis (EDA) on a dataset of Netflix movies and TV shows. The primary goal is to analyze the content library to uncover patterns and trends that can inform data-driven decisions regarding content acquisition, production, and regional strategy.

Beyond the EDA, this notebook also builds two simple content-based models:
1.  A **recommendation engine** using TF-IDF and cosine similarity.
2.  A **KMeans clustering** model to group titles based on their descriptions.

---

## 📊 Dataset

The dataset contains listings of all movies and TV shows available on Netflix as of mid-2021, with over 8,800 unique titles.

* **Source:** `https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/000/940/original/netflix.csv`
* **Key Columns:** `title`, `type` (Movie/TV Show), `director`, `cast`, `country`, `release_year`, `rating`, `duration`, and `listed_in` (genre).

---

## 🛠️ Tools and Libraries Used

* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn, Wordcloud
* **Machine Learning / NLP:** Scikit-learn (TfidfVectorizer, linear_kernel, TruncatedSVD, KMeans)

---

## 🔍 Key Analyses and Questions

This project answers 20 key questions about the Netflix library, including:

* What is the ratio of Movies vs. TV Shows on the platform?
* Which genres are the most popular and which dominate in specific countries (e.g., US vs. Rest of World)?
* What are the top 10 countries for content production?
* Which content ratings are most frequent, and which countries produce the most mature content?
* When did Netflix add the most content, and which months are most popular for new releases?
* Who are the top 10 most frequent directors and actors?
* What is the average duration of a movie, and what is the most common number of seasons for a TV show?
* Is there a discernible trend in movie durations over the years?

---

## 💡 Key Findings (Summary)

* **Content Mix:** The library is movie-heavy (**~69% Movies** vs. 31% TV Shows), but the volume of TV shows has grown steadily.
* **Top Genres:** **International Movies, Dramas,** and **Comedies** are the most common genres globally.
* **Top Producers:** The **USA, India,** and the **UK** are the top 3 content producers.
* **Audience Target:** The most common ratings are **TV-MA** and **TV-14**, indicating a strong focus on adult and teen audiences.
* **Show Length:** The vast majority of TV shows on Netflix are **1 Season long**, suggesting a high volume of new or limited series.
* **Content Peak:** The peak year for adding new content to the platform was **2019**.

---

## 🤖 Models and Features

Beyond the EDA, this notebook also demonstrates two simple content-based models:

1.  **Content-Based Recommender:** A simple recommendation system was built using **TF-IDF** on the `description` column. It calculates the **cosine similarity** (`linear_kernel`) between titles to recommend the top 6 most similar items.
2.  **Description-Based Clustering:** Titles were clustered into 8 thematic groups using **TruncatedSVD** (for dimensionality reduction) and **KMeans clustering** on the TF-IDF vectors.

---

## 🚀 How to Use

1.  Clone the repository:
    ```sh
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/Shre1100/Mini-Project-Netflix-Data-Analysis.git)
    ```
2.  Navigate to the directory:
    ```sh
    cd Mini-Project-Netflix-Data-Analysis
    ```
3.  Install the required libraries:
    ```sh
    pip install pandas numpy matplotlib seaborn scikit-learn wordcloud
    ```
4.  Open and run the `Netflix_Data_Analysis.ipynb` notebook in Jupyter.

---

## ⚠️ Limitations

* **Missing Data:** A significant amount of data for `director`, `cast`, and `country` was missing and imputed as "Unknown," which could skew aggregations.
* **No Viewership Data:** This analysis is based on content *availability*, not *popularity*. There is no data on view counts, watch time, or user ratings.

---

## 📜 License

This project is licensed under the [Your License Name](LICENSE).
