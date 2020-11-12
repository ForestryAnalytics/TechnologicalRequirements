### GraphX
The GraphX is another library that sits on top of the Spark Core. It is basically a graph processing library which can
used for social networks and language modeling. Graph data and the requirement for graph parallel systems is
becoming more common, which is why the GraphX library was developed. Specific scenarios would not be efficient if
it is processed using the data-parallel model. A need for the graph-parallel model is introduced with new graph-parallel
systems like Giraph and GraphLab to efficiently execute graph algorithms much faster than general data-parallel
systems.

There are new inherent challenges that comes with graph computations, such as constructing the graph, modifying its
structure, or expressing computations that span several graphs. As such, it is often necessary to move between table
and graph views depending on the objective of the application and the business requirements.

The goal of GraphX is to optimize the process by making it easier to view data both as a graph and as collections, such
as RDD, without data movement or duplication. The lab exercise goes through an example of loading in a text file and creating a graph from it to find attributes of the
top users.


-------------------------------------------------------------------------------------------

GraphX
GraphX unifies ETL, exploratory analysis, and iterative graph computation within a single system. You can view the same data as both graphs and collections, transform and join graphs with RDDs efficiently, and write custom iterative graph algorithms using the Pregel API. 



#### Spark GraphX

GraphX is a library for manipulating graphs and performing graph-parallel operations. It provides a uniform tool for ETL, exploratory analysis and iterative graph computations. Apart from built-in operations for graph manipulation, it provides a library of common graph algorithms such as PageRank.

Spark GraphX comes with a selection of distributed algorithms for processing graph structures including an implementation of Google’s PageRank. These algorithms use Spark Core’s RDD approach to modeling data; the GraphFrames package allows you to do graph operations on dataframes, including taking advantage of the Catalyst optimizer for graph queries.
