---
Course: CSCC 45
Year Level: 3rd
Semester: 2nd
---
---

## K-Nearest Neighbor (KNN)
---
- simple, non-parametric, and instance based learning algorithm
- "K" is a variable, for the nearest points

### Supervise Learning Algorithm
---
- Commonly used for classification tasks, can also be applied to regression
- Classifies a data point based on how its neighbors are classified. This is the idea

### How KNN Works
---
1. **Training Phase**
	- does not have explicit training phase, stores the entire dataset. "Learning" happens during the prediction phase.
	- hyperparameter - a parameter that identifies the best model; for KNN the hyperparameters are k, distance, and dataset quality.
2. **Choosing k**
	- k represents number of nearest neighbors, for prediction. Choosing the right value for k:
		- overfitting, small k makes the model sensitive to noise
		- underfitting, large k smooths out the decision boundary
		- choose the middle value for k
3. **Distance Measurement**
	- to find the nearest neighbors, the algo calculates the distance between the query point and all other points in the training dataset:
		- Euclidean Distance
		- Manhattan Distance
		- Minkowski Distance
4. **Making Predictions:**
	- for classification task:
		- identify the k
		- count the class labels among k

**Implementation Steps:**
5. Load the data set
6. Select k: cross-validation or domain knowledge
7. calculate distances: do for each query
8. find the nearest neighbors
9. vote or average: for classification, vote for majority; for regression, calculate the average

**Advantages of KNN**
- Simplicity - easy to implement and understand
- No Training Phase
- Versatility - classification and regression

**Disadvantages of KNN**
- Computationally Intensive - large datasets is costly in computing distances
- Sensitive to Irrelevant Features - 
- Curse of Dimensionality - 