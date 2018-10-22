# GITHUB_ID-PHBS_MLF_-2018

Arianna MISERICORDIA: ariannamisericordia

Ewa GERUS: ewagerus

Noam PELEG : Noam-Peleg

Lillah BENARD : Lillahbenard

# _Prediction of automotive accident severity_ 

**Motivation**:

The motivation behind our research is the understanding of specific conditions that affect the severity of an automotive accident. The purpose of this project is to highlight impactful variables while operating a vehicle in order to improve accident prevention.

**Goal**: 

We will execute a classification based on U.K. road accidents ranging from 2012 to 2014 using the methodologies covered in class (Ordered Logistic Regression, KNN, Decision tree). Our classification will specify the impact of certain features on car wreckage. 

**Data Source**: 

The data we collected comes from the U.K. government who amassed traffic data based on police reports. 
The data that we will be analyzing has been composed of the U.K. road accidents from 2012 to 2014 published on Kaggle. It describes the severity (1= fatal, 2= serious, 3 = slight) of the accident according to the day of the week (weekend, working days), time (morning, afternoon, night), weather condition (fine, fog, raining, snowing), number of vehicles involved, number of casualties, speed limit and road type.

**Dataset Source**:

http://data.dft.gov.uk/gb-traffic-matrix/all-traffic-data-metadata.pdf 

http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/ 

https://www.kaggle.com/daveianhickey/2000-16-traffic-flow-england-scotland-wales

**Methodology**: 

_Data preprocessing_:

1-Dropping columns containing variables not mentioned above 

2-Dealing with missing data - deleting observations that are labeled with NaNs

3-Converting some independent variables:

*  Day of the week - creating a binary variable by assigning a value of “0” for Weekdays (Monday- Thursday) and “1” for Weekends (Friday- Sunday) 
*  Time - creating a binary variable that has a value “0” for Day (6:01-18:00), “1” for Night (18:01-6:00)
*  Weather conditions- combining existing labels into just 4: fine, raining, snowing, fog 
Further data processing will be done for each algorithm separately, including dividing into training, test and validation datasets.

_Prediction_:

Accuracy of each of the following methods will be checked to choose the best classifier for reaching our goal. To implement methods mentioned below scikit-learn will be used.

1) Ordered logistic regression (in case of meeting an assumption of proportional odds) or multinominal logistic regression 
additionally an analysis of an impact of statistically important independent variables will be conducted 

2) Decision tree/ Random forest

3) KNN 

