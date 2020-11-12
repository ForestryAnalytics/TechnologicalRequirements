
#### Spark Core

In comparison to MapReduce and other Apache Hadoop components, the Apache Spark API is very friendly to developers, hiding much of the complexity of a distributed processing engine behind simple method calls. The canonical example of this is how almost 50 lines of MapReduce code to count words in a document can be reduced to just a few lines of Apache Spark (here shown in Scala):


\begin{verbatim}
val textFile = sparkSession.sparkContext.textFile(“hdfs:///tmp/words”)
val counts = textFile.flatMap(line => line.split(“ “))
                      .map(word => (word, 1))
                      .reduceByKey(_ + _)
counts.saveAsTextFile(“hdfs:///tmp/words_agg”)
\end{verbatim}


\begin{verbatim}
val textFile = sparkSession.sparkContext.textFile(“hdfs:///tmp/words”)
val counts = textFile.flatMap(line => line.split(“ “))
                      .map(word => (word, 1))
                      .reduceByKey(_ + _)
counts.saveAsTextFile(“hdfs:///tmp/words_agg”)
\end{verbatim}

By providing bindings to popular languages for data analysis like Python and R, as well as the more enterprise-friendly Java and Scala, Apache Spark allows everybody from application developers to data scientists to harness its scalability and speed in an accessible manner.

#### Spark RDD

At the heart of Apache Spark is the concept of the Resilient Distributed Dataset (RDD), a programming abstraction that represents an immutable collection of objects that can be split across a computing cluster. Operations on the RDDs can also be split across the cluster and executed in a parallel batch process, leading to fast and scalable parallel processing.

RDDs can be created from simple text files, SQL databases, NoSQL stores (such as Cassandra and MongoDB), Amazon S3 buckets, and much more besides. Much of the Spark Core API is built on this RDD concept, enabling traditional map and reduce functionality, but also providing built-in support for joining data sets, filtering, sampling, and aggregation.

Spark runs in a distributed fashion by combining a driver core process that splits a Spark application into tasks and distributes them among many executor processes that do the work. These executors can be scaled up and down as required for the application’s needs.



By providing bindings to popular languages for data analysis like Python and R, as well as the more enterprise-friendly Java and Scala, Apache Spark allows everybody from application developers to data scientists to harness its scalability and speed in an accessible manner.
