# 1 Basic

1. [Import libraries ](#schema1)
2. [Create sparksession](#schema2)
3. [Read data](#schema3)
4. [PrintSchema()](#schema4)

<hr>

<a name="schema1"></a>

## 1. Import libraries
~~~python
import pyspark
from pyspark.sql import SparkSession
~~~
A SparkSession can be used create DataFrame, register DataFrame as tables, execute SQL over tables, cache tables, and read parquet files. To create a SparkSession, use the following builder pattern:

<hr>

<a name="schema2"></a>

## 2. Create sparksession
~~~python
spark = SparkSession.builder.appName("Practice").getOrCreate()
~~~

<hr>

<a name="schema3"></a>

## 3. Read data
~~~python
df_pyspark = spark.read.option("header","true").csv("all_data.csv")
~~~

<hr>

<a name="schema4"></a>

## 4. PrintSchema()
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