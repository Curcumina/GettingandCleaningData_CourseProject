##CodeBook.md
This file explains different steps of the script used for loading and analyzing data
========================================================

#CodeBook for run_analysis.R
The "run_analysis.R" script follows the following steps:
1.    It will loads the zipped data files from the (http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) link and put it in a directory named "HAR" (if required, it will create the directory). Then unzips the zip file.
2.    First, read the features and filter only the features that contain "mean()" and "std()".
3.	It will then load all train and test data with only filtered features. It will use negative widths in "read.fwf" to skip the columns that are not required. That makes it much faster to load and process.
4.	The subject files will merge to main data and then merges all train as well as test data using rbind() function. That results in a dataframe named "all_data", and label the columns by the name of the features.
5.	Another dataframe named "all_average" is created that contains the mean of all columns by "subject” using "aggregate" function as described in the run_analysis.R script.
6.	Finally both dataframes were exported to working directory as a CSV files.