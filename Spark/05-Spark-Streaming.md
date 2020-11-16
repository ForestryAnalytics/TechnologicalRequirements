

#### Spark Streaming

Spark Streaming was an early addition to Apache Spark that helped it gain traction in environments that required real-time or near real-time processing. 
Previously, batch and stream processing in the world of Apache Hadoop were separate things. 

You would write MapReduce code for your batch processing needs and use something like Apache Storm for your real-time streaming requirements. This obviously leads to disparate codebases that need to be kept in sync for the application domain despite being based on completely different frameworks, requiring different resources, and involving different operational concerns for running them.

Spark Streaming extended the Apache Spark concept of batch processing into streaming by breaking the stream down into a continuous series of microbatches, which could then be manipulated using the Apache Spark API. In this way, code in batch and streaming operations can share (mostly) the same code, running on the same framework, thus reducing both developer and operator overhead. Everybody wins.

A criticism of the Spark Streaming approach is that microbatching, in scenarios where a low-latency response to incoming data is required, may not be able to match the performance of other streaming-capable frameworks like Apache Storm, Apache Flink, and Apache Apex, all of which use a pure streaming method rather than microbatches.

__________________________________________________________________________


#### Structured Streaming

Structured Streaming (added in Spark 2.x) is to Spark Streaming what Spark SQL was to the Spark Core APIs: A higher-level API and easier abstraction for writing applications. 

In the case of ***Structured Streaming***, the higher-level API essentially allows developers to create infinite streaming dataframes and datasets. 
It also solves some very real pain points that users have struggled with in the earlier framework, especially concerning dealing with event-time aggregations and late delivery of messages. 

All queries on structured streams go through the Catalyst query optimizer, and can even be run in an interactive manner, allowing users to perform SQL queries against live streaming data.

***Structured Streaming*** is still a rather new part of Apache Spark, having been marked as production-ready in the Spark 2.2 release. 
However, Structured Streaming is the future of streaming applications with the platform, so if you’re building a new streaming application, you should use ***Structured Streaming***. 

The legacy Spark Streaming APIs will continue to be supported, but the project recommends porting over to Structured Streaming, as the new method makes writing and maintaining streaming code a lot more bearable.

