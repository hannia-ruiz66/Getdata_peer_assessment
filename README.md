# Getdata_peer_assessment
Getting and cleaning data
This repository is for Getting and Cleaning Data course project. It has the instructions on how to run analysis on Human Activity recognition dataset.

Data set is: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Files:

a) run_analysis.R performs the data preparation and then followed by the 5 steps required as described in the course project’s definition:
1.- Merges the training and the test sets to create one data set.
2.- Extracts only the measurements on the mean and standard deviation for each measurement.
3.- Uses descriptive activity names to name the activities in the data set
4.- Appropriately labels the data set with descriptive variable names.
5.- From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

It downloads the UCI HAR Dataset data set and puts the zip file working directrory. After it is downloaded, it unzips the file into the UCI HAR Dataset folder.
It loads the train and test data sets and appends the two datasets into one data frame. This is done using rbind.
It extracts just the mean and standard deviation from the features data set. This is done using grep.
After cleaning the column names, these are applied to the x data frame.
After loading activities data set, it converts it to lower case using tolower and removes underscore using gsub. activity and subject column names are named for y and subj data sets, respectively.
The three data sets, x, y and subj, are merged. Then, it is exported as a txt file into the Project folder in the same working directory, named merged.txt.
The mean of activities and subjects are created into a separate tidy data set which is exported into the Project folder as txt file; this is named average.txt.
The R code contains str for easier preview of the two final data sets.

b) Tidydata.txt is the exported final data after going through all the sequences described above.

