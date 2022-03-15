# **NETFLIX MOVIES AND TV SHOWS CLUSTERING**

## Problem Statement-
Main purpose of this project is to do EDA, Netflix’s recent year focus, understanding 
what type of content available on Netflix and clustering similar content by using text based features.

## Summary- 
Got a dataset having 7787 records and 12 features, which is not labelled. Then I started by 
understanding the data followed by missing/null value treatment, then some feature engineering for data 
visualization and then data visualization performed. After getting insights from data I did some feature 
engineering like text cleaning, TF-IDF, PCA on data. Then after selecting no. of clusters, I built the 
KMeans clustering model. After that I assigned the clusters in our dataset and created word cloud for each 
cluster and after that calculated silhouette score for evaluation purpose

# Components & Approach
## 1. Exploratory Data Analysis
### a. Understanding the data- 
In this step after loading the data I performed head, tail, columns, 
info, dtypes, describe functions to get basic information about our dataset.
### b. Checking for missing & duplicated values- 
Then I checked for missing values in our dataset 
using is null function. Some of our features had missing values that I filled with ‘unknown’ 
## 2. Cleaning Dataset & Feature Engineering
As some of our features has got null values, I filled all null values with ‘unknown’ using fillna 
method. Then I extracted date, month and year from date added column. Renamed the listed in 
column to genres.
## 3. Data Visualization – 
In data visualization I got some insights like, in type of content, around 69% 
content as movies and remaining 31% as TV shows are present on Netflix. Then in genres 
International movies, dramas and comedies are most occurred types. In content addition day wise 
we can clearly spot the insights that Netflix majorly add the content on the 1st day of every month.
In rating column most of the given rating is for mature adults (TV-MA) for both TV shows and 
Movies. In countries column US, India and UK are the top 3 most occurred countries.
Then another graph shows that from 2017 number of Movies added increased tremendously, but at 
the same time TV shows added from 2017 are also increased but as comparison to Movies
they are very less in numbers
## 4. Feature Engineering- 
After data visualization I did feature engineering in which I added a new 
column which contains all the text and categorical column data, so that we can work on entire text 
data. Then used snowball stemming to stem the text into the column. After stemming and other 
cleaning operations I applied TF-IDF vectorizer on the text. Applied Principal Component 
Analysis (PCA) to reduce the dimensions of X.
## 5. Model Building
### KMeans Clustering-
K-Means Clustering is an Unsupervised Learning algorithm, which groups the unlabeled 
dataset into different clusters The K-Elbow Visualizer implements the “elbow” method of 
selecting the optimal number of clusters for K-means clustering. Then no. of cluster k=15 
selected. After that fitted the model on data and then predicted the labels. Then assigned the 
clusters in datasets and then visualized each cluster using word cloud.
## 6. Evaluating Models 
### Silhouette Score - 
Silhouette analysis can be used to study the separation distance between the 
resulting clusters. The silhouette plot displays a measure of how close each point in one cluster is 
to points in the neighboring clusters and thus provides a way to assess parameters like number of 
clusters visually. This measure has a range of [-1, 1].
We selected number of clusters as 15 which in above calculations showing 0.00708 as silhouette 
score
## 7. Conclusion
a. In cumulative explained variance graph we got 80% of variance captured by 3000 components 
only, that’s why we selected no. of components as 3000. 
b. We selected no. of clusters as 15 from Elbow Method. 
c. Calculated silhouette score for 15 no. of clusters which was showing 0.008 
d. Then we applied KMeans on our data and then we predict the labels. 
e. We plotted word cloud for each cluster so that we can visualize the summary of each cluster. 
f. Then we plotted average silhouette score for clusters ranging from 2 to 16, and in that we get 
silhouette score 0.00708 for cluster=15 which is pretty close to earlier we calculated
## 8. Limitations
1. As the number of dimensions increases, a distance-based similarity measure converges to a constant value between any features.
2. Centroids can be dragged by outliers, or outliers might get their own cluster instead of being ignored.
3. More Computational power required.
4. k-means has trouble clustering data where clusters are of varying sizes and density.
## 9. Future Scope
1. With more computational power can work on more data.
2. Can apply different clustering algorithms.

# Thank You !
(Note- In case above notebook take too long to open please use this link -
https://nbviewer.org/github/sammed97/NETFLIX-MOVIES-AND-TV-SHOWS-CLUSTERING/blob/main/Copy_of_NETFLIX_MOVIES_AND_TV_SHOWS_CLUSTERING.ipynb )
