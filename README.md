# getting-cleaningdata
I start this whole project right after downloading unzipped file from the Internet. Below is detailed explanation for each line of code:
line1: set working directory to a customized place
line2: unzip the file and load it into working directory
line3: read the subject data from the "train" files
line4: read the X data from the "train" files
line5: read the Y data from the "train" files
From my understanding: "subject" contains the number of volunteers on the experiment.
                       "X" contains detailed number of variables for each observation
                       "Y" contains the type of activity
line6: combine the data from "train" files by column bind
line7: read the subject data from the "test" files
line8: read the X data from the "test" files
line9: read the Y data from the "test" files
line10: combine the data from "test" files by column bind
line11: combine all the data from "train" and "test" by row bind
line12: read the feature Data into R, for header use in the following steps
line 13: select the feature containing "mean()" to select mean data, excluding meanFreq/AngleMean etc.
line14: select the feature containing "std" to select standard deviation data
line15: combine mean and standard deviation (including either mean/std)
line16: add 2 columns (for subject and activity), and data into logical vector
line17: select Data with mean and standard deviation feature
line18: read activity file into R
line19: rename one column of total data, for future merge use
line20&21: rename the activity lists, for future merge use
line22: merge data and activity to show more clearly which activity is performed
line23&25%26: select mean and std variables among features, and change into character
line24&30&31&32 get rid of repeated/useless columns
line27: change column name into feature characters
line28: change colume name 
line29: aggregate all the data, by subject and activity, and than calculate mean for remaining variables
line33: write table to txt file
