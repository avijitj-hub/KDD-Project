# KDD-Project

### Project: Prediction for trending videos on YouTube in USA.

### Team:
1. Narendra Pahuja
2. Akshay Popli
3. Monika Chandrashekara
4. Prerana Chandrashekar
5. Avijit

Data and source description:
Trending YouTube Statistics by Mitchell J,Kaggel datasets
The dataset contains several months  of data on daily trending YouTube videos. We have selected data for US for our Analytics.
The dataset has following attributes:
video_id
trending_date
title
channel_title
category_id
publish_time
tags
views
likes
dislikes
comment_count
thumbnail_link
comments_disabled
ratings_disabled
video_error_or_removed
description
URL of the source:https://www.kaggle.com/datasnaek/youtube-new#US_category_id.json

Data Understanding and EDA

Using this data we will Analyse how these factors will affect on the popularity of the videos


Data Preparation:
1. We will merge data from Json and csv file considering id and category_id respectively as common reference to get the category title of video.
2. After merging we will convert the date column in proper format.
3. Clean data by removing redundant.
4. Pre-process the missing values.
5. Visualize the data with differnet plots to find the correlation between variables.

Machine Learning

Evaluation

Conclusion


Application of the CRISP-DM Process (this is the group plan - this can be altered as the project progresses and new knowledge is gained - this will be a summary of the work to be completed - the main information will be in the notebook(s) in code and markdown)
The project aims at predicting the trending videos based on number of views,likes,unlikes,number of comments,published date and trending date
Establishes relationship between popularity and likes

