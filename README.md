# KNN-using-zoo-dataset
This code reads in a dataset from a CSV file, performs k-fold cross-validation on a k-nearest neighbors classifier, and then does a grid search to find the optimal value of k.

The dataset used is called 'zoo.csv' and contains information about different animals such as their names, legs, wings, fins, etc. The goal is to predict the type of animal based on these features.

The code first imports the necessary libraries, including pandas for reading in the CSV file, numpy for numerical operations, and scikit-learn for machine learning functions.

Next, the CSV file is read into a pandas DataFrame object and displayed using the info() method to get a summary of the data.

Then, the features (columns) and target (type) are separated into two different variables, x and y, respectively.

A KFold object is created to split the data into 5 folds for cross-validation, and a k-nearest neighbors classifier is instantiated with n_neighbors=17. The cross_val_score() function is then used to calculate the accuracy of the model for each fold of the data, and the average accuracy is printed out.

After this, a grid search is performed to find the optimal value of k for the k-nearest neighbors algorithm. The possible values of k are set to be integers from 1 to 40, and the GridSearchCV function is used to perform a search over the parameter space. The best_score_ and best_params_ attributes of the resulting GridSearchCV object are printed out to show the optimal value of k and the corresponding accuracy.

Finally, a plot is created to show how the accuracy of the k-nearest neighbors classifier changes as the value of k is varied. The plot shows that the highest accuracy is obtained for a value of k close to 1, which suggests that a more complex model may be necessary to achieve high accuracy on this dataset. The best parameter value found by the grid search is also marked on the plot.
