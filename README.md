# MechaCar Statistical Analysis

## Linear Regression to Predict MPG

![summary_linear_regression](https://user-images.githubusercontent.com/93888037/162664581-932a3b74-0485-4714-b195-9c9ecd24d42b.png)


According to our results, vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the linear model. 
The vehicle length and ground clearance have a significant impact on gas mileage (mpg). 

The slope of our line is not zero because the p-value of our linear regression analysis is 5.35 x 10^-11, which is much smaller than our assumed significance level of 0.05%. Therefore, we can state that there is sufficient evidence to reject our null hypothesis.

From our linear regression model, the adjusted r-squared value is 0.6825, which means that roughly 68% of the variablilty of our dependent variable (miles per gallon) is explained using this linear model.

## Summary Statistics on Suspension Coils

![total_summary](https://user-images.githubusercontent.com/93888037/162664607-15fbceaa-3b70-4770-bec2-2e167fd1bd7c.png)


After creating summary statistics for the suspension coil data, we can see that the average weight capacity is approximately 1499 PSI. 
The variance in the weight capacity is low, around 62 PSI.

![summary_by_lot](https://user-images.githubusercontent.com/93888037/162664631-8c01802c-64eb-48ec-9ead-8843e9f023e3.png)

However, when examining the PSI summary statistics by lot, we can see a significant difference in the data coming from Manufacturing Lot #3. 
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 
In both Lot 1 and Lot 2, these specifications are met easily, with both lots having a variance of under 10. The variance in Lot 3 is 170. 

While the design specifications were met when looking at the manufacturing lots as a whole, they are not being met by Lot 3. 

## T-Tests on Suspension Coils
For this data, our significance level is 0.05 percent.

![t_test_all_lots](https://user-images.githubusercontent.com/93888037/162664646-1aa9e9a1-a091-4468-99bb-0ca9234849f3.png)


When examining the t-test results for all three lots combined, we can see that there is not enough evidence to reject the null hypothesis because the p-value is greater than 0.05. The two means are statistically similar. 

We have similar results when examining the data from Lots 1 and 2 individually. See the results below: 

![t_test_lot_1](https://user-images.githubusercontent.com/93888037/162664656-e88fc997-f53d-42fa-b860-5d5d82b71b39.png)

![t_test_lot_2](https://user-images.githubusercontent.com/93888037/162664668-14731644-aea5-4a3b-92e7-f0abd7f14fdc.png)


However, when examining Lot 3's individual data, we can see that we do have enough evidence to reject the null hypothesis. The p-value is below 0.05 at 0.04. These means are not statistically similar. 

![t_test_lot_3](https://user-images.githubusercontent.com/93888037/162664679-354375cb-90e8-4204-9c84-270d1d71a320.png)


Based on both the summary statistics and the t-tests, there appears to be a variation in production occurring in Lot 3.

## Study Design: MechaCar vs Competition 
With the cost of living in America rising every second, I believe that it is vital to compare the MechaCar's city fuel efficiency and maintenance cost to vehicles from other manufacturers. Consumers want a car that has value every single day, so these two metrics will impact them the most. 

We would test the null hypothesis that the MechaCar cannot have a lower "Everday Value" than its competitors. This means that the mean city fuel efficiency is not statistically different from the mean fuel efficiency of its competitors AND the mean maintenance cost is not statistically lower than its competitors.
Of course, we would hope to be able to reject this null hypothesis and accept the alternative hypothesis that the MechaCar's city fuel efficiency and maintenance costs are statistically lower than its competitors. 

I would want to use an ANOVA test for this hypothesis because the ANOVA test can tell us if there is a statistical difference between the distribution means from multiple samples. We would want to see how the MechaCar stacks up against multiple competitors, so the ANOVA test would be our best plan of attack. 

In order to run this statistical test, we would need the average city mpg and average yearly maintenance cost for the closest competitor to the MechaCar from each car manufacturer.
