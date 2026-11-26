MACHINE LEARNING

1. Data Analysis
   Category: Exploratory Data Analysis (EDA)

Data analysis is the process of inspecting and understanding a dataset
before applying machine learning algorithms. It helps identify patterns,
relationships, missing values, unusual observations, and possible
data-quality issues.

Typical activities:
Load the dataset and inspect its dimensions.
Examine column names, data types, and summary statistics.
Identify missing values and duplicate records.
Analyse numerical and categorical features.
Study distributions and relationships between variables.
Visualise the data using suitable plots.

Common visualisations: Histograms, box plots, bar charts, scatter
plots, and correlation heatmaps.

Purpose: To understand the dataset and decide which preprocessing
steps and modelling techniques may be appropriate.


2. Single Variable Linear Regression
   Category: Supervised Learning --- Regression

Simple linear regression models the relationship between one independent
variable (input) and one dependent variable (target). It fits a straight
line that minimises the sum of squared differences between actual and
predicted values.

Equation:
h(x)=Qo +Q1x

Where: - (x): input feature
h(x): predicted output
(Q_0): intercept 
(Q_1): slope or coefficient


3. Multiple Variable Linear Regression
Category: Supervised Learning --- Regression

Multiple linear regression extends simple linear regression by using two
or more independent variables to predict a continuous target.
Equation:
h(x)=Qo +Q1x1+Q2X2+...+QnXn


4. Polynomial Regression
Category: Supervised Learning --- Regression

Polynomial regression models non-linear relationships by adding powers
of the input features.
Equation:
h(x)=Qo +Q1x1+Q2X2+Q3X3+Q4X1X2+...+QnXn

What to observe: Increasing the polynomial degree makes more complex
curves possible. However, an excessively high degree can overfit the
training data and perform poorly on unseen data.


5. K-Nearest Neighbors (KNN)
Category: Supervised Learning --- Classification or Regression

KNN predicts the output for a new observation by finding the (k) closest
training observations. It is a distance-based algorithm.

How it works: 
1. Store the labelled training observations. 
2. Choose a value of (k).
3. Calculate the distance between the new observation
and training observations. 
4. Select the (k) nearest neighbours. 
5. For classification, use majority voting. For regression, commonly use the
mean of the neighbours' target values.

Important parameter: n_neighbors ((k)).

What to observe: A small (k) can make the model sensitive to noise(overfit),
while a large (k) can smooth the decision boundary too much. Feature
scaling is generally important because KNN relies on distances.


6. K-Means Clustering
Category:Unsupervised Learning --- Clustering

K-Means divides observations into a specified number of clusters. Each
observation is assigned to the cluster whose centroid is nearest to it.

How it works:
1. Choose the number of clusters, (K).
2. Initialise (K) centroids. 
3. Assign each observation to its nearest centroid.
4. Recalculate each centroid as the mean of the observations assigned to it. 
5. Repeat assignment and centroid updates until convergence or the
iteration limit is reached.

Objective: Minimise the within-cluster sum of squared distances:

What to observe: The choice of (K), and initial
centroid positions can affect the final clusters. The elbow method can help assess clustering choices.


7. Hierarchical Clustering
Category: Unsupervised Learning --- Clustering

Hierarchical clustering builds a hierarchy of clusters. In
hierarchical clustering, every observation initially forms its own
cluster, and clusters are repeatedly merged according to a distance and
linkage rule.

How it works:
1. Start with each observation as an individual cluster.
2. Calculate distances between clusters.
3. Merge the two closest clusters according to the selected linkage criterion.
4. Repeat until the desired number of clusters or a stopping condition is reached. 
5. Visualise the hierarchy using a dendrogram when applicable.


8. DBSCAN

Category: Unsupervised Learning --- Density-Based Clustering

DBSCAN (Density-Based Spatial Clustering of Applications with Noise)
groups together observations in dense regions and identifies
observations in low-density regions as noise or outliers.

Important parameters: 
eps: Maximum neighbourhood distance used to identify nearby observations.
min_samples: Minimum number of observations in an eps neighbourhood for a point to qualify as a core
point.

Types of points:
Core point: Has at least `min_samples` observations in its neighbourhood, including itself in the common
implementation convention. 
Border point:Is near a core point but does not itself have enough neighbours to be a core point.
Noise point: Neither od the above

How it works:
1. Select an unvisited observation. 
2. Find its neighbours within distance `eps`.
3. If it has enough neighbours, start or expand a cluster.
4. Continue expanding through density-reachable
core points. 
5. Mark observations that do not belong to any cluster as
noise.

What to observe: DBSCAN does not require the number of clusters in
advance and can identify irregularly shaped clusters. Its performance
depends strongly on eps, min_sample, and feature
scaling. It may struggle when clusters have very different densities.


9. Support Vector Machine (SVM)
Category:Supervised Learning --- Classification or Regression

A Support Vector Machine learns a decision boundary that separates
classes. For classification, it aims to find a hyperplane with the
largest possible margin between the classes.

Key concepts:
Hyperplane: The decision boundary separating classes.
Support vectors: Training observations closest to the decision boundary. 
Margin: Distance between the decision boundary and the nearest observations from the classes.
Kernel: A function that enables the model to represent non-linear decision boundaries.


10. Decision Tree and Random Forest
Category: Supervised Learning --- Classification or Regression
Decision Tree

A Decision Tree makes predictions using a sequence of feature-based
decisions. It repeatedly splits the data into smaller groups, aiming to
make the resulting groups more homogeneous with respect to the target.

What to observe: Deep trees can fit training data very closely but
may overfit. Limiting depth or increasing minimum samples per split/leaf
can make a tree simpler.

Random Forest
Random Forest is an ensemble learning method that combines predictions
from multiple decision trees. Each tree is trained using a randomised
sample of the training data and, at each split, a random subset of
features is considered.

How it works: 
1. Create multiple bootstrap samples from the training
data (when bootstrap sampling is enabled).
2. Train a decision tree on each sample, using feature randomness. 
3. Collect predictions from all trees. 
4. For classification, combine predictions using majority voting;
for regression, average the predictions.

What to observe: Increasing the number of trees can make predictions
more stable, but also increases computation.


11. Kernel-Based Image Processing

Category: Digital Image Processing --- Spatial Filtering

Kernel-based image processing applies a small matrix, called a kernel or
filter, to an image. The kernel is moved across the image, and each
output pixel is calculated from a weighted combination of neighbouring
pixels.

How it works:
1. Load an image.
2. Represent the filter as a matrix of weights.
3. Move the kernel across the image.
4. Multiply the kernel values by the corresponding image neighbourhood values.
5. Sum the products to calculate the output pixel. 
6. Handle image boundaries using an appropriate padding strategy.


12. Convolutional Neural Network (CNN)
Category: Deep Learning --- Image Processing and Computer Vision


13. Principal Component Analysis (PCA)

Category: Unsupervised Learning --- Dimensionality Reduction

PCA transforms a dataset with potentially many correlated features into
a smaller set of new, uncorrelated variables called principal
components.