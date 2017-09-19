# NYC Taxi Tips Prediction
> by Weiye Deng

## Introduction

This report aims to build a quantitative model to predict the percentage of tip to be paid by each customer after a taxi trip. The dataset, Nov 2015 NYC Green Taxi, is publicly available on NYC Taxi & Limousine Commission’s official website. Data cleaning, feature engineering and data partitioning procedures were performed before the model is constructed. The least absolute shrinkage and selection operator (LASSO) and linear regression were applied during the modeling process. A random forest classification model is introduced to turn the prediction problem into a classification problem due to the poor fitness on the linear regression model. The original data need to be re-partitioned. Cross validation and accuracy testing processes on the random forest classification model are demonstrated.  Finally, further consideration and enhancement possibilities are proposed at the end of this report.

## Environment Setup

**1. Install R and RStudio:** <br />
If R and Rstudio are not installed, please install them before the code is run. Please refer to this [setup instruction]( 
	https://courses.edx.org/courses/UTAustinX/UT.7.01x/3T2014/56c5437b88fa43cf828bff5371c6a924/) or type the below command to terminal:
```
sudo apt-get install r-base
```

**2. Install Spark:** <br />
Open RStudio, type in the following code in the RStudio Console:
```r
install.packages("sparklyr")
library(sparklyr)
spark_install(version = "1.6.2")
```

**3. Install the required packages** <br />
```r
install.packages('ggplot2')
install.packages('readr')
install.packages('rgeos')
install.packages('sp')
install.packages('rgdal')
install.packages('lubridate')
install.packages('utils')
install.packages('googleVis')
install.packages('chron')
install.packages('glmnet')
install.packages('sparklyr')
install.packages('dplyr')
install.packages('ggmap')
install.packages('reshape2')
install.packages('caret')
```

**4. Set the working directory to folder, Data_File, using command** 
```r 
setwd()```
