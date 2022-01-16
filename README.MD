
**Source of the data sets (websites/fields):**

* imdb.com
* amazon.com
* yelp.com

It contains sentences labelled with positive(1) or negative(0) sentiment, extracted from reviews of products, movies, and restaurants.

For each website, there exist 500 positive and 500 negative sentences. Those were selected randomly for larger datasets of reviews. 
We attempted to select sentences that have a clearly positive or negative connotation, the goal was for no neutral sentences to be selected.

**Data Format:**

sentence \t score \n


**Details:**

Score is either 1 (for positive) or 0 (for negative)	

**Code Execution Process:** 

The entire solution is developed in jupyter notebook.

The ipynb file is kept in a directory and there is a sub-directory called 'pp1data' which contains all the 3 text input data files.

The jupyter notebook contains two(2) sections

* **Part 1) Experiment 1 :** For each of the 3 datasets run stratified cross validation to generate learning curves for Naive Bayes with m = 0 and with m = 1. For each dataset, plots of averages of the accuracy and standard deviations (as error bars) as a function of train set size. 

* **Part 2) Experiment 2 :** Run stratified cross validation for Naive Bayes with smoothing parameter m = 0, 0.1, 0.2. . . 0.9 and 1, 2, 3. . . 10 (i.e., 20 values overall). Plot the cross validation accuracy and standard deviations as a function of the smoothing parameter(m).

In each of the section, the complete program is written in a single cell with main() function and other user defined functions. The main() function takes the input selection from user as it prompts to give a data set selection option.

All the text input files automatically get detected in the 'pp1data' directory and asks the user to chose which dataset to execute.

**Input:**

* Enter 1 for amazon_cells_labelled.txt
* Enter 2 for yelp_labelled.txt
* Enter 3 for imdb_labelled.txt

The user selects either of 1/2/3 as per their choice of data set and the program proceeds with the selected data set to read it from the directory 'pp1data' and process for the given experiments.

**Output:**

For Experiment 1 - 
* list of average accuracy per training set size in K folds for smoothing parameter m =0 and m = 1
* list of standard deviation per training set size in K folds for both m =0 and m=1
* plot of averages of the accuracy (as error bars) as a function of train set size
* plot of standard deviations (as error bars) as a function of train set size

For Experiment 2 - 
* list of average accuracy for 20 smoothing parameter from m =0, 0.1, 0.2....0.9 and 1, 2...9
* list of standard deviation for 20 smoothing parameter from m =0, 0.1, 0.2....0.9 and 1, 2...9
* plot of the cross validation accuracy as a function of the smoothing parameter(m)
* plot of standard deviations (as error bars) as a function of the smoothing parameter(m)


