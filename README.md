# PHBS_MLF_2018

[Arianna MISERICORDIA](https://github.com/ariannamisericordia) 1802010234

[Ewa GERUS](https://github.com/ewagerus)  1802010260

[Noam PELEG](https://github.com/Noam-Peleg) 1802010275

[Lillah BENARD](https://github.com/Lillahbenard) 1802010264

# _Prediction of automotive accident severity_ 

**MOTIVATION**:

The motivation behind our research is the understanding of specific conditions that affect the severity of an automotive accident. The purpose of this project is to highlight impactful variables while operating a vehicle in order to improve accident prevention.

**GOAL**: 

We executed a classification based on U.K. road accidents ranging from 2014 to 2016 using the methodologies covered in class (Ordered Logistic Regression or Multinomial Logistic Regression, KNN, Decision tree). Our classification specify the impact of certain features on car wreckage. 

**DATA SOURCE**: 

The data we collected comes from the U.K. government who amassed traffic data based on police reports. 
The data that we will be analyzing has been composed of the U.K. road accidents from 2014 to 2016. 

Accidents are recorded according to these features:
*  Reference Number,
*  Grid Ref:Easting,
*  Grid Ref: Northing,
*  Expr1,
*  Severity, 
*  Day of the week, 
*  Time (24hr), 
*  1st Road Class,
*  Road surface,
*  Accident date,
*  Weather condition, 
*  Lighting conditions,
*  Number of vehicles involved, 
*  Casualty class,
*  Sex of casualty,
*  Age of casualty,
*  Type of vehicle.

**DATASET SOURCE**:

https://data.gov.uk/dataset/6efe5505-941f-45bf-b576-4c1e09b579a1/road-traffic-accidents

**METHODOLOGY**: 

**_I. Data preprocessing_**:

*  Merging data sets

*  Dropping columns containing  references and correlated variables.

*  Dealing with missing data - deleting observations that are labeled with NaNs

*  Listing variables:
   *  Time (24hr): Day-time, Night-time
   *  Weather conditions: Fine, Snowing, Raining, Fog, Other
   *  Type of Vehicle: Car, Bus, Goods vehicles, Motorcycle, Other
   *  Day: Weekday, Weekend
   *  Casualty class: Passenger, Pedestrian, Driver

*  Creating dummies and dropping variables containing the same information ( Sex of casualty_Female, Day_Weekday , Time (24hr)_ Day-time)
    
* Re-sampling our unbalanced data
  *  Slight: 6739, Serious: 957, Fatal: 48
  *  Slight: 957, Serious: 957, Fatal: 48
  *  Slight: 957, Fatal: 957, Serious: 957
  
**_II. Prediction_**:

Accuracy of each of the following methods were checked to choose the best classifier for reaching our goal. To implement methods mentioned below scikit-learn were used.

*  **Decision tree**

![kfold decision tree](https://user-images.githubusercontent.com/43052624/48170888-87be4b80-e334-11e8-8302-7c8437f7903f.png)

Kfold best mean accuracy of 73.95% for a decision tree depth equal to 6.

![decision tree](https://user-images.githubusercontent.com/43052624/48113500-116b0c00-e296-11e8-8a0f-52ce61ae41cc.png)

The 3 most important features in decision tree model are: Casualty Class_Pedestrian, Road Surface_Dry, Road Surface_Wet or Damp.

*  **Neural network**

The mean accuracy is equal to 72.41% (standard deviation 2.46%.

*  **KNN** 

![kfold knn](https://user-images.githubusercontent.com/43052624/48171438-dcfb5c80-e336-11e8-82e7-7f259129e643.png)

Kfold best mean accuracy of 71.37% (standard deviation 2.77%) for n_neighbors=5.

*  **Ordered Logistic Regression**

_With PCA_

The mean accuracy is equal to 53.12% (standard deviation 2.32%)

_Without PCA_

The mean accuracy is equal to 53.54% (standard deviation 2.67%)

![logistic regression](https://user-images.githubusercontent.com/43052624/48114206-1ed5c580-e299-11e8-80b8-1e1cc922a2a0.png)

**CONCLUSION**: 

![summary](https://user-images.githubusercontent.com/43052624/48114312-8724a700-e299-11e8-86e6-2bc53ce08bbf.png)

The best model is the decision tree with a mean accuracy of 73.95%. 

We can conclude that the 3 most important features that affect the severity of an automotive accident are: Casualty Class_Pedestrian, Road Surface_Dry, Road Surface_Wet or Damp.
