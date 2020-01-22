# Datacleaning
repo created for data cleaning quiz


## This ReadMe.md file describes :-
- assumptions used in the analysis
- how the run_analysis.r script works
- the variables, the data, and any transformations performed to clean up the data

## Purpose

The main purpose of this project is to demonstrate my ability to collect, clean and work with a dataset. I have tried to create a dataset that can be used at a later date to do some analysis.
This dataset is the data collected from the users who were wearing Samsung SII on their waists. More information is available here:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones


## Assumptions

01. The data files required for this are at :
"https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
02. I assume the original data files have been downloaded & extracted locally in appropriate
folders
03. The raw data files are NOT included in this analysis.
04. Variable Selection Criteria
The raw sensor data fetaures are being extracted by the application of a set of signal
filters. The features are chosen because they are assumed to have significance to the
activity labelling problem.
05. Variable & File names, data folder structure remain the same.


## Raw data Description

The data comes from the Human Activity Recognition Using Smartphones Experiment.
The obtained dataset was randomly partitioned into two sets, where70% of the volunteers was
selected for generating the training data and 30% the test data.

Gyroscope is a device for measuring or maintaining orientation, based on the
principles of angular momentum & allows accurate recognition of movement within a 3D space
In contrast, an accelerometer is a compact device designed to measure non-gravitational
acceleration.


### UCI HAR Dataset Description
The dataset includes the following files:-
- 'README.txt'
- 'features_info.txt': Shows information about the variables used on the feature vector
- 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.


### Variable Description
For each participant, there are several things being measured along the XYZ axes,
- Angular Velocity, Acceleration, Maginutude, Angle along with some derived values,
e.g. Jerk is derived from Acceleration and Angular Velocity
- tBodyAcc-XYZ | tGravityAcc-XYZ | tBodyAccJerk-XYZ | tBodyGyro-XYZ
- tBodyGyroJerk-XYZ | tBodyAccMag | tGravityAccMag | tBodyAccJerkMag
- tBodyGyroMag | tBodyGyroJerkMag | fBodyAcc-XYZ | fBodyAccJerk-XYZ
- fBodyGyro-XYZ | fBodyAccMag | fBodyAccJerkMag
- fBodyGyroMag | fBodyGyroJerkMag |
- Using, the Euclidean norm, the magnitude of the inputs listed above were calculated
- The variable have a time (prefix t) and frequency (prefix f) domain component.
- Variables are normalized and bounded within [-1,1]
- These signals were used to estimate statistical variables [mean, std deviation, min, max
,skew, kurtosis etc.] for each of the feature vector pattern: '-XYZ' is used to denote 3
axial signals in the X, Y and Z directions.
- A listing of the statistical variables created is described under the file "FeatureInfo"
- A complete list of the 561 variables is available in the file "Features.txt"
As stated in the assumptions above, as part of the project, only mean() & stddev() estimates
are included in the analysis.

## run_analysis.R

The script "run_analysis.R" contains the sequence proposed for the project, consisting of:

- Merging the training and the test sets to create one data set;
- Extracting the measurements on the mean and standard deviation for each measurement. That is, mean and standard deviation for the following: tBodyAcc-XYZ tGravityAcc-XYZ tBodyAccJerk-XYZ tBodyGyro-XYZ tBodyGyroJerk-XYZ tBodyAccMag tGravityAccMag tBodyAccJerkMag tBodyGyroMag tBodyGyroJerkMag fBodyAcc-XYZ fBodyAccJerk-XYZ fBodyGyro-XYZ fBodyAccMag fBodyAccJerkMag fBodyGyroMag fBodyGyroJerkMag
- Using descriptive activity names to name the activities in the data set.
- Appropriately labeling the data set with descriptive variable names.
- From the data set in step above, creating an independent tidy data set with the average of each variable for each activity.


### Codebook

CodeBook.md - This code book describes the variables, data, process I followed in order to create the R script.
