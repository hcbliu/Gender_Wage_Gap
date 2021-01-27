Final Project
================
Hui-Chen Betty Liu
December 6, 2019

### Problem Statement

> Is there a significant difference in income between men and women?
> Does the difference vary depending on other factors (e.g., education,
> marital status, criminal history, drug use, childhood household
> factors, profession, etc.)?

    ## 
    ## Call:
    ## lm(formula = income2012 ~ gender + race + jobs.held1990, data = nlsydata1)
    ## 
    ## Residuals:
    ##    Min     1Q Median     3Q    Max 
    ## -66880 -22624 -14597  10229 336254 
    ## 
    ## Coefficients:
    ##                Estimate Std. Error t value  Pr(>|t|)    
    ## (Intercept)    23750.95     748.65  31.725   < 2e-16 ***
    ## genderFemale  -11160.45     807.75 -13.817   < 2e-16 ***
    ## raceHispanic    1124.81    1143.84   0.983     0.325    
    ## raceBlack      -4144.16     962.91  -4.304 0.0000169 ***
    ## jobs.held1990   1002.88      63.28  15.849   < 2e-16 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 45470 on 12681 degrees of freedom
    ## Multiple R-squared:  0.03632,    Adjusted R-squared:  0.03601 
    ## F-statistic: 119.5 on 4 and 12681 DF,  p-value: < 2.2e-16

    ## Analysis of Variance Table
    ## 
    ## Model 1: income2012 ~ gender + jobs.held1990
    ## Model 2: income2012 ~ gender + race + jobs.held1990
    ##   Res.Df            RSS Df   Sum of Sq      F     Pr(>F)    
    ## 1  12683 26271361125224                                     
    ## 2  12681 26223706960785  2 47654164439 11.522 0.00001001 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

    ## 
    ## Call:
    ## lm(formula = income2012 ~ gender + race + jobs.held1990 + gender:race, 
    ##     data = nlsydata1)
    ## 
    ## Residuals:
    ##    Min     1Q Median     3Q    Max 
    ## -69728 -21639 -14458   9525 338516 
    ## 
    ## Coefficients:
    ##                            Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)                25610.20     809.04  31.655  < 2e-16 ***
    ## genderFemale              -15166.83    1048.24 -14.469  < 2e-16 ***
    ## raceHispanic               -2037.11    1615.60  -1.261  0.20737    
    ## raceBlack                 -10070.08    1350.20  -7.458 9.34e-14 ***
    ## jobs.held1990               1025.88      63.32  16.203  < 2e-16 ***
    ## genderFemale:raceHispanic   6354.36    2287.42   2.778  0.00548 ** 
    ## genderFemale:raceBlack     12033.02    1925.17   6.250 4.23e-10 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 45410 on 12679 degrees of freedom
    ## Multiple R-squared:  0.0394, Adjusted R-squared:  0.03894 
    ## F-statistic: 86.66 on 6 and 12679 DF,  p-value: < 2.2e-16

|               | Estimate | Std. Error | t value | Pr(\>|t|) |
| :------------ | -------: | ---------: | ------: | --------: |
| (Intercept)   |    23751 |        749 |   31.73 |    0.0000 |
| genderFemale  |  \-11160 |        808 | \-13.82 |    0.0000 |
| raceHispanic  |     1125 |       1144 |    0.98 |    0.3254 |
| raceBlack     |   \-4144 |        963 |  \-4.30 |    0.0000 |
| jobs.held1990 |     1003 |         63 |   15.85 |    0.0000 |

**(0)** Data cleaning and data exploration

    ## # A tibble: 3 x 5
    ##   race     income.gap  upper  lower is.significant
    ##   <fct>         <dbl>  <dbl>  <dbl>          <dbl>
    ## 1 Other        14766. 12486. 17045.              1
    ## 2 Hispanic     10387.  6558. 14215.              1
    ## 3 Black         4285.  1956.  6613.              1

![](FinalRProject_HuiChenBettyLiu_github_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

**(1)** Data Summary

**(2)** Methodology

**(3)** Findings

**(4)** Discussion
