## Remarks on R

Remarks on Currently Used Technologies

- R
- Python


#### Remarks on R

* Coillte have been using the R programming language very successfully. R Software was a key component of the NIS document processing, and Cutting Strategy Analyses.
* The Remsoft Server has, as part of its design specifications, java Interface packages that allow R to communicate with MS office packages.
* Serious issues have arisen with the PSM2i Server in the past regarding the inability to install necessary software updates. 
* Can we get a bespoked R & Python Server - with a regular update policy
   
Remarks on Python

* (DMcI & JP)



-------------------------------------------------------------------------------------
## Data.Table


-------------------------------------------------------------------------------------
## R package {dbplyr}

* dbplyr is a "TidyVerse" back end for databases that allows you to work with remote database tables as if they are in-memory data frames. 
* Basic features works with any database that has a 'DBI' back end; more advanced features require 'SQL' translation to be provided by the package author.

* Reference: https://cran.r-project.org/web/packages/dbplyr/vignettes/dbplyr.html
* Reference: https://www.nickvasile.com/2020/04/16/dplyr-and-microsoft-sql-server/


-------------------------------------------------------------------------------------

## Spark

Apache Spark™ is a unified analytics engine for large-scale data processing.


#### Versions

#### References
* http://spark.apache.org/



-------------------------------------------------------------------------------------

## Spark Interfaces: PySpark and sparklyr


### sparklyr: R interface for Apache Spark

* This package supports connecting to local and remote Apache Spark clusters, provides a 'dplyr' compatible back-end, and provides an interface to Spark's built-in machine learning algorithms.
* With {sparklyr}, you can connect to both local instances of Spark as well as remote Spark clusters. Here we’ll connect to a local instance of Spark via the spark_connect function.

#### References
* https://spark.rstudio.com/
* https://cran.r-project.org/web/packages/sparklyr/index.html


### PySpark
PySpark is a great language for performing exploratory data analysis at scale, building machine learning pipelines, and creating ETLs for a data platform. If you’re already familiar with Python and libraries such as Pandas, then PySpark is a great language to learn in order to create more scalable analyses and pipelines. 


Apache Spark is a Python API for Spark that supports the collaboration of Apache Spark and Python
PySpark interfaces with Resilient Distributed Datasets (RDDs) in Apache Spark and Python, by means of the Py4j library.
Py4J is a popular library which is integrated within PySpark and allows python to dynamically interface with JVM objects.

#### Reference

* https://towardsdatascience.com/a-brief-introduction-to-pyspark-ff4284701873
* https://databricks.com/discover/introduction-to-data-analysis-workshop-series/intro-apache-spark

------------------------------------------------------------------------------

##  Apache Arrow

* Apache Arrow is a cross-language development platform for in-memory data. 
* Apache Arrow defines a language-independent columnar memory format for flat and hierarchical data, organized for efficient analytic operations on modern hardware like CPUs and GPUs. The Arrow memory format also supports zero-copy reads for lightning-fast data access without serialization overhead.


Arrow itself is not a storage or execution engine. It is designed to serve as a shared foundation for the following types of systems:

* SQL execution engines (e.g., Drill and Impala)
* Data analysis systems (e.g., Pandas and Spark)
* Streaming and queueing systems (e.g., Kafka and Storm)
* Storage systems (e.g., Parquet, Kudu, Cassandra and HBase)

#### References

* https://www.dremio.com/origin-history-of-apache-arrow/

-------------------------------------------------------------------------------------

## Hadoop

* Hadoop is an ecosystem of open source components that fundamentally changes the way enterprises store, process, and analyze data. 

#### Distributions

* Hadoop is available either open-source through the Apache distribution, or through vendors such as Cloudera (the largest Hadoop vendor by size and scope), MapR, or HortonWorks.


#### Version Status

* Initial release	April 1, 2006;
* Version Series 3.3.x	(i.e. 3.3.0 etc) was released on 14 July 2020

#### Hadoop Ecosystem

* The term Hadoop is often used for both base modules and sub-modules and also the ecosystem, or collection of additional software packages that can be installed on top of or alongside Hadoop, such as Apache Pig, Apache Hive, Apache HBase, Apache Phoenix, Apache Spark, Apache ZooKeeper, Cloudera Impala, Apache Flume, Apache Sqoop, Apache Oozie, and Apache Storm.




#### Performace Comparison 

Spark: Spark has been found to run 100 times faster in-memory, and 10 times faster on disk. It's also been used to sort 100 TB of data 3 times faster than Hadoop MapReduce on one-tenth of the machines. Spark has particularly been found to be faster on machine learning applications, such as Naive Bayes and k-means.(https://logz.io/blog/hadoop-vs-spark/).


#### Hadoop References

* https://searchdatamanagement.techtarget.com/definition/Hadoop

------------------------------------------------------------------------------------

## Graph Analytics


### Use-case Applications of Graph Analytics 

*(Source: https://www.ibmbigdatahub.com/blog/what-graph-analytics)*

* Performing grid and network quality of service such as identifying weaknesses in power grids, water grids and transportation networks as well as helping prevent cybercrime attacks on computer networks
* Optimizing routes in the airlines and retail and manufacturing industries as well as for supply distribution chains and logistics
* Conducting research in life sciences (bioinformatics) including medical research, disease pathologies and so on

### What is a Graph Database?

Very simply, a graph database is a database designed to treat the relationships between data as equally important to the data itself. It is intended to hold data without constricting it to a pre-defined model. Instead, the data is stored like we first draw it out - showing how each individual entity connects with or is related to others.

------------------------------------------------------------------------------

## Neo4J
Neo4j is an open-source, NoSQL, native graph database that provides an ACID-compliant transactional backend for your applications. Initial development began in 2003, but it has been publicly available since 2007. The source code, written in Java and Scala, is available for free on GitHub or as a user-friendly desktop application download

#### Use Case

* "Transforming Logistics: Real-time Routing and Tracking with Neo4j"

“A logistics network is a graph, and doesn’t fit the table structure of a relational database well,” says Wagenknecht. The team chose Neo4j for its flexibility and scalability. With Neo4j’s native graph storage and processing engine, transactions took milliseconds, not minutes, for high-speed, full graph, database traversals.

* https://neo4j.com/case-studies/global-500-logistics/

#### Use Case: Supply Chain Management

* https://neo4j.com/graphgist/supply-chain-management


#### Interfaces

* (https://neo4j.com/developer/spark/)
* Conneting to Neo4J from Python (https://neo4j.com/developer/python/)

#### References

* https://neo4j.com/graph-databases-book/


