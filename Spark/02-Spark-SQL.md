

#### Spark SQL

Originally known as Shark, Spark SQL has become more and more important to the Apache Spark project. 
It is likely the interface most commonly used by today’s developers when creating applications. 
Spark SQL is focused on the processing of structured data, using a dataframe approach borrowed from R and Python (in Pandas). But as the name suggests, Spark SQL also provides a SQL2003-compliant interface for querying data, bringing the power of Apache Spark to analysts as well as developers.

Alongside standard SQL support, Spark SQL provides a standard interface for reading from and writing to other datastores including JSON, HDFS, Apache Hive, JDBC, Apache ORC, and Apache Parquet, all of which are supported out of the box. Other popular stores—Apache Cassandra, MongoDB, Apache HBase, and many others—can be used by pulling in separate connectors from the Spark Packages ecosystem.

Selecting some columns from a dataframe is as simple as this line:
<pre><code>
citiesDF.select(“name”, “pop”)
</code></pre>
Using the SQL interface, we register the dataframe as a temporary table, after which we can issue SQL queries against it:

<pre><code>
citiesDF.createOrReplaceTempView(“cities”)
spark.sql(“SELECT name, pop FROM cities”)
</code></pre>

Behind the scenes, Apache Spark uses a query optimizer called Catalyst that examines data and queries in order to produce an efficient query plan for data locality and computation that will perform the required calculations across the cluster. In the Apache Spark 2.x era, the Spark SQL interface of dataframes and datasets (essentially a typed dataframe that can be checked at compile time for correctness and take advantage of further memory and compute optimizations at run time) is the recommended approach for development. The RDD interface is still available, but is recommended only if you have needs that cannot be encapsulated within the Spark SQL paradigm.
