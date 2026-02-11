# KNN and Radius Neighbors Classifier Lab

## Purpose of the Lab

The purpose of this lab was to explore and compare the performance of the K-Nearest Neighbors (KNN) and Radius Neighbors (RNN) classification algorithms using the Wine dataset from the sklearn library. The goal was to understand how different parameter values (k for KNN and radius for RNN) affect model accuracy and to identify which configurations provide the best results.

## Key Insights and Observations

* The accuracy of the KNN model varied depending on the value of k.
* Smaller k values tended to be more sensitive to noise, while larger k values provided more stable predictions.
* There was an optimal range of k where the model achieved its highest accuracy.
* The RNN model’s accuracy depended on the selected radius value.
* Smaller radii sometimes resulted in fewer neighbors and less stable predictions, while larger radii included more data points and produced more consistent results.
* Overall, KNN showed more stable performance across parameter values, while RNN performance was more sensitive to the chosen radius.

## Challenges and Decisions

* One challenge was selecting appropriate parameter values for both k and radius without prior knowledge of the dataset’s scale.
* The radius values required experimentation because too small a radius could lead to outliers with no neighbors.
* To address this, the `outlier_label='most_frequent'` option was used in the RNN classifier to handle cases where no neighbors were found.
* A stratified train-test split was used to ensure that class distributions remained balanced between training and testing sets.

Overall, the lab demonstrated how parameter tuning directly impacts the performance of distance-based classification algorithms.