# Histogram-and-Boxplot-in-R
 The following data was collected by the local hospital. This data set contains 5 variables based on observation of 8 patients. In addition to the measurements of the patients checking in to the hospital that night, this data provides the patients' histories regarding the frequency of their visits to the hospital in the last 12 months.

This data displays the measurement of blood pressure, first assessment by general doctor (bad=1, good =0) titled "first," the second assessment by external doctor (called "second"), and the last row provides the head of the emergency unit's decision regarding immediate care for the patient based on the values 0 or 1 (low = 0, high =1).
The names of your variables are as follows: "Freq","bloodp","first”, " second”, ”finaldecision”
The rows 
1.    "0.6","103","bad","low","low”
2.     "0.3","87","bad","low","high”
3.     "0.4","32","bad","high","low”
4.      "0.4","42","bad","high","high"
5.     "0.2","59","good","low","low”
6.      "0.6","109","good","low","high”
7.     "0.3","78","good","high","low”
8.      "0.4","205","good","high","high”
9.      "0.9","135",”NA","high","high"
10.    "0.2","176",”bad","high","high”

Your first assignment: Create a side-by-side boxplot (boxplot(x, ...)) and and histogram ((hist(x, ...)). 



#First I created data frame with 5 variables and 8 observation using the following function in RStudio


#The names of your variables are as follows: “Freq”,“bloodp”,“first”, ” second”, ”finaldecision”

#The rows

Frequency <- c(0.6,0.3,0.4,0.4,0.2,0.6,0.3,0.4,0.9,0.2)

BP <- c(103,87,32,42,59,109,78,205,135,176)

First <- c(1,1,1,1,0,0,0,0,NA,1)

Second <- c(0,0,1,1,0,0,1,1,1,1)

FinalDecision <- c(0,1,0,1,0,1,0,1,1,1)

pdf <- data.frame(Frequency,BP,First,Second,FinalDecision )

print(pdf)

library(tidyr)

#droping the missing values using tidyr oakage and drop_na function

pdf %>% drop_na(First)

#A histogram can be created in R with the hist function

hist(pdf$BP)

#A box plot can be created with the boxplot function.

boxplot(pdf)

 #I tried to show in histogram the frequency and the BP measurement from my data called "pdf" 
 

#on second graph I tried to indicates that I have created this simple boxplot blood pressures measurement comparing with the four other variables.






