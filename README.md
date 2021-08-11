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

2. kmeans clustering:
3. 
# Selected Features: 
- a1_x_mean
- a1_y_mean 
- a1_z_mean 
- a2_x_mean 
- a2_y_mean
- a2_z_mean
- rpm_mean
- hz_mean
- w_mean
- a1_x_range
- a1_y_range
- a1_z_range
- a2_x_range
- a2_y_range
- a2_z_range
- w_range
- a1_x_min
- a1_y_min
- a1_z_min
- a2_x_min
- a2_y_min
- a2_z_min
- a1_x_max
- a1_y_max
- a1_z_max
- a2_x_max
- a2_y_max
- a2_z_max
- w_max
- a1_x_fft_mean
- a1_y_fft_mean
- a1_z_fft_mean
- a2_x_fft_mean
- a2_y_fft_mean
- a2_z_fft_mean
- a1_x_ff_range
- a1_y_fft_range
- a1_z_fft_range
- a2_x_fft_range
- a2_y_fft_range
- a2_z_fft_range
- a1_x_fft_min
- a1_y_fft_min
- a1_z_fft_min
- a2_x_fft_min
- a2_y_fft_min
- a2_z_fft_min
- a1_x_fft_max
- a1_y_fft_max
- a1_z_fft_max
- a2_x_fft_max
- a2_y_fft_max
- a2_z_fft_max
- status

# Machine learning
The target variable: status (1 = Good, 0 = Defective).<br>
We tested 3 models, all of them had high performance:
- Random Forest
- SVC 
- KNN

| Model         | Accuracy | Precision   | Recall      | 
| --------------| -------- | ----------- |-------------|
| Random Forest | 0.91     | 1.00 & 0.25 | 0.91 & 1.00 |
| SVC           | 1.00     | 1.00 & 1.00 | 1.00 & 1.00 |
| KNN           | 1.00     | 1.00 & 1.00 | 1.00 & 1.00 |

In the end, we can see that either the SVC or KNN models are the best performer with perfect scores of 1.00.
We choose KNeighbors as our model and made further analysis/visuals about its performance.

KNeighbors Classifier's confusion matrix
![](/Visuals/visual_confusion_matrix.png)<br>
KNeighbors Classifier's AOC
![](/Visuals/visual_AOC.png)

# Contributors
| Name           | GitHub                                                                              |
|----------------|-------------------------------------------------------------------------------------|
| Heba Elebrak | <a href="https://github.com/Helabrak">https://github.com/Helabrak               |



# Timeline
09/08/2021 - 11/08/2021
