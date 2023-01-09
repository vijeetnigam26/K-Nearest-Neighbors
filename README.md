<h2 align="center"> K Nearest Neighbors </h2>

<p align="center">
  <img src="https://miro.medium.com/max/1080/0*49s1xDlDKDsn55xa.gif" height=55% width=55% />
</p>

K-Nearest Neighbors (KNN) is a **supervised machine learning algorithm** that can be used for either **regression** or **classification** tasks. It is **non-parametric**, which means that the algorithm does not make assumptions about the underlying distributions of the data. This algorithm is based on **Feature Similarity**. This is in contrast to a technique like linear regression, which is parametric, and requires us to find a function that describes the relationship between dependent and independent variables.

<h2> Minkowski Distance</h2>

The distance between points is determined by using a generalized formula, known as Minkowski distance, i.e., represented as follows:

<p align="center">
<img src="https://miro.medium.com/max/1000/1*nxGbicBE1MSV4LbBFueJvg.png" height=45% width=45% style="text-align:center;">
</p>

*where X and Y are data points, n is the number of dimensions, and p is the Minkowski power parameter.*

When **p=1**, the distance is known at the **Manhattan (or Taxicab) distance**, and when **p=2** the distance is known as the **Euclidean distance**. 


