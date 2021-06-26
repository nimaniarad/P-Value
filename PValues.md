
*P-Values Concept*

Using Heart Disease UCI Data Set
:<https://www.kaggle.com/ronitf/heart-disease-uci>

    ## 
    ## -- Column specification --------------------------------------------------------
    ## cols(
    ##   age = col_double(),
    ##   sex = col_double(),
    ##   cp = col_double(),
    ##   trestbps = col_double(),
    ##   chol = col_double(),
    ##   fbs = col_double(),
    ##   restecg = col_double(),
    ##   thalach = col_double(),
    ##   exang = col_double(),
    ##   oldpeak = col_double(),
    ##   slope = col_double(),
    ##   ca = col_double(),
    ##   thal = col_double(),
    ##   target = col_double()
    ## )

*Regression*

``` r
lm.fit.1 = lm(age ~ chol + trestbps + fbs, data = Heart)
summary(lm.fit.1)
```

    ## 
    ## Call:
    ## lm(formula = age ~ chol + trestbps + fbs, data = Heart)
    ## 
    ## Residuals:
    ##     Min      1Q  Median      3Q     Max 
    ## -23.522  -6.156   0.375   6.053  22.507 
    ## 
    ## Coefficients:
    ##             Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept) 29.60494    4.21865   7.018 1.52e-11 ***
    ## chol         0.03201    0.00960   3.335 0.000962 ***
    ## trestbps     0.12605    0.02883   4.373 1.70e-05 ***
    ## fbs          1.92927    1.40865   1.370 0.171845    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 8.581 on 299 degrees of freedom
    ## Multiple R-squared:  0.1162, Adjusted R-squared:  0.1073 
    ## F-statistic: 13.11 on 3 and 299 DF,  p-value: 4.602e-08

*chol* & *trestbps* have P-Values close to zero which means they are
playing a key role in connection with age. Technically, it is said they
are statistically significant.

The question is what it means exactly? Imagine you have a friend named
Jimmy that goes to a specific bar every Friday night and drink a lot. He
brings a lot of friends with himself too. He goes other night too, but
you are not sure about it. The bar owner asks you to find out if Jimmy
is playing a key role on increasing their profit on Friday nights much
more than other busy nights there like Saturdays. When you collecting
the data, you got a distribution of revenue based on the number of
drinks. You find out because of Jimmy, they make much more money on
Friday nights. The bar owner asks you he sometimes see Jimmy on other
nights too, would you tell me if Jimmy can play a key role on other
nights too? You are going to say to the owner that no, just Friday
nights and Jimmy roles is not significant on other nights. What are you
saying is there is slight chance that you can find Jimmy here at other
nights, but he is here on Friday nights and making more money for you!
So, Jimmy is playing a key role on the bar profit even if you consider
other nights too. So, it is not by chance that Jimmy brings more money
for the bar, however, we cannot find him in other nights. It means
P-Values for Jimmy would be close to zero for other nights but he plays
a key role on making more money for the bar.
