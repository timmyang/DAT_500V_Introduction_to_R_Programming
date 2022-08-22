R_Module2_Practice_Problem
================

## R-Class Module 2 Practice Problem 1

#### 1. Create an empty numeric vector nv1 of length 6

``` r
nv1 <- numeric(6)
nv1
```

    ## [1] 0 0 0 0 0 0

#### 2. Create a numeric vector nv2 with even numbers from 2 to 20(2,4,. . . 20)

``` r
nv2 <- seq(from = 2,to = 20, by = 2)
nv2
```

    ##  [1]  2  4  6  8 10 12 14 16 18 20

#### 3. How many elements are there in nv2?

``` r
length(nv2)
```

    ## [1] 10

#### 4. What is the 6th element of nv2?

``` r
nv2[6]
```

    ## [1] 12

#### 5. Add a new value 22 to the end of nv2

``` r
nv2 <- c(nv2, 22)
nv2
```

    ##  [1]  2  4  6  8 10 12 14 16 18 20 22

#### 6. Delete 2 from nv2

``` r
nv2 <- nv2[-1]
```

#### 7. Print your new nv2

``` r
nv2
```

    ##  [1]  4  6  8 10 12 14 16 18 20 22

#### 8. Caluclate the mean(),min(),max(),sd() of nv2

``` r
mean(nv2)
```

    ## [1] 13

``` r
min(nv2)
```

    ## [1] 4

``` r
max(nv2)
```

    ## [1] 22

``` r
sd(nv2)
```

    ## [1] 6.055301

#### 9. Create a numeric vector nv3 from 1 to 10

``` r
nv3 <- 1:10
nv3
```

    ##  [1]  1  2  3  4  5  6  7  8  9 10

#### 10. Add 3 to each element of nv3

``` r
nv3 <- nv3 + 3
nv3
```

    ##  [1]  4  5  6  7  8  9 10 11 12 13

#### 11. Coerce nv3 to character

``` r
nv3 <- as.character(nv3)
```

#### 12. Print the new nv3

``` r
nv3
```

    ##  [1] "4"  "5"  "6"  "7"  "8"  "9"  "10" "11" "12" "13"

## R-Class Module 2 Practice Problem 2

#### 1. Use seq() to generate a vector v3 of length 15, odd numbers from 1 to

29

``` r
v3 <- seq(from = 1, to = 29, by = 2)
v3
```

    ##  [1]  1  3  5  7  9 11 13 15 17 19 21 23 25 27 29

#### 2. Use matrix() to construct m1 of 3\*5 from v3, fill by column

``` r
m1 <- matrix(data = v3, nrow = 3, ncol = 5)
m1
```

    ##      [,1] [,2] [,3] [,4] [,5]
    ## [1,]    1    7   13   19   25
    ## [2,]    3    9   15   21   27
    ## [3,]    5   11   17   23   29

#### 3. Use matrix() to construct m2 of 5\*3 from v3, fill by column

``` r
m2 <- matrix(data = v3, nrow = 5, ncol = 3)
m2
```

    ##      [,1] [,2] [,3]
    ## [1,]    1   11   21
    ## [2,]    3   13   23
    ## [3,]    5   15   25
    ## [4,]    7   17   27
    ## [5,]    9   19   29

#### 4. Add 1 to each element of m1

``` r
m1 + 1
```

    ##      [,1] [,2] [,3] [,4] [,5]
    ## [1,]    2    8   14   20   26
    ## [2,]    4   10   16   22   28
    ## [3,]    6   12   18   24   30
