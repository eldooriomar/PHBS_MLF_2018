# PHBS_MLF_2018

[Arianna MISERICORDIA] (https://github.com/ariannamisericordia) 1802010234

[Ewa GERUS] (https://github.com/ewagerus)  1802010260

[Noam PELEG] (https://github.com/Noam-Peleg) 1802010275

[Lillah BENARD] (https://github.com/Lillahbenard) 1802010264

# _Prediction of automotive accident severity_ 

**Motivation**:

The motivation behind our research is the understanding of specific conditions that affect the severity of an automotive accident. The purpose of this project is to highlight impactful variables while operating a vehicle in order to improve accident prevention.

**Goal**: 

We will execute a classification based on U.K. road accidents ranging from 2014 to 2016 using the methodologies covered in class (Ordered Logistic Regression or Multinomial Logistic Regression, KNN, Decision tree). Our classification will specify the impact of certain features on car wreckage. 

**Data Source**: 

The data we collected comes from the U.K. government who amassed traffic data based on police reports. 
The data that we will be analyzing has been composed of the U.K. road accidents from 2014 to 2016. 

Accidents are recorded according to these features:
*  Severity (1 = fatal, 2 = serious, 3 = slight), 
*  Day of the week (weekend, working days), 
*  Time (day , night), 
*  Accident date,
*  Weather condition (fine, fog, raining, snowing), 
*  Lighting conditions,
*  Number of vehicles involved, 
*  Speed limit,
*  Road type,
*  Casualty class,
*  Sex of casualty,
*  Age of casualty,
*  Type of vehicle.

**Dataset Source**:

https://data.gov.uk/dataset/6efe5505-941f-45bf-b576-4c1e09b579a1/road-traffic-accidents

**Methodology**: 

_Data preprocessing_:

*  Dropping columns containing variables not mentioned above 

*  Dealing with missing data - deleting observations that are labeled with NaNs

*  Feature selection- separately for each algorithm 
     
*  Further data processing may be done if the algorithm requires it

*  Division into training, test and validation datasets

_Prediction_:

Accuracy of each of the following methods will be checked to choose the best classifier for reaching our goal. To implement methods mentioned below scikit-learn will be used.

*  Ordered Logistic Regression (in case of meeting an assumption of proportional odds) or Multinominal Logistic Regression 
     *  An analysis of the impact of statistically important independent variables will be conducted 

*  Decision tree/ Random forest

*  KNN 

