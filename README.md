# Final Project: Programming Basics and Technical Data Analysis

## Project Overview
This project focuses on analyzing a dataset of tweets, performing data cleaning, exploratory analysis, natural language processing (NLP), and visualization. output are saved in the `output` folder, while the main processing logic resides in the Jupyter Notebook (`final_project.ipynb`).

## Features
### Part 1: Data Cleaning
- **Weekday Conversion**: Abbreviated weekdays converted to full names (e.g., `Mon` -> `Monday`).
- **Month Conversion**: Abbreviated months replaced with numeric equivalents (e.g., `Jan` -> `01`).
- **Clean Date Column**: Added a new column in the `DD.MM.YYYY` format (additional step by me).
- **Stopword Removal**: Removed unnecessary words from the tweet text.
- **Extracted Links**: Extracted tweet, media, and URL links. Data saved to `.txt` files.

### Part 2: Exploratory Data Analysis
- Identified:
  - Top 5 tweets by likes and retweets.
  - Tweets by verified users.
  - Tweets from the earliest account and the most-followed user.
  - Most common day for tweets.
- Saved analysis results to individual CSV files in the `output` folder.

### Part 3: Natural Language Processing
- Extracted:
  - People (`persons`)
  - Places (`places`)
  - Organizations (`organisations`)
- Created respective columns in the processed dataset.

### Part 4: Visualization
- Generated a bar chart showing the number of tweets per weekday.
- Saved the chart as `tweets_per_day.png` in the `output` folder.

## Output
All results are saved in the `output` folder:
1. `processed_tweets.csv`: Fully processed dataset.
2. `tweet_links.txt`: List of tweet URLs.
3. `url_links.txt`: List of URLs found in tweets.
4. `media_links.txt`: List of media links.
5. `top_likes.csv`: Top 5 tweets by likes.
6. `top_retweets.csv`: Top 5 tweets by retweets.
7. `earliest_user_tweets.csv`: Tweets from the earliest created account.
8. `most_followed_tweets.csv`: Tweets from the most-followed user.
9. `verified_users.csv`: Tweets from verified users.
10. `tweets_per_day.png`: Visualization of tweet frequency by weekday.

## Requirements
- Python 3.8+
- Required libraries are listed in `requirements.txt`. Install them using:
  ```bash
  pip install -r requirements.txt
  ```

## Usage
1. **Set Up Environment**:
   ```bash
   python -m venv env
   source env/bin/activate
   pip install -r requirements.txt
   ```

2. **Run the Notebook**:
   Open `final_project.ipynb` in Jupyter Notebook or JupyterLab and execute all cells.

3. **View output**:
   Check the `output` folder for all processed results and visualizations.

## Folder Structure
```
project-root/
│
├── final_project.ipynb  # Jupyter Notebook containing all processing logic
├── dane1.csv            # Input dataset
├── requirements.txt     # Required libraries
│
├── output/
│   ├── processed_tweets.csv
│   ├── tweet_links.txt
│   ├── url_links.txt
│   ├── media_links.txt
│   ├── top_likes.csv
│   ├── top_retweets.csv
│   ├── earliest_user_tweets.csv
│   ├── most_followed_tweets.csv
│   ├── verified_users.csv
│   └── tweets_per_day.png
│
└── README.md            # Project documentation
```

## Acknowledgments
- This project uses the `pl_core_news_lg` SpaCy model for processing Polish text.
