R_Module4_Practice_Problem
================

## R-Class Module 4 Practice Problem 1

#### 1. Create a data.frame called running with the following data

``` r
running <- data.frame(Name = c("Sally", "Mike", "Carol"), Gender = c("F", "M", "F"), TenK = c(55, 46, 62), PR = c(52, 44, 58), Qualified = c(FALSE, TRUE, FALSE))
running
```

    ##    Name Gender TenK PR Qualified
    ## 1 Sally      F   55 52     FALSE
    ## 2  Mike      M   46 44      TRUE
    ## 3 Carol      F   62 58     FALSE

#### 2. Add the following column to running

``` r
running$HalfMarathon = c(120, 100, 140)
running
```

    ##    Name Gender TenK PR Qualified HalfMarathon
    ## 1 Sally      F   55 52     FALSE          120
    ## 2  Mike      M   46 44      TRUE          100
    ## 3 Carol      F   62 58     FALSE          140

#### 3. Add the following row to running

``` r
newRow = data.frame(Name = "Sage", Gender = "M", TenK = 40, PR = 42, Qualified = TRUE, HalfMarathon = 81)
running <- rbind(running, newRow)
running
```

    ##    Name Gender TenK PR Qualified HalfMarathon
    ## 1 Sally      F   55 52     FALSE          120
    ## 2  Mike      M   46 44      TRUE          100
    ## 3 Carol      F   62 58     FALSE          140
    ## 4  Sage      M   40 42      TRUE           81

## R-Class Module 4 Practice Problem 2

#### 1. Create a list new_list with the following members

-   1st member: a vector of length 10 from uniform distribution from -2
    to 2  
-   2nd member: a matrix from 1:10, with 2 rows, 5 columns, fill by row
-   3rd member: the running data.frame

``` r
new_list <- list(runif(10, -2, 2), matrix(1:10, 2, 5, byrow = TRUE), running)
new_list
```

    ## [[1]]
    ##  [1] -0.440017343  0.003742931 -1.177109864 -1.055749844 -0.979237525
    ##  [6]  1.585433240 -1.520011089  0.917212589  1.203999438 -1.478099315
    ## 
    ## [[2]]
    ##      [,1] [,2] [,3] [,4] [,5]
    ## [1,]    1    2    3    4    5
    ## [2,]    6    7    8    9   10
    ## 
    ## [[3]]
    ##    Name Gender TenK PR Qualified HalfMarathon
    ## 1 Sally      F   55 52     FALSE          120
    ## 2  Mike      M   46 44      TRUE          100
    ## 3 Carol      F   62 58     FALSE          140
    ## 4  Sage      M   40 42      TRUE           81

#### 2. Add 2 to each element of the first member of new_list

``` r
new_list[[1]] + 2
```

    ##  [1] 1.5599827 2.0037429 0.8228901 0.9442502 1.0207625 3.5854332 0.4799889
    ##  [8] 2.9172126 3.2039994 0.5219007

#### 3. Calculate the sum of the 2nd member of new_list

``` r
sum(new_list[[2]])
```

    ## [1] 55

#### 4. Remove the 3rd member of new_list

``` r
new_list[[3]] = NULL
new_list
```

    ## [[1]]
    ##  [1] -0.440017343  0.003742931 -1.177109864 -1.055749844 -0.979237525
    ##  [6]  1.585433240 -1.520011089  0.917212589  1.203999438 -1.478099315
    ## 
    ## [[2]]
    ##      [,1] [,2] [,3] [,4] [,5]
    ## [1,]    1    2    3    4    5
    ## [2,]    6    7    8    9   10

## R-Class Module 4 Practice Problem 3

#### 1. Create a ordered factor mons from the following character vector:

c(“March”,“April”,“January”,“November”,“January”,“September”,“Octo
ber”,“September”,“November”,“August”,“January”,“November”,“Nove
mber”,“February”,“May”,““July”,“December”,“August”,“August”,“Septe
mber”,“November”, “February”,“April”)

``` r
mons <- c("March","April","January","November","January","September","October","September","November","August","January","November","November","February","May","July","December","August","August","September","November","February","April")
factor(mons, levels = c("January", "February", "March","April", "May", "June", "July", "August", "September", "October", "November","December"), ordered = TRUE)
```

    ##  [1] March     April     January   November  January   September October  
    ##  [8] September November  August    January   November  November  February 
    ## [15] May       July      December  August    August    September November 
    ## [22] February  April    
    ## 12 Levels: January < February < March < April < May < June < ... < December

#### 2. Count the occurrence of each month

``` r
table(mons)
```

    ## mons
    ##     April    August  December  February   January      July     March       May 
    ##         2         3         1         2         3         1         1         1 
    ##  November   October September 
    ##         5         1         3

#### 3. Create a factor factor_weight with the weight of women of 2 levels

``` r
head(women)
```

    ##   height weight
    ## 1     58    115
    ## 2     59    117
    ## 3     60    120
    ## 4     61    123
    ## 5     62    126
    ## 6     63    129

``` r
factor_weight <- cut(women$weight, 2, labels = c("Low", "High"))
```

#### 4. Assign levels of “Low” and “High” to the factor

``` r
table(factor_weight)
```

    ## factor_weight
    ##  Low High 
    ##    9    6
