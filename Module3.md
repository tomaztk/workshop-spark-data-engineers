# Module 3: Designing and building pipelines, moving data and building data models with Spark


# What are pipelines

Data pipelines are set of instructions for data movement from source to sink. It is commonly known in data scinece community and also between data engineers for ETL or ELT.

Pipeline is undestood as a:
1.  sequence of transformations on data
2. Source data is typically semi-structured/unstructured (JSON, CSV etc.) and structured (JDBC, Parquet, ORC, the other Hive-serde tables)
3. Output data is integrated, structured and curated.
4. Data at the end of the pipeline is ready for further data processing, analysis and reporting.




# Building Pipelines using Spark

```
// assumes you are under $SPARK_HOME
val rdd = sc.textFile("data/mllib/sample_movielens_data.txt").map { line =>
  val Array(user, item, rating) = line.split("::")
  (user, item, rating)
}

```

Create the dataFrame

```
val df = sqlContext.createDataFrame(rdd).toDF("user", "item", "rating")
```

```
df.show
```


# Data Sources and DAta Sinks

## Reading data with spark, Python, R

## Storing data with Spark, Python, R



# Moving data around




# Working with SQL

all SQL functions: https://spark.apache.org/docs/latest/api/sql/index.html


# Working with Parquet

## using Python

## using R

# Using SQL

# Working with RDD files

# Modelling data
