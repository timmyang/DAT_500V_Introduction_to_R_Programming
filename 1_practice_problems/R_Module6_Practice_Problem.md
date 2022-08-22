R_Module6_Practice_Problem
================

## R-Class Module 6 Practice Problem 1

#### Refer to the daily sales-advertising data of a chocolate store presented in the table.

#### Conduct a hypothesis test (at α = 0.05) to determine if sales (y) is linearly related to advertising expenditure.

``` r
Sales <- c(1097, 1187, 1152, 1112, 1131, 1157, 1128, 1197, 1170, 1139)
Advertisement <- c(50, 100, 75, 50, 60, 70, 75, 100, 80, 75)

df1 <- cbind(Sales, Advertisement)
df1 <- as.data.frame(df1)
df1
```

    ##    Sales Advertisement
    ## 1   1097            50
    ## 2   1187           100
    ## 3   1152            75
    ## 4   1112            50
    ## 5   1131            60
    ## 6   1157            70
    ## 7   1128            75
    ## 8   1197           100
    ## 9   1170            80
    ## 10  1139            75

``` r
LinReg.Model <- lm(Sales ~ Advertisement, data = df1)
summary(LinReg.Model)
```

    ## 
    ## Call:
    ## lm(formula = Sales ~ Advertisement, data = df1)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -21.550  -8.797   3.696   6.454  15.951 
    ## 
    ## Coefficients:
    ##                Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)   1022.0300    17.6097  58.038 8.63e-12 ***
    ## Advertisement    1.7003     0.2337   7.275 8.59e-05 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 12.26 on 8 degrees of freedom
    ## Multiple R-squared:  0.8687, Adjusted R-squared:  0.8523 
    ## F-statistic: 52.93 on 1 and 8 DF,  p-value: 8.593e-05

There is a statistically significant evidence at 0.05 significance level
that Sales and Advertisement have a positive, linear relationship.

## R-Class Module 6 Practice Problem 2

#### A construction company employs three sales engineers. Engineers 1, 2, and 3 estimate the costs of 30%, 20%, and 50%, respectively, of all jobs bid by the company. For i = 1, 2, 3 define Ei to be the event that a job is estimated by engineer i. The following probabilities describe the rates at which the engineers make serious errors in estimating costs:P(error/E1) = 0.01, P(error/E2) = 0.03, and P(error/E3) = 0.02

#### Given there was an error, what is the probability that Engineer 3 made the error?estimated by engineer i. The following probabilities describe the rates at which the engineers make serious errors in estimating costs: P(error/E1) = 0.01, P(error/E2) = 0.03, and P(error/E3) = 0.02

#### Given there was an error, what is the probability that Engineer 3 made the error?

``` r
library(LaplacesDemon)

Prior = c(0.3,0.2,0.5)
Likelihood = c(0.01, 0.03, 0.02)

BayesTheorem(Prior,Likelihood)
```

    ## [1] 0.1578947 0.3157895 0.5263158
    ## attr(,"class")
    ## [1] "bayestheorem"

The probability that Engineer 3 made the error is 0.5263.
