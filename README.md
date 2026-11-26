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

How it works: 1. Store the labelled training observations. 2. Choose
a value of (k). 3. Calculate the distance between the new observation
and training observations. 4. Select the (k) nearest neighbours. 5. For
classification, use majority voting. For regression, commonly use the
mean of the neighbours' target values.

Common distance measure --- Euclidean distance:

\(d(p,q) = `\sqrt{\sum_{i=1}^{n}(p_i-q_i)^2}`{=tex}\)

Important parameter: n_neighbors ((k)).

What to observe: A small (k) can make the model sensitive to noise,
while a large (k) can smooth the decision boundary too much. Feature
scaling is generally important because KNN relies on distances
