# DataVine Analytics — Prototype Modeling

## Project Overview

This project prototypes three data-science solutions for different client use cases:

1. **Wine Classification** — classify wine cultivars from chemical measurements.
2. **Feed Recommendation** — recommend similar feed types based on chick growth outcomes.
3. **Crime Pattern Clustering** — identify regional patterns in crime statistics.

Each use case follows a structured workflow of data preparation, dimensionality reduction, model development, evaluation, and interpretation.

---

## 1. Wine Classification

A k-Nearest Neighbors (k-NN) classifier was developed to classify wines into three cultivars.

### Approach

* Standardized numerical features
* Applied PCA while retaining 95% of variance
* Used `GridSearchCV` to tune k-NN hyperparameters
* Evaluated performance on a held-out test set

### Result

The tuned model achieved:

* **Cross-validation accuracy:** 97.91%
* **Test accuracy:** 100%
* **PCA components retained:** 10 of 13

---

## 2. Feed Recommendation

A recommendation approach was developed using the `chickwts` dataset to identify feed types with similar performance characteristics.

The analysis:

* Aggregated average chick weight and coefficient of variation by feed type
* Standardized the resulting profiles
* Used PCA to create a performance score
* Calculated cosine similarity between feed types

The approach produced meaningful similarity relationships between feed types, providing a simple framework for recommending alternatives based on historical outcomes.

---

## 3. Crime Pattern Clustering

The `USArrests` dataset was used to identify natural groupings of U.S. states based on crime statistics.

### Approach

* Standardized the crime variables
* Selected Murder, Assault, and Rape as the primary clustering features
* Applied PCA for dimensionality reduction and visualization
* Used the elbow method to determine the K-Means cluster count
* Used BIC to determine the optimal number of GMM components
* Compared K-Means and Gaussian Mixture Model results

Both methods selected **2 clusters**, revealing distinct regional crime profiles.

---

## Technologies

**Python | Pandas | NumPy | Scikit-learn | Matplotlib**

### Techniques

k-NN • PCA • GridSearchCV • Cosine Similarity • K-Means • Gaussian Mixture Models • Clustering • Dimensionality Reduction
