#### MLlib 
The MLlib library contains algorithms and utilities for
classification, regression, clustering, collaborative filtering and dimensionality reduction. Essentially, you would use
this for specific machine learning use cases that requires these algorithms. In the lab exercise, you will use the
clustering K-Means algorithm on a set of taxi drop off points to figure out potentially where the best place to hail a
cab would be.


#### Summary:
Having completed this lesson, you should be able to understand and use the various Spark libraries.


#### Spark MLlib

Apache Spark also bundles libraries for applying machine learning and graph analysis techniques to data at scale. Spark MLlib includes a framework for creating machine learning pipelines, allowing for easy implementation of feature extraction, selections, and transformations on any structured dataset. MLLib comes with distributed implementations of clustering and classification algorithms such as k-means clustering and random forests that can be swapped in and out of custom pipelines with ease. Models can be trained by data scientists in Apache Spark using R or Python, saved using MLLib, and then imported into a Java-based or Scala-based pipeline for production use.

Note that while Spark MLlib covers basic machine learning including classification, regression, clustering, and filtering, it does not include facilities for modeling and training deep neural networks (for details see InfoWorld’s Spark MLlib review). However, Deep Learning Pipelines are in the works.

