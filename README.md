# GITHUB_Lillahbenard-PHBS_MLF_2018

Arianna MISERICORDIA: ariannamisericordia 1802010234

Ewa GERUS: ewagerus  1802010260

Noam PELEG : Noam-Peleg 1802010275

Lillah BENARD : Lillahbenard 1802010264

# _Prediction of automotive accident severity_ 

**Motivation**:

The motivation behind our research is the understanding of specific conditions that affect the severity of an automotive accident. The purpose of this project is to highlight impactful variables while operating a vehicle in order to improve accident prevention.

**Goal**: 

We will execute a classification based on U.K. road accidents ranging from 2012 to 2014 using the methodologies covered in class (Ordered Logistic Regression or Multinomial Logistic Regression, KNN, Decision tree). Our classification will specify the impact of certain features on car wreckage. 

**Data Source**: 

The data we collected comes from the U.K. government who amassed traffic data based on police reports. 
The data that we will be analyzing has been composed of the U.K. road accidents from 2014 to 2016. It describes the severity (1 = fatal, 2 = serious, 3 = slight) of the accident according to the day of the week (weekend, working days), time (morning, afternoon, night), weather condition (fine, fog, raining, snowing), number of vehicles involved, number of casualties, speed limit and road type.

**Dataset Source**:

http://data.dft.gov.uk/gb-traffic-matrix/all-traffic-data-metadata.pdf 

http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/ 

https://data.gov.uk/dataset/6efe5505-941f-45bf-b576-4c1e09b579a1/road-traffic-accidents

**Methodology**: 

_Data preprocessing_:

*  Dropping columns containing variables not mentioned above 

*  Dealing with missing data - deleting observations that are labeled with NaNs

*  Converting some independent variables:

     *  Day of the week - creating a binary variable by assigning a value of “0” for Weekdays (Monday- Thursday) and “1” for Weekends (Friday- Sunday) 
     *  Time - creating a binary variable that has a value “0” for Day (6:01-18:00), “1” for Night (18:01-6:00)
     *  Weather conditions- combining existing labels into 4: fine, raining, snowing, fog 
     
*  Further data processing may be done if the algorithm requires it

*  Division into training, test and validation datasets

_Prediction_:

Accuracy of each of the following methods will be checked to choose the best classifier for reaching our goal. To implement methods mentioned below scikit-learn will be used.

*  Ordered Logistic Regression (in case of meeting an assumption of proportional odds) or Multinominal Logistic Regression 
     *  An analysis of the impact of statistically important independent variables will be conducted 

*  Decision tree/ Random forest

*  KNN 

