Codebook 

This document describes the run_analysis.R file. 

For the project we were asked to: Create one R script called run_analysis.R that does the following:
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The following goes through how I did this.

- install the required packages: reshape2 & data.table
- download the file from: 
	https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
- I then copied the file into my documents and set it as the working directory as I couldn't get it to load from the temp file
- Starting with the test data: loaded the activity labels, features names and created a function that calculated the mean & standard deviation of the features
	- then load all the test data (x, y & subject test)
	- use the previously created function to extract the mean and standard deviation measurements for each variable
	- load the activity labels 
	- bind the test data together

- Do the same for the training data: 
	- then load all the test data (x, y & subject test)
	- use the previously created function to extract the mean and standard deviation measurements for each variable
	- load the activity labels 
	- bind the test data together
-Merge the test and training data together
	- add the labels
-Apply mean function to dataset using dcast function to re-write the data table to tidy_data
