# Employee_attrition_case
Understanding the reason of employee turnover rate in a company using visualization and machine learning techniques in Python language
## About Dataset
Import from https://www.kaggle.com/HRAnalyticRepository/employee-attrition-data
\\Data is a mix of string and integer values.
\\Some features with strings should be dates. These should be converted to date and time if used. The features are recorddate_key, birthdate_key, orighiredate_key, and terminationdate_key.
EmployeeID is for identification. It shouldn't be used for training the machine learning model, but can be useful for filtering rows.
The age can be found by usng the record date and the birth date. So one set may be dropped.
The length of service can be found using the record date and the original hire date. So one set may be dropped.
The termination date uses 1/1/1900 if the employee is still active.
The store_name is given as a number, even though it is a nominal categorical feature. The store name itself is unlikely to be cause of employment termination, but particular feature values may be associated with particular stores. It could be an interesting separate investigation.
Gender is given in short and full. Only one of them is necessary so one will be dropped.
An employee whose employment is terminated has valid entries for termination date, termination reason and termination type. These 3 features should not be used for training the machine learning model because the features are results, not predictors, of employment termination. They may be interesting as labels, however, if the prediction goal changes.
The status_year column repeats information in the record date.
The status column is the label to predict. It should be converted from string to numerical.
There are only 2 business unit values, so the feature can be converted to numerical Boolean.
The city, department name and job title features have multiple unique values. There may be a way to categorise these features.
## Observation of 1st Visualization
People may leave the company after working for any length of time from 0 to 25 years and any age from 20 to 60. Take a closer look at the distribution of ages and service times for terminations.
## Observation of 2nd Visualization
There appear to be 3 peaks in the age when people stop working. There are 4 major peaks in the length of service before people stop working.
The largest age peak of above 60 years old overlaps the service peak of 25 years. This would be people who are retiring from the work force.
The second largest age peak of 20-25 years old overlaps the service peak of 0 years. This is likely people who are trying jobs to find something they would like.
The third age peak of 29-34 overlaps the service peak of 8 years. This is likely people who have become tired of their work and want a career change. It may also be people who have family commitments that force them to change.
The largest service peak of around 13 years overlaps with the age peak of above 60 years and with ages between 40-50. The group over 60 years old would be middle are people who changed careers to join the company.
## Observation of 4th Visualization
Nobody has stopped employment when they were at executive level.
Executives and board members only work in cities.
There does not appear to be a major difference in employment termination between males and females.
Managers and board members stop employment after at least 14 years of service. This means that they were likely internally promoted to those positions.
## Observation of 5th Visualization
Layoffs occur for all ages and all service lengths in remote and rural areas.
Resignations are uncommon in remote areas.
As expected, layoffs are involuntary, whereas resignations and retirements are voluntary.
## Observation of 6th Visualization
2014 had an unusually high number of employment terminations.
There was a peak in employment terminations in 2007-2008, when the GFC occurred.
There is another peak in 2012, but it is lower than the GFC peak.
Employment terminations in 2015 is similar to the GFC peak, but much lower than the 2014 peak. The dataset reaches 31 December 2015, so the 2015 record is complete.
## Preprocessing for machine learning models
## Split data for testing and training
## Logistic Regression
Accuracy achieved- 0.9704
## Random Forest Classifier
Accuracy achieved- 0.9863
## Support Vector Classification 
Accuracy achieved- 0.9872
## K-Nearest Neighbour
Accuracy achieved- 0.9869
## XGB Regressor
Accuracy achieved- 0.9869
