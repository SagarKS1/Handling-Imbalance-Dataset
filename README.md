# Handling-Imbalance-Dataset using Under sampling and over sampling techniques


Today any machine learning practitioner working with binary classification problems must have come across this typical situation of an imbalanced dataset. This is a typical scenario seen across many valid business problems like fraud detection, spam filtering, rare disease discovery, hardware fault detection, etc. Class imbalance is a scenario that arises when we have unequal distribution of class in a dataset

Under sampling technique

NearMiss : 

The algorithm first calculates the distance between all the points in the larger class with the points in the smaller class. This can make the process of undersampling easier. 
Select instances of the larger class that have the shortest distance with the smaller class. These n classes need to be stored for elimination. 
If there are m instances of the smaller class then the algorithm will return m*n instances of the larger class. 

Over sampling technique

SMOTE : Synthetic Minority Oversampling Technique

At first the total no. of oversampling observations, N is set up. Generally, it is selected such that the binary class distribution is 1:1. But that could be tuned down based on need. Then the iteration starts by first selecting a positive class instance at random. Next, the KNN’s (by default 5) for that instance is obtained. At last, N of these K instances is chosen to interpolate new synthetic instances. To do that, using any distance metric the difference in distance between the feature vector and its neighbors is calculated. Now, this difference is multiplied by any random value in (0,1] and is added to the previous feature vector. 

Over and under sampling technique

SMOTETomek link:

SMOTE+TOMEK is such a hybrid technique that aims to clean overlapping data points for each of the classes distributed in sample space. After the oversampling is done by SMOTE, the class clusters may be invading each other’s space. As a result, the classifier model will be overfitting. Now, Tomek links are the opposite class paired samples that are the closest neighbors to each other. Therefore the majority of class observations from these links are removed as it is believed to increase the class separation near the decision boundaries. Now, to get better class clusters, Tomek links are applied to oversampled minority class samples done by SMOTE

