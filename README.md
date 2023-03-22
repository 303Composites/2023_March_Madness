# March-Madness-ML

Applying machine learning to March Madness: Credit to this repo was initially adapted from [here](https://github.com/adeshpande3/March-Madness-2017) and the orginal [blog post](https://adeshpande3.github.io/adeshpande3.github.io/Applying-Machine-Learning-to-March-Madness) without this initial start this project would have taken ages so thank you adeshpande3. 
This has been updated to include additional models and stats categories as well as additional data for the 2023 season. 

## Overview

* Data: The Data folder contains different CSVs that show team stats, regular season game results, etc. It will contain data that I've scraped, data from Kaggle, and a folder that contains precomputed xTrain and yTrain matrices so that we don't have to keep recomputing the training set. 
This will need to be updated year to year and can be used to make changes to the model.

## Requirements and Installation

* python 3
* [pipenv](https://pipenv.readthedocs.io/en/latest/) for managing virtualenv and pip package dependencies.

## What To Do Every March
* Download data files from [Kaggle](https://www.kaggle.com/c/mens-machine-learning-competition-2023), who will normally have a competition going (look for the competition for the current year). They will provide CSV files that show the results from games since 1985, information on conferences, tourney seed history, etc. It's important to download this data every year because Kaggle will add data from the most recently completed season and so you'll have a bit more training data. Replace the files as needed for the season in the correct file structure.
* We also want to get the advanced rating statistics from Basketball Reference. Basically, go to https://www.sports-reference.com/cbb/seasons/2023-ratings.html, replace 2023 with whatever year you're looking at, choose to get the table as a CSV (available in one of the dropdowns), disregard the first line, start with the line that begins with "Rk,School..", copy that over to a new text doc in Sublime (or any text editor), save it as a CSV, and then upload it to [this folder](https://github.com/adeshpande3/March-Madness-ML/tree/master/Data/RatingStats).
* If you get an error with the data or results where all the probabilities are the same check the CSV files for invalid characters, Sublime is helpful for this as it will show errors like <0xA0> that wont load properly in the csv file. 
* We also want to get the regular season statistics from Basketball Reference. Basically, go to https://www.sports-reference.com/cbb/seasons/2023-school-stats.html, replace 2023 with whatever year you're looking at, choose to get the table as a CSV (available in one of the dropdowns), disregard the first line, start with the line that begins with "Rk,School..", copy that over to a new text doc in Sublime (or any text editor),
* For both of the above steps, make sure that the column names are the same from year to year! In 2023, Basketball Reference made some small changes to the column names (X3P to 3PA for example)
* 2020 regular season data is included but no tourney data is used due to the Pandemic. Jupyter will give a runtime error for this but will still complete the 2020 training set.


## Other things to add
* Modify the machine models 
* Perform data visualizations to see which features are the most important
* Decide what type of additional data preprocessing might be needed
 

