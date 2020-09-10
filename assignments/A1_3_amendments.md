# Assignment 1.3 amendments

Some mistakes were found in A1.3, in the markdown description of the functions `extract_features` and `evaluate`.  These are the updated descriptions:

### Extract features

The preprocessed text can then be turned into feature vectors in some way, the final step before applying a machine learning algorithm to the training data.
You must implement the function `extract_features`, which takes two list of strings, a train split and a development/test split, and returns two numerical array-like objects representing the two data splits.

### Evaluate trained classifier

Implement the function `evaluate`, which takes as input a trained model, as well as a labeled dataset, and returns the following evaluated performance metrics: recall, precision, F$_1$, and accuracy.
