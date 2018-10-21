# Week4 Course Project for Courser Course Getting and Cleaning Data
## Instructions
1. Makre sure you can run R command in your command line.
2. Clone the project to your local disk
3. In the cloned folder, run: Rscript run_analysis.R
4. During the script running process, the screen will print out the current progress.
5. Once the script finishes running, a new file tidy_data.txt will be generated in the current folder. This file contains the average of each variable for each activity and each subject.

## Script Explainations
1. All the data required for the script can be found in the 'UCI HAR Dataset' folder.
2. The script reads the activity labels and feature names from activity_labels.txt and features.txt files.
3. The test dataset is read from X_test.txt, while the test activity ids for each row in the test dataset is read from y_test.txt and the subject performing the activities for each row in the test dataset is read from subject_test.txt. The test data files are found in the test folder. After all three types of data are read, combine them into a single dataframe using cbind.
4. Read in the training dataset and its corresponding actvity ids and subjects by following the same steps used in reading the test data. Also use cbind to combine the training data into a single dataframe.
5. Merge the test and training data into a single dataframe using rbind.
6. Use the actvity and feature labels read from step 2 to change the column names of the dataframe resulting from step 4.
7. Use aggregate to group the dataframe by subject and actvity and calculate the mean for each measurement.
8. Write the result from step 7 to tidy_data.txt.
