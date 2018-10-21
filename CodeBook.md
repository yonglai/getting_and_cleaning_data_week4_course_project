# Getting and Ceaning Data --- Week4 Course Project Code Book
## Script Explanations
1. All the data required for the script can be found in the 'UCI HAR Dataset' folder.
2. The script reads the activity labels and feature names from activity_labels.txt and features.txt files.
3. The test dataset is read from X_test.txt, while the test activity ids for each row in the test dataset is read from y_test.txt and the subject performing the activities for each row in the test dataset is read from subject_test.txt. The test data files are found in the test folder. After all three types of data are read, combine them into a single dataframe using cbind.
4. Read in the training dataset and its corresponding actvity ids and subjects by following the same steps used in reading the test data. Also use cbind to combine the training data into a single dataframe.
5. Merge the test and training data into a single dataframe using rbind.
6. Use the actvity and feature labels read from step 2 to change the column names of the dataframe resulting from step 4.
7. Use aggregate to group the dataframe by subject and actvity and calculate the mean for each measurement.
8. Write the result from step 7 to tidy_data.txt.
## Tidy data variables
1. The first column is the id of the subject the performed the corresponding activity.
2. The second column is a descriptive name of the activity for the current row of data.
3. The rest columns are mean and standard deviations of different measurements.
