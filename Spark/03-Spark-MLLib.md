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

--------------------------------------------------------\section*{MLlib}
%=================================%

\begin{itemize}
\item  MLlib is a machine learning library that provides various algorithms designed to scale out on a cluster for classification, regression, clustering, collaborative filtering, and so on. 
\item Some of these algorithms also work with streaming data, such as linear regression using ordinary least squares or k-means clustering (and more on the way). 
\item Apache Mahout (a machine learning library for Hadoop) has already turned away from MapReduce and joined forces on Spark MLlib.
\end{itemize}
\newpage

The advantages of MLlib’s design include:
\begin{description}
\item[Simplicity:] Simple APIs familiar to data scientists coming from tools like R and Python. Novices are able to run 
algorithms out of the box while experts can easily tune the system by adjusting important knobs and switches (parameters).

\item[Scalability:] Ability to run the same ML code on your laptop and on a big cluster seamlessly without breaking down. 
This lets businesses use the same workflows as their user base and data sets grow.
Streamlined end-to-end: Developing machine learning models is a multistep journey from data ingest through trial 
and error to production. Building MLlib on top of Spark makes it possible to tackle these distinct needs with a 
single tool instead of many disjointed ones. The advantages are lower learning curves, less complex development 
and production environments, and ultimately shorter times to deliver high-performing models.

\item[Compatibility:] Data scientists often have workflows built up in common data science tools, such as R, Python pandas, and 
scikit-learn. Spark DataFrames and MLlib provide tooling that makes it easier to integrate these existing workflows with 
Spark. For example, SparkR allows users to call MLlib algorithms using familiar R syntax, and Databricks is writing 
Spark packages in Python to allow users to distribute parts of scikit-learn workflows.
At the same time, Spark allows data scientists to solve multiple data problems in addition to their machine learning problems. 
\end{description}
The Spark ecosystem can also solve graph computations (via GraphX), streaming (real-time calculations), and real-time 
interactive query processing with Spark SQL and DataFrames. The ability to employ the same framework to solve many 
different problems and use cases allows data professionals to focus on solving their data problems instead of 
learning and maintaining a different 
tool for each scenario.
