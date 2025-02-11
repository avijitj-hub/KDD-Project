### KDD-Project

### Instruction to run the project
1. Take the clone of repository in local system.
2. As our dataset or .csv file is zipped, you need to unzip that, the only you will be able to access the dataset.
3. Then Run jupyter file, you will be able to access the dataframe.

### Project: Prediction for trending videos on YouTube in USA.
The objective of the project is to predict number of views for a trending videos based on the number of likes, dislikes, number of comments, published date and trending date. 

### Team:
1. Narendra Pahuja
2. Akshay Popli
3. Avijit Jaiswal
4. Prerana Chandrashekar
5. Monika Chandrashekara

### Data and source description:
In this project we are using Trending YouTube Statistics by Mitchell J, Kaggle datasets. 
This dataset includes several months (and counting) of data on daily trending YouTube videos. Data is included for the US, GB, DE, CA, FR, RU, MX, KR, JP and IN regions (USA, Great Britain, Germany, Canada, France, Russia, Mexico, South Korea, Japan and India respectively), with up to 200 listed trending videos per day. We have selected US for our Analytics.
The dataset has following attributes:
* video_id – ID of the video
* trending_date – Date the video started to trend
* title – Title of the video 
* channel_title – Channel title of the video
* category_id – Category ID of the video 
* publish_time – Time the video was published
* tags – Places this video was tagged
* views – Number of views for the video
* likes – Number of likes for the video
* dislikes – Number of dislikes for the video
* comment_count – Number of comments for the video
* thumbnail_link – Links to thumbnail this video
* comments_disabled – States True if the comments for the video is disabled else False
* ratings_disabled – States True if the rating is disabled for the video else False
* video_error_or_removed – States True if the video has any error or if it is removed else states False.
* description – Description of the video

URL of the source: https://www.kaggle.com/datasnaek/youtube-new#USvideos.csv

### Application of the CRISP-DM Process: 

#### Domain Knowledge (document sources):
The YouTube trending video dataset link: https://www.kaggle.com/datasnaek/youtube-new#USvideos.csv

#### * Data Understanding and EDA:
EDA is the process of visualizing and analyzing data to extract insights from it.It helps in summarizing important characteristics of data in order to gain better understanding of the dataset.The relation between variables in the YouTube trending dataset is analyzed using graphical representation. The categorical and numerical features are studied to gain better understanding of the dataset to perform machine learning algorithms on the dataset.We have analyzed the data using various graphs and plots like bar plots, box whisker plot etc to uncover important relations between the data.

#### Data Preparation:
1. Merged data from Json and csv file considering id and category_id respectively as common reference to get the category title of video.
2. After merging converted the date column to datatime format.
3. Cleaned data by removing redundant values.
4. Handled the missing values in description column.
5. Removed the pipelines in tags column.
6. Changed the format of Trending date and Published time to Datetime datatype.
7. A new column is added as "number of days" which shows the number of days between Trending date and Published date.
8. Dropped the records where Trending date is lesser than Publish date, because it is not possible for a video to trend even before its published.
9. The columns views, likes, dislikes are evaluated to see if they are normally distributed or not.
10. Different groups of views are created using binning.
11. Visualized the data with different plots to find the correlation between variables.


#### Handling Discrimination and bias:
There is no bias in our dataset as it does not contain any user related information.so we dont need to handle discrimination and bias

#### Machine Learning:
This is project we have used a Random Forest Regression model to predict the number of views based on various columns like number of likes, number of dislikes and the number of comments.Higher the number of likes, dislikes and comments indicates that the video has higher number of views.By using this model we get a accurate predictions because Random Forest model uses a combined knowledge wherein the result from various decision trees is aggregated to give a final predictor.We can also see that there variables used to predict the number of views are highly co-reralted. We choose the best features inorder to make the predictions because we wanted to provide the model with optimal informations to make accurate prediction  <br><br> 

#### Evaluation:
YouTube trending video data set is analyzed in this project. Random Forest Regression and logistic regression are used to predict the number of views for trending videos. For both Random Forest Regression and Logistic Regression the accuracy of the training and test set is almost equal, from this we can say the model is not overfit or underfit. The accuracy for predicting the number of views is high for both Random Forest Regression (97.69 %) and Logistic Regression(97.18 %). Since the accuracy is greater for Random Forest Regression, it is best model to predict the number of views for YouTube trending data set.
The random forest model used to predict the number of views is giving a good accuracy rate, the the accuracy score on  both train and test model is very close this means the model is capable of making accurate predictions without overfitting or underfitting the data.
Evaluated popularity based on likes and comments.
Evaluated positive or negative comments based on category. 


### Interesting Features and Finding
1. Videos that belongs to "Entertainment" has highest count.
2. The category "Music videos" has received the increased number of views, likes and comments.
3. Games category has the maximum number of likes and the views are 5000000.
4. The correlation matrix showed the high correlation between views, likes, dislikes and comment count.
5. Other finding we got is, the maximum videos published in 2017 and 2018.
6. Entertainment and Music videos trended on same day they published as number of days between it published and trended is Zero(0).
7. Film and Animation category of videos got more than 100000 views on the day they released.
8. The number of videos published from June to November is minimal.
9. No videos going to be in trend in the month of July, August, September, October.
10. Maximum number of videos published between 2pm to 6pm of the day.

### Conclusion and Important Results:
The YouTube trending dataset is used to predict the type of video trending on YouTube depending on the number of likes, comments, reactions etc. 
Used Random Forest Regression model to predict the number of views based on number of likes, comments and dislikes.
We have preprocessed the data in the YouTube trending videos dataset and handled missing values. Binning method is used on views column of the dataset, videos having views less than 400k can be discarded as a video is said to be trending if it has more number of views. We also find the relation between the variables in the dataset. After performing Exploratory Data Analysis we determine the features such as : 'likes', 'dislikes' and 'comment_count' can be used to determine if a video on YouTube is trending or not.
Found the number of days between trending and published date, from that we deteremined the category of videos that have very less difference between these dates indicating they become popular quickly.
Found that the number of videos published on weekends is usually less in comparison with the remaining days of the week.
The number of videos trending on a particular day of the week seems to remain constant throughout the week by this we mean that  the videos are not trending on any  one particular day of the week, the day of the week has no influence on the trending factor.
The videos with very short span of time difference between trending and published date are the ones which trend at the fastest rate, so we subseted this videos and determined the category where the videos usually have the tendency to trend quickly. The analysis revealed that entertainment category videos usually trend at the fastest rate. 

#### Future Scope:
The future scope is that we can use event based filtering on the dataset and parse the tags associated with each video to find which kinds of videos trend more during a particular event.
There is also a scope to group videos into clusters of same catgeory like for example politics, music, sports etc.Now the main idea is that the videos belonging to the same cluster will have common tags.Tags like comedy, humor, funny, laugh etc can be grouped into one cluster and the category of this cluster can be comedy.
Evaluating how a positive or negative event effect popularity of particular category of videos using the tags and the event date.
