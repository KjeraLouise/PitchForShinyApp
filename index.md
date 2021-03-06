---
title       : Calculate Days Before/After a Given Date
subtitle    : Developing Data Products Course Project
author      : Kjera Seregi
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [shiny, interactive, bootstrap]            # {mathjax, quiz, bootstrap}
mode        : selfcontained  # {standalone, draft}
knit        : slidify::knit2slides

    
---
## Why this App is Helpful
    1. Setting trackable, measureable professional and personal goals
        a. Weight loss
        b. Finish Coursera certificate
        c. Submit article
    2. Pace your event planning
        a. Anniversaries, birthdays, graduations
    3. Keeping yourself in check - How long has it actually been since...
        a. Making those New Year resolutions
        b. Saying you would start that project


---
## How the App Works Example - Bob's Garage
    1. Over the 4th of July holiday Bob Sitsalot said he would clean his garage.
    2. Bob has done nothing with this.  How long has it been?

```r
Date1 <- as.Date("2015-07-04"); DaysLeft <- difftime(Date1,Sys.Date(), units="days")
Days <- as.character(abs(DaysLeft), units = "days")
    if (Date1 < Sys.Date() ){
    Reply  <- paste("That date was ", Days, " day(s) ago.", sep="")
    }else if (Date1 == Sys.Date() ){
    Reply <- "That is today!"
    }else {
    Reply <- paste("That date is ", Days , " day(s) away.", sep="")
    }
Reply
```

```
## [1] "That date was 319 day(s) ago."
```



---
## Bob's Garage - continued
1. Bob understands the time he wasted and will now set a new, measurable goal.
2. Clean the garage before the weather gets cold... say October 15th. How long 
until this date?

```r
    Date1 <- as.Date("2016-10-15")
    DaysLeft <- difftime(Date1,Sys.Date(), units="days")
    Days <- as.character(abs(DaysLeft), units = "days")
        if (Date1 < Sys.Date() ){
        Reply  <- paste("That date was ", Days, " day(s) ago.", sep="")
        }else if (Date1 == Sys.Date() ){
        Reply <- "That is today!"
        }else {
        Reply <- paste("That date is ", Days , " day(s) away.", sep="")
        }
    Reply
```

```
## [1] "That date is 150 day(s) away."
```



---
## Happy Planning!!!
1. Use this app to help your planning and time awareness/management.
2. Check regularly, to stay on track.  
3. Rememember Bob's example. The number of days Bob has left until his goal date is: 
      
      ```
      ## [1] "150"
      ```
3. Good Luck working toward your goal(s)!!!


