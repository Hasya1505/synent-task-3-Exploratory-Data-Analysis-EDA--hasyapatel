# Netflix Content Analysis (EDA Project)

## Project Overview

With the massive amount of content on Netflix, I wanted to dig into the data to see what actually drives the platform. This project isn't just about plotting charts; it’s about finding the underlying patterns in how Netflix builds its library.

I focused on a few core questions:
* What does the growth curve look like over the last decade?
* Which genres dominate the catalog?
* Is there actually a link between how popular a show is and its rating?
* Who are the biggest geographical contributors?

---

## Dataset & Data Challenges

I worked with a dataset of about 16,000 titles. While the data was rich, it had some specific issues that required manual fixing:

* **Missing Data:** The `duration` column was entirely empty, so I had to drop it from the analysis.
* **Cleaning multi-values:** The `genres` column was a mess—multiple categories were crammed into single cells. I had to write logic to split these so I could count individual genre frequencies accurately.
* **Key Columns:** I focused heavily on `vote_average` for quality, `popularity` for reach, and `release_year` for trends.

---

## My Workflow

### 1. Initial Data Probe
I started by checking the basic info (`df.info()`) to see where the null values were hiding and to understand the distribution of the data types.

### 2. The Cleanup Phase
Raw data is rarely ready for plotting. I spent time:
* Scrubbing duplicates.
* Standardizing date formats.
* Exploding the genre and country columns so that a movie listed in both "Drama" and "Thriller" gets counted in both categories.

### 3. Feature Engineering
I added a few custom columns to make the charts more readable:
* **Decades:** Grouping years into blocks (e.g., 2010s) to see long-term shifts.
* **Rating Tiers:** Categorizing `vote_average` into Low, Mid, and High brackets.
* **Popularity Segments:** Breaking down the popularity scores into easier-to-digest groups.

### 4. Deep Dive Analysis
I looked at the data from three angles:
* **Distributions:** Checking how ratings are spread out (mostly around the 6-7 mark).
* **Comparisons:** Looking at Genre vs. Rating and Country vs. Popularity.
* **Correlations:** I ran a correlation matrix and found something surprising: Popularity and Ratings have almost zero connection. High-quality content isn't always what's trending.

---

## What I Learned (Key Insights)

* **The 2015 Pivot:** There is a massive jump in content production starting in 2015. This clearly marks when Netflix shifted its strategy toward aggressive original content growth.
* **Genre Trends:** Drama is the undisputed king of the platform, with Comedy and Thriller following behind.
* **The "Hidden Gem" Effect:** I found a lot of titles with very high ratings but near-zero popularity scores. This suggests that Netflix has a "long tail" of quality content that doesn't always get promoted.
* **US Dominance vs. Global Quality:** While the US produces the most volume, many international titles actually hold higher average ratings.

---

## Final Thoughts

This project showed me that Netflix's strategy seems to favor variety and volume. The fact that popularity doesn't correlate with quality suggests that their recommendation algorithm is likely driving "popular" trends regardless of the actual user rating.

## Next Steps
In the future, I want to use this cleaned data to build a basic recommendation engine and perhaps pull in a separate dataset for user reviews to see if the "hidden gems" I found have a specific cult following.

---

**Author:** Hasya Patel  
**Tech Stack:** Python, Pandas, Matplotlib, Seaborn
