# 📊 Netflix Content Analysis (EDA Project)

## 📌 Problem Statement

With so much content available on Netflix, it becomes difficult to understand what actually works well.
In this project, I tried to explore questions like:

* How has Netflix content grown over the years?
* Which genres are most common on the platform?
* Does more popular content always mean better quality?
* Which countries contribute the most to Netflix content?

The goal was not just to analyze data, but to **understand patterns that could help in content decisions**.

---

## 📂 Dataset Details

The dataset contains around **16,000 Netflix titles**, including both movies and TV shows.

### Main columns used:

* `vote_average` → used as rating (quality indicator)
* `popularity` → shows how much attention a title gets
* `release_year` → helps in trend analysis
* `genres` → type of content (like Drama, Comedy, etc.)
* `country` → where the content is produced
* `director`, `cast` → for deeper analysis

### Things I noticed while working:

* The `duration` column was completely empty, so I ignored it
* Some columns (like genres) had multiple values in one cell, so I had to split them properly

---

## ⚙️ Approach

I followed a step-by-step approach while working on this dataset:

### 🔹 1. Understanding the Data

First, I explored the dataset structure to understand:

* What kind of data is available
* Which columns are useful
* Where problems like missing values exist

---

### 🔹 2. Data Cleaning

Then I cleaned the data:

* Removed duplicates
* Handled missing values
* Fixed date formats
* Broke down multi-value columns (like genres)

This step was important because raw data is usually messy.

---

### 🔹 3. Feature Engineering

To make analysis better, I created some new features:

* Grouped years into decades (like 2000s, 2010s)
* Categorized content into low/medium/high ratings
* Split popularity into segments

This helped in simplifying complex patterns.

---

### 🔹 4. Exploratory Data Analysis

#### ✔ Univariate Analysis

I looked at individual columns:

* Rating distribution
* Most common genres

#### ✔ Bivariate Analysis

Then I compared variables:

* Genre vs rating
* Country vs popularity

#### ✔ Correlation Check

I checked how numerical values relate to each other.
One interesting thing I noticed was that **popularity and rating are not strongly connected**.

---

### 🔹 5. Trend Analysis

I also analyzed how things changed over time:

* Content increased rapidly after 2015
* Some genres became more common in recent years

This part helped in understanding Netflix’s growth.

---

## 📈 Results & Insights

Here are some key things I found:

* 📌 **Content Growth:**
  There is a clear spike in content after 2015. This shows Netflix expanded aggressively during this period.

* 🎭 **Genre Distribution:**
  Drama is the most common genre, followed by Comedy and Thriller.

* ⭐ **Popularity vs Rating:**
  I expected popular content to have high ratings, but that was not always true. The relationship is actually very weak.

* 🌍 **Country Contribution:**
  The United States produces most of the content, but other countries also contribute some high-quality titles.

* 💡 **Interesting Observation:**
  Some highly rated content has very low popularity, which means good content is sometimes hidden.

---

## 🧠 Conclusion

From this analysis, I understood that:

* Netflix focuses more on **content quantity and variety**
* Popular content is not always the best-rated
* Growth after 2015 played a major role in shaping the platform
* There is a mix of global content contributing to quality

Overall, this project helped me understand how real-world data behaves and how insights are not always obvious.

---

## 🚀 Future Improvements

If I continue this project, I would like to:

* Build a recommendation system
* Use machine learning to predict content success
* Create dashboards for better visualization
* Analyze user reviews if available

---

## 🛠️ Tools Used

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Jupyter Notebook

---

## 👨‍💻 Author

**Hasya Patel**

