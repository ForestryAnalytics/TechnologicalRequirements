## Spark

Apache Spark™ is a unified analytics engine for large-scale data processing.

#### Introduction

* Apache Spark is a lightning-fast cluster computing technology, designed for fast computation, and fast, in-memory data processing. 
* It is based on Hadoop MapReduce and it extends the MapReduce model to efficiently use it for more types of computations, which includes interactive queries and stream processing. 
* The main feature of Spark is its in-memory cluster computing that increases the processing speed of an application.
* Spark is designed to cover a wide range of workloads such as batch applications, iterative algorithms, interactive queries and streaming. 
* Apart from supporting all these workload in a respective system, it reduces the management burden of maintaining separate tools.
* Spark has an expressive development APIs to allow data workers to efficiently execute streaming, machine learning or SQL workloads that require fast iterative access to datasets. 
* With Spark running on Apache Hadoop YARN, developers everywhere can now create applications to exploit Spark’s power, derive insights, and enrich their data science workloads within a single, shared dataset in Hadoop.

-----------------------------------------------------------------------------------
#### Deployment

* Spark runs on Hadoop, Apache Mesos, Kubernetes, standalone, or in the cloud. It can access diverse data sources.

* Spark can be operated using its standalone cluster mode, on EC2, on Hadoop YARN, on Mesos, or on Kubernetes. Access data in HDFS, Alluxio, Apache Cassandra, Apache HBase, Apache Hive, and hundreds of other data sources. 

* Spark can closely integrate with Hadoop and Hive, the ability to cache data into memory across multiple nodes, data transformers, and its Machine Learning libraries.

-------------------------------------------------------------------------------------

## Spark Ecosystem

Other than Spark Core API, there are additional libraries that are part of the Spark ecosystem and provide additional capabilities in Big Data analytics and Machine Learning areas. These libraries facilitate Spark is an Analysis Engine. 

These libraries include:

* ***Spark Streaming***: Spark Streaming can be used for processing the real-time streaming data. This is based on micro batch style of computing and processing. It uses the DStream which is basically a series of RDDs, to process the real-time data.
* ***Spark SQL***: Spark SQL provides the capability to expose the Spark datasets over JDBC API and allow running the SQL like queries on Spark data using traditional BI and visualization tools. Spark SQL allows the users to ETL their data from different formats it’s currently in (like JSON, Parquet, a Database), transform it, and expose it for ad-hoc querying.
* ***Spark MLlib***: MLlib is Spark’s scalable machine learning library consisting of common learning algorithms and utilities, including classification, regression, clustering, collaborative filtering, dimensionality reduction, as well as underlying optimization primitives.
* ***Spark GraphX***: GraphX is the new (alpha) Spark API for graphs and graph-parallel computation. At a high level, GraphX extends the Spark RDD by introducing the Resilient Distributed Property Graph: a directed multi-graph with properties attached to each vertex and edge. To support graph computation, GraphX exposes a set of fundamental operators (e.g., subgraph, joinVertices, and aggregateMessages) as well as an optimized variant of the Pregel API. In addition, GraphX includes a growing collection of graph algorithms and builders to simplify graph analytics tasks.



Outside of these libraries, there are others like BlinkDB and Tachyon.

* ***BlinkDB*** is an approximate query engine and can be used for running interactive SQL queries on large volumes of data. It allows users to trade-off query accuracy for response time. It works on large data sets by running queries on data samples and presenting results annotated with meaningful error bars.
888=
* ***Tachyon*** is a memory-centric distributed file system enabling reliable file sharing at memory-speed across cluster frameworks, such as Spark and MapReduce. It caches working set files in memory, thereby avoiding going to disk to load datasets that are frequently read. This enables different jobs/queries and frameworks to access cached files at memory speed.


And there are also integration adapters with other products like Cassandra (Spark Cassandra Connector) and R (SparkR). With Cassandra Connector, you can use Spark to access data stored in a Cassandra database and perform data analytics on that data.

-------------------------------------------------------------------------------------

#### Versions

* Spark 3.0.0 was released on 18th June 2020.

#### References
* http://spark.apache.org/

