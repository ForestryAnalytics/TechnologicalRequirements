## HDFS

* The Hadoop Distributed File System (HDFS) is a distributed file system designed to run on commodity hardware. 
* It has many similarities with existing distributed file systems. However, the differences from other distributed file systems are significant. 
* HDFS is highly fault-tolerant and is designed to be deployed on low-cost hardware. HDFS provides high throughput access to application data and is suitable for applications that have large data sets. 
* HDFS relaxes a few POSIX requirements to enable streaming access to file system data. 
* HDFS was originally built as infrastructure for the Apache Nutch web search engine project. HDFS is now an Apache Hadoop subproject. 

The project URL is https://hadoop.apache.org/hdfs/. 

------------------------------------------------------

## YARN (Yet Another Resource Negotiator)

* YARN allocates resources to various applications effectively. 
* It runs two dæmons, which take care of two different tasks: the resource manager, which does job tracking and resource allocation to applications, the application master, which monitors progress of the execution.


------------------------------------------------------
#### References

* https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html
