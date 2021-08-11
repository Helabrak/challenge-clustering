# Challenge classification - Bearings

## Mission objectives

Your boss was happy with your previous work on the bearing analysis, guessing faulty bearings was a piece of cake for you! The team came back to you for further expertise; They want to know what type of failures occur! Or rather, if the failures exhibit similarities to other failures. This is a perfect clustering challenge.

The steps to do so the following was implemented:
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
* plotly.express
* sklearn.preprocessing 
* sklearn.cluster import KMeans

# Usage
| Filename                             | Usage                                                     |
|--------------------------------------|-----------------------------------------------------------|
| notebook_final.ipynb | Jupyer Notebook file containing Python code.<br>Used to clean the data.<br>Used to draw plots and do preliminary analysis. <br>Used to create our prediction model.|
| Visuals | Folder containing visuals.|

# Data exploration
![](/Visuals/visual_mean_status_distribution.png)<br>
The distribution of defective and good bearings is unbalanced: Out of 112 bearing, 100 are defective and 12 are good ones.
![](/Visuals/visual_mean_a1_x.png)<br>
By using the mean of every acceleration for each bearing, we can already identify a pattern using a1_x. Good bearings (1) have generally a higher a1_x than defectives ones (0).
![](/Visuals/visual_mean_a1_z.png)
By using the mean of every acceleration for each bearing, we can already identify a pattern using a1_z. Good bearings (1) have generally a higher a1_z than defectives ones (0).
![](/Visuals/visual_vibration_a1_x_105.png)<br>
Vibration of a1_x over time of bearing_id 105
![](/Visuals/visual_hz_16.png)
Hz over time of bearing_id 16

# Feature engineering
To help the model make predictions, we created new features. In total, we have 54 features:
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
