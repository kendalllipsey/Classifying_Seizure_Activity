To improve the medical response and treatment of seizures, and ultimately improve people’s lives affected by seizures, diagnosis of seizures must be improved. 
# Goal
To goal for this project was to improve the classification of seizures based off of brain wave activity. 
## Exploratory Data Analysis
To do this, we started with Data processing and Data exploration to fully understand the data provided. 
## Algorithms 
We then performed a logistic regression with varying hyperparameters. 
Next we executed K Nearest Neighbors with different distance metrics. 
We then performed Decision Trees and Random Forests with pruning techniques. 
Finally, we executed a convolutional neural network and evaluated our algorithms. 

### Data Source
https://archive.ics.uci.edu/ml/datasets/EEG+Database

Our data comes from the university of california irvine machine learning repository. The UCI Machine Learning Repository is a collection of databases, domain theories, and data generators that are used by the machine learning community for the empirical analysis of machine learning algorithms.
Our dataset consists of  EEG readings from 500 patients. 20%, or 100 patients, had confirmed seizures while the other 400 did not. Each patient has 23 seconds of brain activity recorded, with each second consisting of 178 points.


# Conclusions

### Logistic Regression and K-Nearest Neighbors
For the simpler models employed such as Logistic Regression and K-Nearest Neighbors), the accuracy resulted in around 88%.
 At first glance this looks like a promising baseline, however a further investigation shows that non-seizure activity accounted for 80% of the data. 
Therefore, if you predicted everything was non seizure activity you would result in 80% accuracy. 

A more nuanced look requires looking deeper. 
When looking at the confusion matrix for the K-Nearest neighbors (Euclidean Distance), 56.5% of seizure activity was put into non-seizure activity. 
This shows that our variable of interest which is correctly classifying seizure activity, performed  quite poorly. 

### Decision Trees and Random Forests
Moving to more complex algorithms  such as Decision Trees and Random Forests, we begin to see a shift in the classification accuracy moving away from false negatives. 
The Random Forest predicted 82.6% of seizure activity correctly. This indicates more complex trends exist that aren’t necessarily detectable by simpler algorithms.
### Convolutional Nueral Network 
Our most complex algorithm, the Convolutional Neural Network, performed best with an accuracy of 99%. 
However, this increase in accuracy came at the expense of increased computational time. 
The overall runtime of the neural net with 10 epochs was 1 hour and 48 minutes. However, the accuracy leveled off at only 3 epochs. 
Therefore, to obtain the same level accuracy, this neural could be run in just over 30 minutes. 
