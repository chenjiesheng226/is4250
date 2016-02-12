    ## Warning: package 'ggplot2' was built under R version 3.2.3

    ## Warning: package 'dplyr' was built under R version 3.2.3

1.  

<!-- -->

    ##                       Diabetic Complications Present
    ## Diabetic Control Good                              3
    ## Diabetic Control Poor                              4
    ##                       Diabetic Complications Absent
    ## Diabetic Control Good                             7
    ## Diabetic Control Poor                             2

    ##                       Diabetic Complications Present
    ## Diabetic Control Good                      0.3000000
    ## Diabetic Control Poor                      0.6666667
    ##                       Diabetic Complications Absent
    ## Diabetic Control Good                     0.7000000
    ## Diabetic Control Poor                     0.3333333

From above table, indeed it is different.

1.  

<!-- -->

    ## 
    ##  Welch Two Sample t-test
    ## 
    ## data:  prop.table(B, 1)[, 1] and prop.table(B, 1)[, 2]
    ## t = -0.12856, df = 2, p-value = 0.9095
    ## alternative hypothesis: true difference in means is not equal to 0
    ## 95 percent confidence interval:
    ##  -1.148893  1.082226
    ## sample estimates:
    ## mean of x mean of y 
    ## 0.4833333 0.5166667

    ## 
    ##  Fisher's Exact Test for Count Data
    ## 
    ## data:  B
    ## p-value = 0.3024
    ## alternative hypothesis: true odds ratio is not equal to 1
    ## 95 percent confidence interval:
    ##  0.0137305 2.7634624
    ## sample estimates:
    ## odds ratio 
    ##  0.2384682

Given the fisher test, p-value is 0.3024 \> 0.05. Hence, the difference
between the two rates is not statistically different.

1.  Pearson's chi-squared test (χ2) is a statistical test applied to
    sets of categorical data to evaluate how likely it is that any
    observed difference between the sets arose by chance.

Since there are no categorical data in this matrix, chi-squired test is
not applicable.
