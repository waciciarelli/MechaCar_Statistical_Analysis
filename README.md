# MechaCar_Statistical_Analysis

This analysis is a statistical analysis of production data for AutoRUs' newest prototype of the MechaCar. This analysis provides insight that may assist the manufacturing team with production troubles.

## Linear Regression to Predict MPG

![linear regression](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/summary().png?raw=true)

### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

When determining if a variable or coefficient provides a non-random amount of variance, the "Pr(>|t|)" value is used. The closer this number is to 0, the less likely that the variable/coefficient is to provide a random amount of variance. As such, The Intercept, vehicle_length, and ground_clearance are unlikely to provide a random amount of variance.

### Is the slope of the linear model considered to be zero? Why or why not?

The slope of this model is not zero as determined by reviewing the p-value. This p-value is 5.35e-11 which is much smaller than the assumed significance value of 0.05. As such, there is sufficient evidence to reject the null hypothesis.

### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

This summary model is somewhat effective in predicting the mpg of MechaCar prototypes. This is determined by the Multiplied R-squared value which is 0.7149. This means that around 71.49% of the variability of the dependent variables is explained in this model.

## Summary Statistics on Suspension Coils

### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

![Total Summary](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/total_summary.png?raw=true)

When looking at whether or not the current manufacturing data meet this design specification, we must first look at the data as a whole. The table above gives us a statistical analysis of all manufacturing lots and their PSI's. The variance of this analysis is 62.30 PSI, which is less than the dictated 100 PSI.

![Lot Summary](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/lot_summary.png?raw=true)

Next, we look at the statistical analysis of each of the 3 lots to determine if they meet this standard as well. While Lot 1 and Lot 2 meet this standard with variances of 0.98 PSI and 7.47 PSI respectively, Lot 3 far exceeds this standard with a variance of 170.29 PSI.

## T-Tests on Suspension Coils
### summary of the t-test results across all manufacturing lots and for each lot

The following are one-sample t-tests on the Suspension Coil data. This investigates whether the PSI across all manufacturing lots is statistically different from the population mean of 1,500 PSI.

![T test for all Lots](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/ttest()%203.1.png?raw=true)

Above is the t-test for all manufactuting lots. The p-value of this t-test is 0.06028. Because our significance value is 0.05, we fail to reject our null hypothesis. As such, there is no significant difference between the PSI of all of the manufacturing lots as a whole and the population mean of 1,500 PSI.

![t test Lot 1](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/ttest()%203.2%20Lot1.png?raw=true)

The t-test for Lot 1 is shown above. In Lot 1, the p-value is 1. As was demonstrated early in the statistical analysis of Lot 1, the mean for Lot 1 is 1,500 PSI meaning there is no difference between the sample mean and the population mean. We fail to reject the null hypothesis for Lot 1.

![t test Lot 2](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/ttest()%203.2%20Lot2.png?raw=true)

The t-test for Lot 2 is shown above. In Lot 2, the p-value is 0.6072. With a significance value of 0.05, we fail to reject the null hypothesis for Lot 2. This means there is no significant difference between the PSI of Lot 2 and the population mean.

![t test Lot 3](https://github.com/waciciarelli/MechaCar_Statistical_Analysis/blob/main/Screenshots/ttest()%203.2%20Lot3.png?raw=true)

The t-test for Lot 3 is shown above. In Lot 3, the p-value is 0.04168. Because our significance value is 0.05, we reject this null hypotheis. This means that there is a significant difference between the PSI of Lot 3 and the population mean.

## Study Design: MechaCar vs Competition
### Short Description of a Statistical Study

To create a study of MechaCar versus its competition, we would need to investigate similar makes and models to the MechaCar to see how they perform mgp and sales-wise. 

### What metric or metrics are you going to test?
For this study we would need to consider that which the consumer would consider. This includes, but is not limited to:
* City and Highway Fuel Efficiency
* Cost
* Maintenance Cost
* Interior Design and Comfort
* Technology

### What is the null hypothesis or alternative hypothesis?

The null hypothesis of this test bould be that consumers are more likely to purchase vehicles with high MPG's

### What statistical test would you use to test the hypothesis? And why?

For this study, I would use Multiple Linear Regression. With this, we could assess the relationship between the competitor's car sales and MPG to determine wheter more cars with higher MPG are purchased compared to cars with lower MPG.

### What data is needed to run the statistical test?

To test this, we would need to consider the MPG's and number of sales of cars of similar makes and models as the MechaCar.
