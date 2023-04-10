# DG_WK6

For this assignment, I used data that I found from an open Kaggle database (https://www.kaggle.com/datasets/kaggle/meta-kaggle?select=UserAchievements.csv).
It contained 11 features and 52132908 occurences. The original file was 3.37 GB in .csv format. I used the jupyter notebook shell on Kaggle to open and work with the data.

I tried multiple read methods and measured their execution times using:

import time
startTime = time.time()
executionTime = (time.time() - startTime)

I read the data using Pandas, Datatables, Dask, PySpark, Polars, and Vaex. Their respective read times are recorded in 'time.txt'.

I chose to move forward with Pyspark, as it performed the best. And then I followed the sample schema and validation process, making changes for the use of pyspark instead of pandas. The pyspark dataframe was then read into a .csv file and compressed with gzip.

This repository contains the two jupyter notebooks (one for checking the reading methods, and one for processing and validating the schema), as well as the compressed data files (which were broken into 30 parts).
