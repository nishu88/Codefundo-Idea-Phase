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

● The disasters like **tsunami, landslide, floods** caused due to breakage of dams/reservoirs are because of the internally caused earthquakes or more precisely due to the tectonic movement of plates in that region.

● Analyzing and Focusing on periodic tectonic shifts across the area of interest.

![image](https://user-images.githubusercontent.com/29069343/46875708-0f11bf80-ce5a-11e8-8cd5-84f4f297f7db.png)
                                        ***Plate Tectonics Worldmap***
                                        

Combining both the types of data set, we really have large number of training examples to get the best fit. 
From the various source, the prediction of an earthquake must define 3 elements:**1) Date and Time 2) Location 3) Magnitude.** The below paragraph gives the approach to prediction.

 Using the dataset obtained from above, consider a region and taking all the data related to earthquake from the previous days like **Magnitude, Depth, Azimuthal Gap, Magnitude error, Horizontal distance**, caused by and many more features of the region. The above features is fed to Machine Learning Model and obtain accuracy of the model. And then use **Principal Component Analysis (PCA)** to reduce number of features from available, so that precision of predicting the earthquake of that region is more. When the reduced number of features is obtained, these features are fit to the new Machine Learning Model and obtain the accuracy. Then compare the accuracy of both models, choose the one best fits.
 
 The best fit model is trained for all other regions and then predict the magnitude, date and time of the earthquake. Setting a threshold that the prediction is true, a warning message will be sent to people of that region using online text message sending portal.
 
 
https://data.gov.in/keywords/earthquake  - One of the source for the data.

https://www.kaggle.com/nksingh673/earthquake-indian-subcontinent Dataset 

https://www.kaggle.com/usgs/earthquake -database Dataset

## Machine Learning Approach:-
Thinking of the ML model, it consists of **multilayers of Convolution Layer and MaxPooling layer** with their respective hyperparameters such as Activation function, input nodes. 
When it comes to the part of training, usage of **GridSearch model** come into play. 
For GridSearch model, pass the first parameter as the model, second parameter as ParameterGrid with functions like batch_size, epochs, optimizer, momentum, decay, weight_constraints, etc. with their different set of values like 10, 20, 50, 100 as batch_size or SGD, Adadelta, Adamax as optimizers. 
Then Grid Search model is fit with input train and input test values and obtain the set of values of hyperparameters used which has got highest accuracy. Using the obtained set of values of hyperparameters.

**Webscraping** popular earthquake predicting websites like :-

https://www.ditrianum.org/

https://world-earthquakes.com/

No prediction is accurate. We constantly need more data to improve our prediction.

## Proof of Concept:-

The idea of characteristic earthquakes was the basis of the Parkfield prediction: fairly similar earthquakes in 1857, 1881, 1901, 1922, 1934, and 1966 suggested a pattern of breaks every 21.9 years, with a standard deviation of ±3.1 years. Extrapolation from the 1966 event led to a prediction of an earthquake around 1988, or before 1993 at the latest (at the 95% confidence interval). The appeal of such a method is that the prediction is derived entirely from the trend, which supposedly accounts for the unknown and possibly unknowable earthquake physics and fault parameters. However, in the Parkfield case the predicted earthquake did not occur until 2004, a decade late. This seriously undercuts the claim that earthquakes at Parkfield are quasi-periodic, and suggests the individual events differ sufficiently in other respects to question whether they have distinct characteristics in common. 

**(If predicted accurately quarter million lives could’ve been saved back in 2004. )**


## Expected Result :-

Earthquake prediction is an immature science—it has not yet led to a successful prediction of an earthquake from first physical principles. Research into methods of prediction therefore focus on empirical analysis, with two general approaches: either identifying distinctive precursors to earthquakes, or identifying some kind of geophysical trend or pattern in seismicity that might precede a large earthquake.
We would predict earthquakes in 2 stages:-

•	**Trend analysis** of earth quakes using datasets available on reliable sites. Gain enough data on earthquakes for 2 – 5 decades in past. And apply **Machine learning algorithms** on the dataset. (**prediction years before the actual earthquake happens.**)

•	With the help of scientifically proven precursors like **Animal behavior**(low frequency P-waves), **Dilatancy–diffusion**(Detection of variations in the relative velocities of the primary and secondary seismic waves), **Changes in Vp/Vs** -(**prediction minutes before the earthquake.**)

**Predictions even 10 min before earthquakes can save thousands of lives. They’d get enough time to vacate buildings and reach safe distance.**


## Post Disaster :-

•	Awareness of Rescue camps setup around the affected areas will be available on an **Disaster-relief application**.

•	This app downloads the map of User's surroundings within a radius of 10 km from google maps for the **offline use** and prepares for the worst whenever connected to the internet. (doesn’t require a reliable internet connection 24/7)

•	**SOS distress 24/7 helpline** with **load balancer** for peak hours which redirects calls to different numbers who are all willing to help.

•	**Twitter Sentiment Analysis** to map out the more affected areas and make sure which areas require more help.

•	**Setup basic communication** required across help channels by indicating knocked out Cell towers on an area map. (Because communication is key in responding to requests and saving lives.)
