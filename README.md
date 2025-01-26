# Amazon Product Review Analysis
## Overview
This project analyzes Amazon product reviews data stored in an SQLite database. The main objective of this project is to explore user behavior, product popularity, and review sentiment, along with determining which users Amazon can recommend more products to based on their purchasing behavior and review patterns.

For Dataset go to the link: https://drive.google.com/file/d/1IoTcM2yXrBKzGqGRjUMZdsOY1u_FUdwl/view?usp=drive_link

## Key Features and Analysis
### Reading Data from SQLite Database:
The project begins by reading data from an SQLite database containing Amazon product reviews using sqlite3.
The review data includes features like ProductId, UserId, Score, Text, Summary, and Time (timestamp).

### Data Cleaning and Preparation:
Basic data wrangling steps, such as removing invalid rows and duplicates.
The "Time" feature, originally in int64 format, is converted to a proper datetime format to facilitate time-based analysis.

### User Recommendations for More Products:
The project identifies top users who have a higher probability of purchasing more products. The analysis suggests that Amazon can recommend more products to users who have a better conversion rate (i.e., those who purchase more items).
The top 10 users are highlighted based on their review activity, which can serve as the target audience for product recommendations.

### Identifying Products with Good Number of Reviews:
The analysis includes finding out which products have a significant number of reviews. 

### Behavioral Differences Between Frequent and Infrequent Viewers:
A comparison between frequent and infrequent reviewers reveals insights into their review patterns. 'Frequent users' tend to give more discerning feedback (less extreme ratings), while 'infrequent users' may be more extreme in their ratings.

### Text Analysis and Word Count Distribution:
A detailed analysis of whether frequent users are more verbose in their reviews compared to infrequent users.
Results suggest that frequent reviewers typically write longer reviews, whereas infrequent reviewers often write shorter reviews.

### Sentiment Analysis:
Sentiment analysis is performed on review texts to understand the overall sentiment (positive, negative, or neutral) expressed by users.
The TextBlob library is used to compute sentiment polarity for each review, helping to determine the overall sentiment distribution across the reviews.

## Technologies Used
SQLite for data storage and querying
### Python Libraries:
1. pandas for data manipulation
2. numpy for numerical operations
3. matplotlib and seaborn for data visualization
4. sqlite3 for database interaction
5. TextBlob for sentiment analysis
6. collections.Counter for counting and frequency analysis
