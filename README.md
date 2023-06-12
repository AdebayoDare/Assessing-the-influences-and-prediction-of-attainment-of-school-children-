# Assessing-the-influences-on-attainment-of-school-children
Analysis and prediction of attainment of school children in the United Kingdom



## Table of Contents

- [Project Description](#project-description)
- [Data](#data)
- [Data Cleaning](#data-cleaning)
- [Some Visualizations](#some-visualizations)
- [Models](#models)
- [Recommendation](#recommendation)
- [Limitation](#limitation)
- [References](#references)

## Project Description

This project assessed the influence on Key Stage 2 (KS2) academic achievements of 125 schools in
East Riding of Yorkshire Council (ERYC) using publicly available datasets from UK government
and ERYC websites. 

This project considered an inclusive and wide range of probable
factors. The variables considered include; school type, previous academic performances,
students financial and socio-economic status, financial capacity of school, teachers’ motivation
and general attention given to teaching resources. The project employed Python data and
statistical analysis through Pearson correlation and one-way Analysis of Variance (ANOVA). The
following variables; socio-economic factors such as Healthy Life Expectancy (HLE), Indices of
Multiple Deprivation (IMD), religious affiliation, school type, eligibility of free school meal and
variables related to attention to different workers influenced KS2 progress scores or attainment
with p-values less than the significant level (α =0.05). School type variable is seen to have the
highest influence on school KS2 attainment with absolute natural logarithm of the p-value
being 256.96. This is followed by HLE and IMD with 256.98 and 214.74 measures respectively.

Five machine learning models with a stacked model were trained on the dataset with K-Nearest
Model having the highest accuracy of 87.56%. These models were tested on a separate year
2015 dataset. The Random Forest model gives the most accurate prediction of 75% of this
separate dataset. 




## Data

The data used in this project was downloaded from the government website. A brief discription of the downloaded files are given below:

Vehicle Data: This gives the information of each vehicle involved in road accident with a unique vehicle reference number.

Accident Data: This gives the information of each accidents with a unique accident reference.

Causality Data: This contains the details of causalities involved in the accidents.

## Data Cleaning

Minimal cleaning was done on the data. This is expected, since the data was extracted from the government website. However, some nan values were present in the data specifically at the locations column. The nan values were replaced with the mean values for the location as indicated by the police force area.

## Some Visualizations

Frequency of accidents with hours of the day

![image](https://github.com/AdebayoDare/Prediction-of-United-Kingdom-Road-Traffic-Accident/assets/93272487/63f9c1e0-6cea-49bc-b2bf-218866008fc3)

Frequency of accidents with days of the week

![image](https://github.com/AdebayoDare/Prediction-of-United-Kingdom-Road-Traffic-Accident/assets/93272487/9743bf7c-b67c-4d86-a5cf-01f97f737efa)


Frequency of accidents with vehicle types

![image](https://github.com/AdebayoDare/Prediction-of-United-Kingdom-Road-Traffic-Accident/assets/93272487/d6b79b24-b7d6-48cc-b13e-9b9e2c52f3e8)






## Models

Several models were built to predict the severity of accidents. Decision tree and logistic regression classifiers were trained, achieving high-performance judged by different performance metrics. To further improve these metrics, an ensemble or stacked model was necessary. After training gradient boost and random forest ensembles, approximate accuracies of 94% and 97% were achieved, respectively. The random forest ensemble exhibited the best model performance across all metrics, with 97% accuracy, while logistic regression had the lowest accuracy at 93%.

The following steps were taking before training models on the data: 

FEATURE SELECTION: Select K-Best and chi-square libraries were used to select the best attributes in the dataset to increase model performance, while other attributes were dropped.

DATA SCALING: Due to the relatively high figures in some of the dataset, the minmaxscaler library was used to scale the data in the dataframe.

IMBALANCE: The imbalance issue in the dataset was addressed through the Synthetic Minority Over-Sampling Technique (SMOTE).


## Recommendation
1.	The analysis shows that Kent has a relatively more accident. Hence, there is a need for the police in the area to be more proactive in ensuring road accidents are reduced.
2.	There is a need to involve the police to control road traffics accidents on Fridays as most of the accidents occur on Fridays.
3.	The police and other traffic marshals should be deployed to control traffic between 8:00am and 9:00am in the morning and 5:00pm and 6:00pm in the evening everyday as most accidents occur at this period.
4.	Government should enact policies to support women while taking their children to school as the analysis shows that women have more accidents than men during this period compared with other times.
5.	Government should put measures in place to help a safe driving to and from work as most of the accidents are work related. 
6.	Most of the accidents that occur at night occur in places with over 60mph speed limit where there is no street light. Therefore, government needs to provide street lights at these places.


## Limitation

The project does not consider accidents that are not reported to the police. However, a well-policed country like the United Kingdom should have very few occurrences of such unreported accidents.

## References

DfT (2013) Road accidents and safety statistics. Available online: https://www.gov.uk/government/collections/road-accidents-and-safety-statistics [Accessed 15/05/2022].

DfT (2019) Data on all licensed and registered cars, produced by Department for Transport. Available online: https://www.gov.uk/government/statistical-data-sets/veh02-licensed-cars [Accessed 13/05/2022].

DfT (2020) Light Rail and Tram Statistics,
England: 2019/20.  Available online: https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/951076/light-rail-and-tram-statistics-england-march-2020.pdf [Accessed 13/05/2022].

DVLA (2020) Vehicle licensing statistics: 2019. Available online: https://www.gov.uk/government/statistics/vehicle-licensing-statistics-2019#:~:text=At%20the%20end%20of%202019%2C%20there%20were%3A,licensed%20vehicles%20in%20Great%20Britain [Accessed 13/05/2022].

Latlong (2022) London, the UK. Available online: https://www.latlong.net/place/london-the-uk-14153.html [Accessed 13/05/2022].

RAC (2011) Mortality statistics and road traffic accidents in the UK. 13/05/2022].

TaD (2019) Clock Changes in London, England, United Kingdom 2019. Available online: https://www.timeanddate.com/time/change/uk/london?year=2019 [Accessed 13/05/2022].

UKPD (2021) English Counties by Population and Area 2021/2022. Available online: https://populationdata.org.uk/english-counties-by-population-and-area/ [Accessed 23/05/2022].


