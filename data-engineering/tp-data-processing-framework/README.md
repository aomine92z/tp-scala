# Practices - Data engineering

## TP - Data processing with Apache Spark
To process a large amount of data partitioned on a data lake, you can use data processing frameworks such as Apache Spark :
1. Read : https://spark.apache.org/docs/latest/sql-programming-guide.html

Some questions :
* What is Spark RDD API ?
    Answer : Spark RDD API is used for processing immutable distributed collections of objects in parallel across a cluster.
             The API provides transformations and actions such as map, filter, reduce, groupBy, and join.
* What is Spark Dataset API ?
    Answer : Spark Dataset API is a strongly typed API for working with structured and semi-structured data.
             It provides the benefits of both RDDs and DataFrames, including strong typing, compile-time type safety, and optimized execution plans.
* With which languages can you use Spark ? 
    Answer : Spark supports multiple programming languages such as Java, Scala, Python, and R, but the most commonly used ones are Scala and Python.
* Which data sources or data sinks can Spark work with ?
    Answer : Spark works with various data sources and sinks, including HDFS, Cassandra, HBase, S3, JDBC databases, Kafka, and more.
             It also supports popular data storage and processing systems such as Avro, Parquet, and ORC, and various file formats, such as CSV, JSON, XML, and binary formats.
  



Spark works with various data sources and sinks, including HDFS, Cassandra, HBase, S3, JDBC databases, Kafka, and more. It also supports popular data storage and processing systems such as Avro, Parquet, and ORC, and various file formats, such as CSV, JSON, XML, and binary formats.
### Analyse data with Apache Spark and Scala 
One engineering team of your company created for you a TV News data stored as JSON inside the folder `data-news-json/`.

Your goal is to analyze it with your savoir-faire, enrich it with metadata, and store it as [a column-oriented format](https://parquet.apache.org/).

1. Look at `src/main/scala/com/github/polomarcus/main/Main.scala` and update the code 

**Important note:** As you work for a top-notch software company following world-class practices, and you care about your project quality, you'll write a test for every function you write.

You can see tests inside `src/test/scala/` and run them with `sbt test`

### How can you deploy your app to a cluster of machines ?
* https://spark.apache.org/docs/latest/cluster-overview.html

### Business Intelligence (BI)
How could use we Spark to display data on a BI tool such as [Metabase](https://www.metabase.com/) ?

Tips: https://github.com/polomarcus/television-news-analyser#spin-up-1-postgres-metabase-nginxand-load-data-to-pg

### Continuous build and test
**Pro Tips** : https://www.scala-sbt.org/1.x/docs/Running.html#Continuous+build+and+test

Make a command run when one or more source files change by prefixing the command with ~. For example, in sbt shell try:
```bash
sbt
> ~ testQuick
```