getdata
=======

Assignment:  
You should create one R script called run_analysis.R that does the following. 
1. Merges the training and the test sets to create one data set. 
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set 
4. Appropriately labels the data set with descriptive variable names. 
5. Creates a second, independent tidy data set with the average of each variable for each activity and
each subject.


This README file explains:
1.  How the raw data is processed to generate the tidy data sets
2.  How all of the scripts work and how they are connected

run_analysis.R
- performs creates the two required tidy datasets as described in the assignment
- runs sequentially two R scripts

getData1.R
- creates the required tidy data set from raw data
- requires raw data, unaltered data and unaltered file structure to be in same directory as script

1.  For training and test sets separately, convert y_train/y_test from activity label code to activity label text.  
2.  For training and test sets separately, extact mean and std columns from X_train/X_test files.  
3.  For training and test sets separately, join columns of subject_train (subject numbers), y_train (activity label), X_train (training set data - features).  
4.  Join rows of training and test dataframes to create the final tidy dataset.  
5.  Write the final tidy dataset to output files called output1.csv and output1.txt (two file formats of same data).  

getData2.R
-  Create a second dataframe of averages for each feature by subject and activity
-  requires tidy dataset to be in R with name of tidydf

1.  Computes the mean of each variable in tidydf for each activity and each subject
2.  Writes the means from #1 to output file (two file formats of same data): output2.csv and output2.txt



