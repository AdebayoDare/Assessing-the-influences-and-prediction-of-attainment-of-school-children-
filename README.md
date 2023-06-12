# Assessing-the-influences-on-attainment-of-school-children
Analysis and prediction of attainment of school children in the United Kingdom



## Table of Contents

- [Project Description](#project-description)
- [Data](#data)
- [Data Cleaning](#data-cleaning)
- [Data preprocessing](#data-preprocessing)
- [Visualizing the influences on attainment](#Visualizing-the-influences-on-attainment)
- [Models](#models)
- [Conclusion](#conclusion)
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
The data for this project was publicly sourced from the UK government and the East Riding of
Yorkshire Council (ERYC) websites (DfE, 2021b; ERYC, 2021). The data contains SATs test
attainment figures of Year 6 (KS2) students in ERYC. The pupils are assessed in three subjects;
English Reading , Mathematics and English Writing (EL, 2021). This project used the datasets of
2016-2017,2017-2018 and 2018-2019 academic sessions to monitor the progress or decline of
academic attainments influenced by other variables in the dataset.
In 2016, the DfE introduced progress measure to rate schools (DfE, 2016). The school progress
score is an average of all the pupils’ progress scores. The school progress score indicates how
well the pupils improve from their Year 2 (KS1) scores in mathematics, reading and writing
when compared with other pupils who have the same KS1 results across England (DfE, 2019). A
progress score of 0 indicates that a pupil has made an average amount of improvement by the
end of KS2 similar to someone achieving the level that they achieved at the end of KS1. A
positive score indicates their improvement is above average while a negative score implies it is
below average.
This project uses the progress scores of the subjects and average academic progress of each
school in ERYC as the target variable, while other variables are used
as independent variables. These variables are categorised into school description variables,
variables relating to KS1 performance, students financial and socio-economic status, finance of
the school, teachers’ motivation, attention to other sections of schools apart from classrooms
and attention given to teaching resources. Most of the independent variables were obtained
from the UK government website (DfE, 2021b) and some missing information about HLE and
IMD were obtained from ERYC council website (ERYC, 2021) by mapping the schools’
postcodes with the HLE and IMD scores of the area

## Data Cleaning

Data cleaning was done on missing and suppressed values. Two datasets were extracted from
the gov.uk site. These are the school general attainment (this also includes the data from ERYC
indicating IMD and HLE) and funding datasets. These were merged on the unique reference
number (URN) of the schools.
Two columns related to percentage of disadvantaged students were removed because of the
large number of suppressed values. However, the cleaned dataset retained a more concise
column regarding disadvantaged students and level of deprivation. In addition, schools with
suppressed academic attainment/progress scores were removed, while other missing variables
were replaced by the median values of the distribution.

## Data Preprocessing
For the purpose of analysis and machine learning, categorical variables such as school religious
affiliation, school type, IMD and HLE were encoded

## Visualizing the influences on attainment
Graph showing the relative influences on attainment measured by absolute natural logarithm of the p-value 

![image](https://github.com/AdebayoDare/Assessing-the-influences-and-prediction-of-attainment-of-school-children-/assets/93272487/daa276c4-be12-4f9e-a6ee-8ae96ac1729f)








## Models

Five machine learning algorithms were trained on the dataset to detect the most efficient
model. The algorithms are: Logistic Regression (LR), Support Vector Machine (SVM), Random
Forest (RF), Gradient Boost (GB) and K-nearest neighbours (KNN). These models were also
stacked to train the dataset to check if the model performance will increase. The figure below
gives the relative performance of the models with KNN performing best with approximately
88%. To validate this high accuracy, other performance metrics such has precision, recall and
f1-score were calculated, each with 85%.

![image](https://github.com/AdebayoDare/Assessing-the-influences-and-prediction-of-attainment-of-school-children-/assets/93272487/888ad96d-2c36-4824-ae25-ee545be2c601)




## Conclusion
The findings in this study suggests that KS2 attainment is mostly dependent on school type.
Moreover, socio-economic factors such as IMD, HLE and FSM largely influence attainment. It is
important for government to address these factors; the well-being of the communities where
these schools are located can effectively improve with government intervention. Also,
variables related to funding and attention given to workers in the primary schools are seen to
influence attainment. Hence, if KS2 attainment is to be improved, government through DfE
should ensure these are addressed.
While DfE releases annual performance of KS2 attainment and progress, a more impactful
action is to investigate wide range of factors influencing these attainments at the schools and
deploy models which will be utilized to caution and guide schools predicted to have low
attainment or progress scores.


## References

DfE (2013) National curriculum. Available online:
https://www.gov.uk/government/collections/national-curriculum [Accessed 13/07/2022].

DfE (2016) Primary progress measures. Available online:
https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_da
ta/file/560969/Primary_school_accountability_summary.pdf.pdf [Accessed 13/07/2022].

DfE (2019) Progress measure scores for key stage 2: school performance tables. Available
online:
https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_da
ta/file/851788/KS2_progress_banding_calculations_bandings_2019.pdf [Accessed
05/07/2022].

DfE (2021a) All schools and colleges in England. Available online: https://www.compareschool-performance.service.gov.uk/schools-by-type?step=default&table=schools&region=allengland&for=primary [Accessed 28/07/2022].

DfE (2021b) Find and compare schools in England. Available online: https://www.compareschool-performance.service.gov.uk/ [Accessed 21/07/2022].

DfE (2022) Compulsory education. Available online: https://www.educationni.gov.uk/articles/compulsory-education [Accessed 7/11/2022].

EL (2021) Key Stage 2 SATs explained. Available online:
https://www.explorelearning.co.uk/preparing-for-the-sats/sats-key-stage-2-explained/
[Accessed 21/07/2022].

ERYC (2021) Quality of life. Available online: https://intel-hub.eastriding.gov.uk/ [Accessed
21/07/2022].

