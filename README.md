# Mecha Car Statistical Analysis

## Overview
In this project, We helped Jeremy and his Data Analytics Team to analyze the production problems of AutosRU company's newest prototype "Mecha Car". Our job was to review the production data insights to support the manufacturing team.

In other words, our **purpose** was to perform a multiple linear regression, some t-tests, and other statistical tests in Mecha Car datasets in order to understand and find production problems. 

In addition, We designed a statistical study to compare the vehicle performance of the Mecha Car vehicles against vehicles from other manufacturers.

To accomplish our goal, We used various resources, such as **R, RStudio, Tidiverse, Dpylr, and two csv files**.

## Results

### Linear regression model to predict MPG
Our first objective was to perform a Multiple Linear Regression using R language to predict miles-per-gallon (mpg). 

##### Linear regresion model
![Alt text](/Resources/lm.png "imagen1")

##### Summary of linear regression model
![Alt text](/Resources/lm_summary.png "imagen2")

**- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**

The variables/coefficients **Vehicle Length** and **Ground Clearance** are statistically significant because their p-values are below 0.05. That also means that those variables provide a non-random amount of variance to the mpg values. 

**- Is the slope of the linear model considered to be zero? Why or why not?**

The slope is not zero as the p-value of the linear model is 5.35e-11, which is so much smaller than 0.05. 

**- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**

The r-squared value is 0.7149, which means a substantial correlation for the dataset. We can conclude that the model can predict an approximate 71 percent of mpg (miles-per-gallon) of Mecha Car prototypes effectively.

### Summary statistics on suspension coils
Below we present the results of our second goal, which was to study statistics on suspension coils.

##### Summary statistics for all lots
![Alt text](/Resources/statistics1.png "imagen3")

##### Summary statistics for each lot
![Alt text](/Resources/statistics2.png "imagen9")

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 
**- Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?**

The summary statistics for all lots shows a variance of **62.29356** pounds, which is fine as the design specification of Mecha Car states that the variance of the suspension coils must not exceed 100 pounds per square inch.

Analyzing the variance for each lot individually reveals that **Lot3 does not meet the parameters, because its variance is 170.2861224 and surpasses 100 pounds per square inch**.

### T-test on Suspension Coils
In addition, we performed t-tests to know if all manufacturing lots and each lot individually are statistically different from the population mean of 1500 pounds per square inch

##### T-test of all manufacturing lots
![Alt text](/Resources/lots.png "imagen7")
- All manufacturing lots - p-value= 0.06028.

As we can see, the p-value is more than 0.05, which means that the total manufacturing lot is not statistically different from the population mean.

##### T-tests of each manifacturing lots individually 
![Alt text](/Resources/lot1.png "imagen4")
![Alt text](/Resources/lot2.png "imagen5")
![Alt text](/Resources/lot3.png "imagen6")
- Lot1 - p-value= 1
- Lot2 - p-value= 0.6072
- Lot3 - p-value= 0.04168

Lot1 and Lot2 are not statistically different from the population mean as their p-values are more than 0.05. Therefore we found that **Lot3** is statistically different from the population mean as the p-value is less than 0.05, which also means that we have to reject the null hypothesis.

## Study design: Mecha Car vs Competition
In order to compare the performance of the MechaCar vehicles against the performance of vehicles from other manufacturers, we designed a statistical study on some important metrics associated with the utility of the vehicle.

##### The metrics that we choose are listed below:
- Cost
- Fuel efficiency (city and highway)
- Maintenance costs
- Safety ratings 

##### Null hypothesis (Ho): 
The performance of the metrics of the MechaCar vehicles against the performances of the metrics of the competitors' vehicles are the same and do not have a significant difference concerning utility.

##### Alternative Hypothesis (Ha): 
The performance of the metrics of the MechaCar vehicles  against the performance of the metrics of the competitors' vehicles are not the same and have a significant difference concerning utility

##### Statistical test
First, We determine to perform multiples linear regressions to find if there are differences between the variables examined.

Second, We also decide to perform an Analysis of Variance (ANOVA) to study the performance of the MechaCar vehicles versus the performance of the competition's vehicles. This study will help us validate to determine if the differences are statistically significant.

To carry out these statistical tests we need to obtain and collect data about the cost, fuel efficiency, maintenance costs, and safety ratings of MechaCar vehicles and the competition's vehicles. The sample must be random and significant. We recommend a sample greater than 50 per vehicle for the dataset.  
