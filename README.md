<h2 align="center"> K Nearest Neighbors </h2>

<p align="center">
  <img src="https://miro.medium.com/max/1080/0*49s1xDlDKDsn55xa.gif" height=55% width=55% />
</p>

K-Nearest Neighbors (KNN) is a **supervised machine learning 🤖 algorithm** that can be used for either **regression** or **classification** tasks. It is **non-parametric**, which means that the algorithm does not make assumptions about the underlying distributions of the data. This algorithm is based on **Feature Similarity**. This is in contrast to a technique like linear regression, which is parametric, and requires us to find a function that describes the relationship between dependent and independent variables.

<h2> 🛣️ Minkowski Distance</h2>

The distance between points is determined by using a generalized formula, known as Minkowski distance, i.e., represented as follows:

<p align="center">
<img src="https://miro.medium.com/max/1000/1*nxGbicBE1MSV4LbBFueJvg.png" height=35% width=35% style="text-align:center;">
</p>

> *where X and Y are data points, n is the number of dimensions, and p is the Minkowski power parameter.* <br><br>
> When **p=1**, the distance is known at the **Manhattan (or Taxicab) distance**, and when **p=2** the distance is known as the **Euclidean distance**. 

<h2> 📖 Libraries Used </h2>
numpy, pandas, collections, sklearn, matplotlib.pyplot

<h2> 📚 Data Set </h2>
To test the KNN classifier, I have uses the iris data set from sklearn.datasets. The data set has measurements (Sepal Length, Sepal Width, Petal Length, Petal Width) for 150 iris plants, split evenly among three species (0 = setosa, 1 = versicolor, and 2 = virginica).

<h2> 🪜 Building KNN Model </h2>

1️⃣       Defining a function to calculate distance between two points.. Taking **p = 2**

<p align="center">
  <img src="https://github.com/vijeetnigam26/K-Nearest-Neighbors/blob/main/img/1.png?raw=true" height=90% width=90% />
</p>

2️⃣       Using the distance function to get the distance between a test point and all known data points

<p align="center">
  <img src="https://github.com/vijeetnigam26/K-Nearest-Neighbors/blob/main/img/2.png?raw=true" height=90% width=90% />
</p>

3️⃣       Sort distance measurements to find the points closest to the test point

<p align="center">
  <img src="https://github.com/vijeetnigam26/K-Nearest-Neighbors/blob/main/img/3.png?raw=true" height=90% width=90% />
</p>

4️⃣       Using majority class labels of those closest points to predict the label of the test point 

> Used collections.Counter to keep track of the labels that coincide with the nearest neighbor points and then used the counter.most_common() to return the most commonly occurring label.

5️⃣        Repeat Steps 1 through 4 until All the test data points are classified 

> Firstly, perform a train_test_split on the data (75% train, 25% test), and then scale the data using StandardScaler(). Since KNN is distance-based, it is must to make sure that the features are scaled properly before feeding them into the algorithm. To avoid data leakage, its good to scale the features after the train_test_split has been performed. First, scale the data from the training set only (scaler.fit_transform(X_train)), and then use that information to scale the test set (scaler.tranform(X_test)). This ensures that no information outside of the training data is used to create the model.
> <h4> knn_predict() </h4>
> Function takes in all of the training and test data, k, and p, and returns the predictions my KNN classifier makes for the test set (y_hat_test). The function should return a list of label predictions containing only 0’s, 1’s and 2’s.

<h2> 🎯 Accuracy </h2>

My KNN Model's Accuracy: **0.9736842105263158**

Sklearn KNN Accuracy: **0.9736842105263158** 

<h2> 📉 Effect of Varying 'k' </h2>

KNN doesn’t have as many tune-able parameters as other algorithms like Decision Trees or Random Forests, but k happens to be one of them. Observing the classification accuracy variation with the varying 'k' value:

<p align="center">
  <img src="https://github.com/vijeetnigam26/K-Nearest-Neighbors/blob/main/img/__results___22_0.png?raw=true" height=60% width=60% />
</p>

