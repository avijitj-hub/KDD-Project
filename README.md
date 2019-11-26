# KDD-Project

### Project: Prediction for trending videos on YouTube in USA.
The objective of the project is to predict trending videos based on the number of views, likes, dislikes, number of comments, published date and trending date. 

### Team:
1. Narendra Pahuja
2. Akshay Popli
3. Monika Chandrashekara
4. Prerana Chandrashekar
5. Avijit Jaiswal

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

#### * Domain Knowledge (document sources):
The YouTube trending video dataset link: https://www.kaggle.com/datasnaek/youtube-new#USvideos.csv

#### * Data Understanding and EDA:
The relation between variables in the YouTube trending dataset is analyzed using graphical representation. The categorical and numerical features are studied to gain better understanding of the dataset to perform machine learning algorithms on the dataset.

#### * Data Preparation:
1. We will merge data from Json and csv file considering id and category_id respectively as common reference to get the category title of video.
2. After merging we will convert the date column in proper format.
3. Clean data by removing redundant values.
4. Pre-process the missing values.
5. Visualize the data with different plots to find the correlation between variables.

#### * Handling Discrimination and bias:
There is no bias in our dataset as it does not contain any user related information.so we dont need to handle discrimination and bias

#### * Machine Learning:

We will do sentimental analysis that is, we will take an event / incident date and will find out what other videos became in trending in next 10 days after that incident took place. <br>Based on the tags, we will find data points with the densest scatters and use these densely populated points as cluster centres. We will then find out the cluster with highest scatter points. This will give us what kind of videos were the highest trending after that incident. <br>As K-means clustering is most suitable to group similar data points together and discover underlying patterns, we will follow this approach and make the clusters based on common tags in videos. <br><br> 

#### * Evaluation:
Evaluating popularity based on likes and comments.
Evaluating positive or negative comments based on category. 
Evaluating how a positive or negative event effect popularity of particular category of videos using the tags and the event date  

### Conclusion:
The YouTube trending dataset is used to predict the type of video trending on YouTube depending on the number of likes, comments, reactions etc. 
We have preprocessed the data in the YouTube trending videos dataset and handled missing values. Binning method is used on views column of the dataset, videos having views less than 400k can be discarded as a video is said to be trending if it has more number of views. We also find the relation between the variables in the dataset. After performing Exploratory Data Analysis we determine the features such as : 'likes', 'dislikes' and 'comment_count' can be used to determine if a video on YouTube is trending or not.

 #### Progress :
Found the number of days between trending and published date , from that we deteremined the videos have very less difference indicating they become popular quickly.

#### Next step:
* we are going to use event based filtering on the dataset and will be parsing the tags aaasociated with each video to find which kinds of videos trend more during a particular event.
