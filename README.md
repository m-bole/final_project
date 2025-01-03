# Programming Basics and Technical Data Analysis – Final Project

## Project Overview
This project encompasses a variety of data analysis tasks, ranging from cleaning and preprocessing raw data to conducting exploratory data analysis (EDA) and performing natural language processing (NLP). The final deliverables include cleaned datasets, visualizations, and detailed analyses, all documented in Python notebooks. The project adheres to the requirements outlined in the assignment description, and the final submission includes:

- **Cleaned data** in `.csv` format.
- **Python notebooks** in `.ipynb` format for each major section.
- A folder structure that facilitates reproducibility and easy navigation.

---

## Project Tasks

### Part 1 - Processing and Cleaning the Data
Tasks performed:
1. **Replace Abbreviated Weekday Names:** Abbreviated weekday names in the `created_at` column were replaced with their full English equivalents.
2. **Replace Abbreviated Month Names:** Abbreviated month names in the `user_created_at` column were converted to numerical equivalents (e.g., `Jun` to `06`).
3. **Extract Tweet Links:** All links to tweets were extracted and stored in a separate list.
4. **Extract Links from Tweets:** All links in the `urls` column were extracted and stored in a separate list.
5. **Extract Image Links:** All image links from the `media` column were extracted and stored in a separate list.
6. **Remove Stopwords:** All stopwords in the `text` column were removed, and the cleaned text was saved in a new column, `text_without_stopwords`.

---

### Part 2 - Exploratory Data Analysis (EDA)
Tasks performed:
1. **Top 5 Tweets by Likes:** Listed the top 5 tweets with the highest number of likes.
2. **Top 5 Tweets by Retweets:** Listed the top 5 tweets with the highest number of retweets.
3. **Non-sensitive Tweets:** Filtered tweets not considered 'sensitive' (`possibly_sensitive` column).
4. **Earliest Account Tweets:** Displayed tweets from the user who created their account the earliest.
5. **Most Followed User:** Displayed tweets from the user with the most followers.
6. **Verified Users:** Showed tweets from verified users.
7. **Most Frequent Posting Day:** Identified the most frequent day of the week for tweets in the dataset.

---

### Part 3 - Natural Language Processing (NLP)

**Task:** Extract named entities (people, places, organizations) from the `text` column.

**Model Choice:** Initially, PolDeepNer was considered for this task due to its specificity to Polish NER. However, due to compatibility and runtime issues, an alternative model, **`allegro/herbert-base-cased`**, from Hugging Face’s model hub was used.

- **Justification:**
    - The Hugging Face model is pre-trained on Polish text and supports NER tasks effectively.
    - It integrates seamlessly with modern NLP libraries and is straightforward to use in Python.

A separate notebook (`final_NER.ipyb`) documents the process of loading the model, extracting named entities, and saving results in `processed_dane1_with_entities.csv`.

---

### Part 4 - Visualization

**Task:** Create a graph showing the number of tweets per day of the week using Matplotlib.

Steps:
1. The `weekday` column, created during data cleaning, was used to group tweets by day of the week.
2. A bar graph was plotted to show the distribution of tweets across the week.

