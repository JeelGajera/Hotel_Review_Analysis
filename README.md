# Summary of the Analysis
- The analysis focuses on hotel reviews, aiming to gain insights into sentiment patterns, distribution across locations, and common themes in positive and negative reviews. Here's a breakdown of the analysis:

- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1z0RBT31ohmAX4O84ImjzdiKWcxID6o89?usp=sharing)

## Data Description:

The dataset contains information on hotel reviews, including the review text, date, and location.
There are 6,448 entries with three columns: Review, date, and Location.
Missing values exist in the 'Review' and 'Location' columns.

1. Data Pre-Processing:
- Unnecessary phrases such as "Read more" and "Read less" were removed from the 'Review' column.
- Null values were removed from the dataset.
- The 'date' column was formatted into a datetime format.

2. Sentiment Analysis:
- Natural Language Toolkit (NLTK) library was employed for sentiment analysis.
- Text data underwent pre-processing steps, including lowercasing, removal of punctuation and numbers, tokenization, stop word removal, and stemming.
- SentimentIntensityAnalyzer from NLTK was used to calculate sentiment compound scores.
- Reviews were classified as positive or negative based on a defined threshold (0.2).
- Sentiment distribution across locations was analyzed, and the positive percentage was calculated for each location.

3. Exploratory Data Analysis (EDA):

- Various visualizations were generated using Matplotlib, Plotly and Seaborn to explore sentiment distribution, positive percentage by location, and sentiment trends over time.

- Top locations with the highest review counts were identified and analyzed for sentiment distribution.

4. Common Words in Positive and Negative Reviews:
- The most common words in positive and negative reviews were identified.
- Positive reviews frequently mentioned words such as `room, hotel, staff, great, stay, clean, locat, nice, good, friendli`
- Negative reviews commonly included words like `room, hotel, check, stay, staff, park, time, bed, desk`

5. Word Clouds:
- Word clouds were generated for both positive and negative reviews, providing a visual representation of the most frequent words in each sentiment category.


## Interesting Insights:

### 1. Positive Sentiment Trends Over Time:

Overall, the sentiment trends over time indicate a positive sentiment among reviewers. 
Based on the figure-6:
-  The figure  shows that the sentiment trends fluctuated over time for each location, but generally showed a positive trend.
- USA and New York had the gradual increase in sentiment score over time.
- Canada and California had the lowest sentiment score during Sep 2018 to Jan 2019. After that trends are increased.
- San Jose had the highest sentiment score during Sep 2018 to Mar 2019, After that trends are decreased. that shows a negative impact on the San Jose Location.

### 2. Top Locations with Positive Reviews:

Some locations stand out with a higher percentage of positive reviews, suggesting areas where hotels are more likely to receive positive feedback.
- Location with the highest positive reviews
    - USA, New York, San Jose, California and Canada has the highest positive reviews. This suggests that the hotels are more liked by the customers.
    - Chicago and Washington has the zero nagative reviews.
    - for more location review Figure - 2

- Location with the low positive reviews
    - Puerto Rico, Atlanta GA, Florida and Oregon have the lowest positive reviews.
    - for more location review Figure - 4

- Distribution of Reviews count the number of reviews with percentage of positivity. 
    - 717 (95-100%) reviews.
    - 278 (0-5%) reviews. 
    - 10 (20-35%) reviews.
    - 37 (45-45%) reviews.
    - 45 (60-80%) reviews.
    - for more reiew Figure - 3

### 3. Common Themes in Positive Reviews:

Positive reviews commonly mention aspects like clean rooms, friendly staff. This highlights key factors contributing to positive guest experiences.

- Word Cloud of Positive Reviews (Figure-7): The figure is a colorful word cloud that shows the most frequent words in positive reviews for hotels. The size of the words indicates their relative frequency, with larger words being more common. 

- Key Words in Positive Reviews: The key words in positive reviews are `“room,” “hotel,” “staff,” “clean,” “nice,” “location,” and “stay.”` These words suggest that positive reviews often focus on the quality of the room, the hotel facilities and services, the staff’s friendliness and professionalism, the cleanliness of the hotel, the pleasant atmosphere, the convenient location, and the overall experience during the stay.

### 4. Common Themes in Negative Reviews:

Negative reviews often mention issues with rooms, check-in processes, and staff. Addressing these specific pain points could lead to improved customer satisfaction.

- Word Cloud of Negative Reviews (Figure-8): The figure is a colorful word cloud that shows the most frequent words in negative reviews for hotels. The size of the words indicates their relative frequency, with larger words being more common.

- Key Words in Negative Reviews: the key words in negative reviews are `“room,” “hotel,” “check,” “stay,” and “staff.”` These words suggest that negative reviews often mention issues with the room quality, the hotel facilities and services, the check-in and check-out processes, the overall experience during the stay, and the staff’s attitude and professionalism. Words like `“park,” “desk,” “bed,” and “time”` could also indicate specific problems guests might have faced, such as parking fees, front desk delays, uncomfortable beds, or long waiting times.

### 5. Temporal Patterns in Sentiment:

Analyzing sentiment trends over time reveals potential seasonal patterns or events affecting customer sentiments. Identifying such patterns can help hotels tailor their services to specific times of the year.

- Sentiment Trends Over Time (Figure-5): The figure shows how the sentiment scores of hotel reviews changed over time from September 2018 to July 2019. The sentiment score ranges from 0 to 1, where higher values indicate more positive sentiments.

- Fluctuations and Patterns: The figure reveals that the sentiment trends fluctuated over time, with no clear pattern of consistent increase or decrease. 
    - November 2018 had the lowest sentiment score of 0.087, indicating a high level of dissatisfaction among customers.
    - August 2019 had the highest sentiment score of 0.9952, indicating a high level of satisfaction among customers
    - Feburary 2019 to May 2019 had the significant drops of sentiment scores.
    - September 2018 to January 2019 had significant increases in the sentiment scores.

