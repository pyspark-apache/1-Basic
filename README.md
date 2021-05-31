# 1-Basic



## 1. Import libraries
~~~python
import pyspark
from pyspark.sql import SparkSession
~~~
A SparkSession can be used create DataFrame, register DataFrame as tables, execute SQL over tables, cache tables, and read parquet files. To create a SparkSession, use the following builder pattern:


## 2. Create sparksession
~~~python
spark = SparkSession.builder.appName("Practice").getOrCreate()
~~~


## 3. Read data
~~~python
df_pyspark = spark.read.option("header","true").csv("all_data.csv")
~~~

## 4. printSchema()
~~~python
df_pyspark.printSchema()

root
 |-- Order ID: string (nullable = true)
 |-- Product: string (nullable = true)
 |-- Quantity Ordered: string (nullable = true)
 |-- Price Each: string (nullable = true)
 |-- Order Date: string (nullable = true)
 |-- Purchase Address: string (nullable = true)
 ~~~