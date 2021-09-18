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

## Linear Regression to Predict MPG

In this section, we created a linear regression model to see if we could preduc the mpg by using several variables (vehicle length, vehicle weight, spoiler-angle, ground clearance, and all-wheel-drive). We then used the summary() function to determine the p-value and r-squared values for our linear regression model of our data. Please see below for the Linear Regression Model and the summary of the data:


![linear-regression](https://user-images.githubusercontent.com/84881187/133892937-703e02b2-f7da-446c-b06d-46458a244387.PNG)

![p=Value and r-Squared Summary](https://user-images.githubusercontent.com/84881187/133893081-c0f5a62a-fcb2-4d9a-a756-f3a77ddff0cd.PNG)


When we examine our dataset, the most significant variables that provide a non-random amount of variance to the mpg-values are the Vehicle Length and the Ground Clearance. Examining the visuals above, the linear regression model shows that these variables tested against MPG result in p-values of 2.6e-12 for Vehicle Length and 5.21e-08 for Ground Clearance. The (Intercept) also has significance at 5.08e-8, indicating that there are other variables, not included in our dataset that have a significant impact on MPG.

Looking at our linear model, we can conclude that the slope is not considered to be zero, because some of our independent variables had a significant effect on the dependent variable. When we look at our P-Value of 5.35e-11, we see that the value is less than zero.

The linear progression model does a good job at predicting the MPG of MechaCar prototypes, but there are still some unrecorded variables that could alter our data's strength. Looking at our R-Squared value of 0.7149, we can determine that the efficacy of our linear regression model is about 71% accurate. 

## Summary Statistics on Suspension Coils

Our next step is to load our suspension coils data. The suspencion data is comprised of 150 different vehicle IDs, 3 different lot numbers, and corresponding PSI levels for each vehcile. We created summary tables for a Total Summary of the Mean, Median, Variance, and Standard Deviation of our data; and a Lot Summary Table to examine the 3 different lots the MechaCars are sorted into. Please see below for our Summary Tables:

#### Total Summary Table
![Suspension Coil Total Summary](https://user-images.githubusercontent.com/84881187/133894566-7ffe94f3-3518-450d-8cb1-d6bcdd929b5e.PNG)

332

#### Lot Summary Table
![lot summary](https://user-images.githubusercontent.com/84881187/133894573-0625356c-14ed-4e04-bc18-075f19ff80d1.PNG)

When we look at the Total Summay chart, the current variance is 62.29, which does meet the manufacturer's design specifications. However, when we examine the variance data within the individual lots, we see much greater variance within the Lot Summary Data. While Lot 1 and Lot 2 are well within the manufacturer's specification standards with variances of 0.98 and 7.47 respectively, Lot 3 has a variance of 170.29. Lot 3 is well above the manufacturer's specification where the variance must of the suspencion coils must not exceed 100lbs per square inch. 

### T-Test on Suspension Coils

In our final analysis, we wanted to determine if all of the manufacturing lots and each lot individually are statistically different from the population mean of 1,500lbs per square inch. To do so, we ran a Total Lots T-Test and a T-Test on each of the 3 lots. Please see below for the data for each:


#### Total Lots T-Test

![One-Sample T-Test](https://user-images.githubusercontent.com/84881187/133894949-41b9e433-7e3f-403f-992d-8487e10a8617.PNG)


#### Lot 1 T-Test
![Lot_1_T-Test](https://user-images.githubusercontent.com/84881187/133894958-90e780a5-c3f6-4bf2-b240-b4fd43805248.PNG)



#### Lot 2 T-Test
![Lot_2_T-Test](https://user-images.githubusercontent.com/84881187/133894964-5789349a-7fc5-4093-a1eb-7dcb3ac498da.PNG)


#### Lot 3 T-Test
![Lot_3_T-Test](https://user-images.githubusercontent.com/84881187/133894985-baae076a-dd13-46da-9d8a-212b54d9a34c.PNG)

Looking at the results of out T-Test across all manufacturing lots' suspencion coils, we can see that they are not statistically different from the population mean with all Means being within reasonable range of 1500lbs per square inch. All of our p-values across the Total and individual Lot values are greater than 0.5, with the exception of Lot 3 with a p-value 0.4168. This shows that Lot 3 suspencion coils differ from the population mean slightly, and further testing should be done on this lot.


## Study Design: MechaCar vs Competition

Our analysis on AutosRUs' MechaCars yielded results that will help point the manufacturing team in the right direction to resolves the troubles blocking their progress. However, even with the data we have now, we can still design a study to improve and strengthen our data's significance. We could also design a study to compare performance of the MechaCar vehicles aginst the performance of vehicles from other manufascturers.

Thinking of customer satisfaction and vehicle quality there are several metrics we would need to test the MechaCar against. To go along with the data we have already collected, we should also test fuel efficiency across, city, highway, and rural areas. We could also test for the car's horsepower, weight, and engine size to go along with our MPG data to give our customers a better view of a car's performance against competitors. 

If we focusedon fuel efficiency along with MPG, our Null Hypothesis would be that all cars of similar type/class would have the same levels of fuel efficiency, and our Alternative Hypothesis would state that not all cars by type/class have the same fuel efficiency. It would be beneficial for us to run ANOVA tests to test the fuel efficiency across multiple variables. We would also create several visualizations to show the variances within our data. 

In order to get a more accurate description of analysis, we would need to collect more data. We would need to collect a significant sample size of fuel efficiency across each care class/type. We would need appropriately tested data, and variable data for each car and each car type/class.


