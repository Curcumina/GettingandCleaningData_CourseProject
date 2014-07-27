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
Variable information
mean(): Mean value of attributes mentioned in features_info.txt
std(): Standard deviation of attributes mentioned in features_info.txt
tBodyAcc-X: (Body Acceleration Signal in X orientation)
tBodyAcc-Y: (Body Acceleration Signal in Y orientation)
tBodyAcc-Z: (Body Acceleration Signal in Z orientation)
tGravityAcc-X: (Gravitational Acceleration Signal in X orientation)
tGravityAcc-Y: (Gravitational Acceleration Signal in Y orientation)
tGravityAcc-Z: (Gravitational Acceleration Signal in X orientation)
tBodyAccJerk-X: (body linear acceleration in X orientation)
tBodyAccJerk-Y: (body linear acceleration in Y orientation)
tBodyAccJerk-Z: (body linear acceleration in Z orientation)
tBodyGyroJerk-X: (angular velocity in time to obtain X orientation Jerk signals )
tBodyGyroJerk-Y: (angular velocity in time to obtain Y orientation Jerk signals )
tBodyGyroJerk-Z: (angular velocity in time to obtain Z orientation Jerk signals )
fBodyAcc-X: (fourier transformation of body acceleration in X direction)
fBodyAcc-Y: (fourier transformation of body acceleration in Y direction)
fBodyAcc-Z: (fourier transformation of body acceleration in Z direction)
fBodyAccJerk-X: (fourier transformation of body linear acceleration in X direction)
fBodyAccJerk-Y: (fourier transformation of body linear acceleration in Y direction)
fBodyAccJerk-Z: (fourier transformation of body linear acceleration in Z direction)
fBodyGyro-X: (angular velocity fourier transformation to obtain X orientation Jerk signals)
fBodyGyro-Y: (angular velocity fourier transformation to obtain Y orientation Jerk signals)
fBodyGyro-Z: (angular velocity fourier transformation to obtain Z orientation Jerk signals)
fBodyAccJerkMag: (fourier transformation of body acceleration magnitude)
fBodyGyroMag: (angular velocity fourier transformation Jerk signals magnitude)
fBodyGyroJerkMag: (angular velocity fourier transformation Jerk signals magnitude)

