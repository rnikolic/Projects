1. Introduction
---------------

This document contains few Data Visualization Use Cases

2. Plane Crashes
----------------

The first one was inspired by the latest plane crash in Europe.

Data were extracted from database of plane acccidents hosted at:

<http://planecrashinfo.com>.

Fro data aquisition R code posted by Phill Jette was used

<https://github.com/philjette/CrashData/blob/master/PlaneCrashes.R>

So here we started with preprocessed data.

    library(ggplot2)

    setwd("C:/_RADINA/R/Planes")
    crashData = read.csv("data/CompiledCrashData.csv", header=TRUE)

### Plane Crashes Data Visualization

![plot of chunk
unnamed-chunk-2](./2015_RN_VIS_files/figure-markdown_strict/unnamed-chunk-2.png)

### Plane Crashes Data Summary Statistics

    summary(crashData)

    ##        X             crashDates               crashLocation 
    ##  Min.   :   1   1960-02-26:   4   Moscow, Russia     :  27  
    ##  1st Qu.:1146   1973-02-28:   4   Bogota, Colombia   :  17  
    ##  Median :2292   1976-08-28:   4   Cairo, Egypt       :  17  
    ##  Mean   :2292   1988-08-31:   4   Manila, Philippines:  17  
    ##  3rd Qu.:3438   1992-08-27:   4   Anchorage, Alaska  :  15  
    ##  Max.   :4583   2001-09-11:   4   Sao Paulo, Brazil  :  13  
    ##                 (Other)   :4559   (Other)            :4477  
    ##                     crashOperator  
    ##  Aeroflot\n                 : 245  
    ##  Military - U.S. Air Force\n: 166  
    ##  Indian Airlines\n          :  34  
    ##  Air France\n               :  32  
    ##  Air Taxi\n                 :  31  
    ##  Philippine Air Lines\n     :  31  
    ##  (Other)                    :4044  
    ##                                     crashType      crashOutcome 
    ##  Douglas DC-3                            : 263   2/2(0)  : 262  
    ##  de Havilland Canada DHC-6 Twin Otter 300:  86   3/3(0)  : 248  
    ##  Douglas C-47A                           :  58   4/4(0)  : 195  
    ##  Douglas C-47                            :  37   5/5(0)  : 149  
    ##  Yakovlev YAK-40                         :  37   6/6(0)  : 134  
    ##  Antonov AN-26                           :  35   10/10(0): 125  
    ##  (Other)                                 :4067   (Other) :3470  
    ##      crashF          crashP           Prop        crashYear   
    ##  Min.   :  0.0   Min.   :  0.0   Min.   :0.00   Min.   :1950  
    ##  1st Qu.:  3.0   1st Qu.:  6.0   1st Qu.:0.78   1st Qu.:1967  
    ##  Median : 10.0   Median : 14.0   Median :1.00   Median :1980  
    ##  Mean   : 22.1   Mean   : 30.9   Mean   :0.83   Mean   :1981  
    ##  3rd Qu.: 25.0   3rd Qu.: 35.0   3rd Qu.:1.00   3rd Qu.:1995  
    ##  Max.   :583.0   Max.   :644.0   Max.   :1.00   Max.   :2015  
    ##  NA's   :2       NA's   :30      NA's   :32                   
    ##                crashLococation
    ##  Moscow, Russia        :  27  
    ##  Manila, Philippines   :  18  
    ##  Bogota, Colombia      :  17  
    ##  Cairo, Egypt          :  17  
    ##  Anchorage, Alaska     :  15  
    ##  Rio de Janeiro, Brazil:  13  
    ##  (Other)               :4476
