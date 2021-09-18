# MechaCar_Statistical_Analysis

## Project Overview

AutosRUs' has tasked our team to help review their production data for insights that may help their manufacturing team's progress. Our analysis aims to:

  * Identify which variables predict the MP for their vehicle prototypes
  * Collect summary statistics on the PSI of the suspencion coils
  * Determine if manufacturing lots are statistically different from the mean
  * Design a study to compare performance against vehicles from other competeing manufacturers

## Results

First we imported the MechaCar_mpg.csv file to our active directory, and read it as a dataframe

![imported data](https://user-images.githubusercontent.com/84881187/133892824-dc3de7c9-d64d-4c8a-9716-08d6ce24edb2.PNG)


Now that we can see our data, we then designed a linear model to predict the mpg of MechaCar prorotypes, and create a summary of our data.

### Linear Regression to Predict MPG

In this section, we created a linear regression model to see if we could preduc the mpg by using several variables (vehicle length, vehicle weight, spoiler-angle, ground clearance, and all-wheel-drive). We then used the summary() function to determine the p-value and r-squared values for our linear regression model of our data. Please see below for the Linear Regression Model and the summary of the data:


![linear-regression](https://user-images.githubusercontent.com/84881187/133892937-703e02b2-f7da-446c-b06d-46458a244387.PNG)

![p=Value and r-Squared Summary](https://user-images.githubusercontent.com/84881187/133893081-c0f5a62a-fcb2-4d9a-a756-f3a77ddff0cd.PNG)


When we examine our dataset, the most significant variables that provide a non-random amount of variance to the mpg-values are the Vehicle Length and the Ground Clearance. Examining the visuals above, the linear regression model shows that these variables tested against MPG result in p-values of 2.6x10^-12 for Vehicle Length and 5.21X10^-8 for Ground Clearance. The (Intercept) also has significance at 5.08X10^-8, indicating that there are other variables, not included in our dataset that have a significant impact on MPG.

Looking at our linear model, we can conclude that the slope is not considered to be zero, because F-Statistic P-Value of 5.35X10^-11 is lower than a high level of significance. With this P-Value in mind, we would reject the null hypothesis. 


Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The linear progression model does a good job at predicting the MPG of MechaCar prototypes, but there are still some unrecorded variables that could alter our data's strength. Looking at our R-Squared value of 0.7149, we can determine that the efficacy of our linear regression model is about 71% accurate. 

### Summary Statistics on Suspension Coils

Our next step is to load our suspension coils data. The suspencion data is comprised of 150 different vehicle IDs, 3 different lot numbers, and corresponding PSI levels for each vehcile. We created summary tables for a Total Summary of the Mean, Median, Variance, and Standard Deviation of our data; and a Lot Summary Table to examine the 3 different lots the MechaCars are sorted into. Please see below for our Summary Tables:

#### Total Summary Table
![Suspension Coil Total Summary](https://user-images.githubusercontent.com/84881187/133894566-7ffe94f3-3518-450d-8cb1-d6bcdd929b5e.PNG)



#### Lot Summary Table
![lot summary](https://user-images.githubusercontent.com/84881187/133894573-0625356c-14ed-4e04-bc18-075f19ff80d1.PNG)




