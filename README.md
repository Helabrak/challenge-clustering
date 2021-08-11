# Challenge classification - Bearings

## Mission objectives

Your boss was happy with your previous work on the bearing analysis, guessing faulty bearings was a piece of cake for you! The team came back to you for further expertise; They want to know what type of failures occur! Or rather, if the failures exhibit similarities to other failures. This is a perfect clustering challenge.

To do so I tried implementing the following :
    gathering of features (5+) of failed bearing dataset
    kmeans clustering of at least two features of the failed bearings
    visualization of said clustering
    evaluation of the silhouette score of your clustering method
    extension (one-by-one) to 6 features. (how does the silhouette score evolve?)
    vizualizations of your model evaluation

![](/Visuals/bearing_explanation.jpeg)

# Installation

## Python version
* Python 3.8

## Packages used

* pandas
* numpy
* matplotlib.pyplot
* seaborn
* sklearn.preprocessing 
* sklearn.cluster import KMeans

# Usage
| Filename                             | Usage                                                     |
|--------------------------------------|-----------------------------------------------------------|
| clustering.ipynb | Jupyer Notebook file containing Python code.<br>Used to clean the data.<br>Used to draw plots and do preliminary analysis. 


# Visualization
1- Clustering heatmap with hz_mean for each bearing: 
![image](https://user-images.githubusercontent.com/84380899/129030482-356470e4-bf82-45cc-b053-9e12a625e885.png)


3. example of Silhouette methods to chose the best features
![image](https://user-images.githubusercontent.com/84380899/129045602-e7b2c0cd-c3c0-462a-b860-a14d2c3cc980.png)
![image](https://user-images.githubusercontent.com/84380899/129046469-5f660b05-95b6-4c1c-b651-1aebb5e44d28.png)


5. #Visulaize (Evaluation for test scores): 
![image](https://user-images.githubusercontent.com/84380899/129048127-4cecae81-7df6-435f-b2bf-454a774568f4.png)


# Generating the sample data from make_blobs
# This particular setting has one distinct cluster and 3 clusters placed close together.
# Create a subplot with 1 row and 2 columns
# The 1st subplot is the silhouette plot
# The silhouette coefficient can range from -1, 1 but in this example all
# lie within [-0.1, 1]
    
# The (n_clusters+1)*10 is for inserting blank space between silhouette
# plots of individual clusters, to demarcate them clearly.
   

# Initialize the clusterer with n_clusters value and a random generator
# seed of 10 for reproducibility.
   

# The silhouette_score gives the average value for all the samples.
# This gives a perspective into the density and separation of the formed
# clusters
    
# Compute the silhouette scores for each sample
  
# Aggregate the silhouette scores for samples belonging to
# cluster i, and sort them
    
# Label the silhouette plots with their cluster numbers at the middle

# Compute the new y_lower for next plot


# The vertical line for average silhouette score of all the values

# 2nd Plot showing the actual clusters formed

# Labeling the clusters

# Draw white circles at cluster centers

Silhouette scores : 

Automatically created module for IPython interactive environment
For n_clusters = 2 The average silhouette_score is : 0.7049787496083262
For n_clusters = 3 The average silhouette_score is : 0.5882004012129721
For n_clusters = 4 The average silhouette_score is : 0.6505186632729437
For n_clusters = 5 The average silhouette_score is : 0.56376469026194
For n_clusters = 6 The average silhouette_score is : 0.4504666294372765

# Contributors
| Name           | GitHub                                                                              |
|----------------|-------------------------------------------------------------------------------------|
| Heba Elebrak | <a href="https://github.com/Helabrak">https://github.com/Helabrak               |
   



# Timeline
09/08/2021 - 11/08/2021
