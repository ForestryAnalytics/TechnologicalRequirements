
### sparklyr: R interface for Apache Spark

* This package supports connecting to local and remote Apache Spark clusters, provides a 'dplyr' compatible back-end, and provides an interface to Spark's built-in machine learning algorithms.
* With {sparklyr}, you can connect to both local instances of Spark as well as remote Spark clusters. Here we’ll connect to a local instance of Spark via the spark_connect function.



#### Implementation

R, RStudio, and sparklyr can be added to the YARN managed cluster. 

The highlights are:
*    R, RStudio, and sparklyr need to be installed on one node only, typically an edge node
*    The Data Scientist can access R, Spark, and the cluster via a web browser by navigating to the RStudio IDE inside the edge node




------------------------------------------

#### Deployment

There are two well supported deployment modes for sparklyr:

1.    Local — Working on a local desktop typically with smaller/sampled datasets
2.    Cluster — Working directly within or alongside a Spark cluster (standalone, YARN, Mesos, etc.)




------------------------------------------

#### References
* https://spark.rstudio.com/
* https://cran.r-project.org/web/packages/sparklyr/index.html
