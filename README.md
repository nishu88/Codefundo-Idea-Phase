# Codefundo-Idea-Phase
Earthquake prediction using Machine Learning and Trend Analysis

## Problem Statement :-
Predicting the earthquake and the scale/impact of it in the regions prone to it. 

## Addressing the problem:- 
It is well known that if a disaster has happened in a region, it is likely to happen there again. Some regions really have frequent earthquakes, but this is just a comparative quantity compared to other regions. 

To obtain the best fit so that we can predict accurately we need large number of training examples. 

## Approach:- 
Data set type 1: **Direct Inference**

● Information of the past earthquakes of that region.  (Detecting certain pattern/trends from previous earthquakes.)

Data set type 2: **Indirect Inference**

● The disasters like tsunami, landslide, floods caused due to breakage of dams/reservoirs are because of the internally caused earthquakes or more precisely due to the tectonic movement of plates in that region.

● Analyzing and Focusing on periodic tectonic shifts across the area of interest.

![image](https://user-images.githubusercontent.com/29069343/46875708-0f11bf80-ce5a-11e8-8cd5-84f4f297f7db.png)
                                        ***Plate Tectonics Worldmap***
                                        

Combining both the types of data set, we really have large number of training examples to get the best fit. 
From the various source, the prediction of an earthquake must define 3 elements: 1) Date and Time 2) Location 3) Magnitude. The below paragraph gives the approach to prediction.

 Using the dataset obtained from above, consider a region and taking all the data related to earthquake from the previous days like Magnitude, Depth, Azimuthal Gap, Magnitude error, Horizontal distance, caused by and many more features of the region. The above features is fed to Machine Learning Model and obtain accuracy of the model. And then use Principal Component Analysis (PCA) to reduce number of features from available, so that precision of predicting the earthquake of that region is more. When the reduced number of features is obtained, these features are fit to the new Machine Learning Model and obtain the accuracy. Then compare the accuracy of both models, choose the one best fits.
 
 The best fit model is trained for all other regions and then predict the magnitude, date and time of the earthquake. Setting a threshold that the prediction is true, a warning message will be sent to people of that region using online text message sending portal.
 
https://data.gov.in/keywords/earthquake  - One of the source for the data.
https://www.kaggle.com/nksingh673/earthquake-indian-subcontinent
Dataset https://www.kaggle.com/usgs/earthquake -database Dataset
