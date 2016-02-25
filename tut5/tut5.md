Chen Jiesheng (A0099515U)

    country <- read.spss(file="country122.sav", use.value.labels=TRUE, max.value.labels=Inf, to.data.frame=TRUE)
    colnames(country) <- tolower(colnames(country))

    reg1 <- lm(lifeexpf~birthrat, data=country)
    summary(reg1)

    ## 
    ## Call:
    ## lm(formula = lifeexpf ~ birthrat, data = country)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -17.3110  -2.6524  -0.0768   3.1784  18.1892 
    ## 
    ## Coefficients:
    ##             Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept) 89.58892    1.31645   68.05   <2e-16 ***
    ## birthrat    -0.74471    0.03878  -19.20   <2e-16 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 5.619 on 119 degrees of freedom
    ##   (1 observation deleted due to missingness)
    ## Multiple R-squared:  0.756,  Adjusted R-squared:  0.754 
    ## F-statistic: 368.8 on 1 and 119 DF,  p-value: < 2.2e-16

Given that the p-value is smaller than 0.05, it is statistically
significant that there is a linear relationship between life expectancy
and birth rate.

R-square is 75.4%, so the relationship is pretty strong.

    scatterplot(lifeexpf~birthrat, reg.line=lm, boxplots=FALSE, data=country)

![](tut5_files/figure-markdown_strict/unnamed-chunk-4-1.png)  
 Hence, the simple linear equation is life expectancy = -0.74471 \*
birth rate + 89.58892

Given birthrate of 25 livebirths per 1000 population, life expectancy =

    -0.74471 * 0.025 + 89.58892

    ## [1] 89.5703

The assumptions are that birthrate given is representative to the
population birthrate, not anomaly.
