# Getting-and-Cleaning-Data-Project
Prepare tidy data 

# Script design

Step 1. Merges the training and the test sets into one dataset
* Get data from the list of features’ name in ”features.txt”
* Attributes label to “X_train”,“subject_train”,“ y_train”
* Combine“X_train”,“subject_train”,“ y_train”to"train_set”
* Attributes label to ”X_test”,“subject_test”,“ y_test”
* Combine”X_test”,“subject_test”,“ y_test”to"test_set”
* Combine “train_set”and”test_set”to”data_set”

Step 2. Extract the measurements on the mean and deviation 
* Find target strings that include ”-mean” and “-std”
* Subset target dataset 
* Combine the “subject” and “activity” in one subset 

Step 3. Name the activities in the data set 
Master$activities <- as.character(Master$activities)
Master$activities[Master$activities == 1] <- "Walking"
Master$activities[Master$activities == 2] <- "Walking Upstairs"
Master$activities[Master$activities == 3] <- "Walking Downstairs"
Master$activities[Master$activities == 4] <- "Sitting"
Master$activities[Master$activities == 5] <- "Standing"
Master$activities[Master$activities == 6] <- "Laying"
Master$activities <- as.factor(Master$activities)

Step 4. Label the descriptive variable names
* Extract the old names of variables from the merged data set
* Use regular expressions and “sub()” function to update the names to more  descriptive ones
* Replace the variables’ names with the updated vector of names in the merged data set

Step 5. Creates a tidy data set 
* Fix the rows to show mean values 
* rename the data
write the latest data set using write.talbe()




