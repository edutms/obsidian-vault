2025-07-17 10:42

### Status: #baby

### Tags: [[data-engineering]] [[machine-learning]]

# What is MinHashLSH

MinHashLSH is a LSH class for Jaccard distance. It's input can be dense or sparse vectors, but is more efficient if sparse.

Vectors.sparse (10, [(2, 1.0), (3, 1.0), (5, 1.0)]) means that there are 10 elements in the space, and the set contains elements 2,3, and 5.

Any input vector must have at least 1 non-zero index and all non-zero values are treated as binary 1 values.







# References

https://spark.apache.org/docs/latest/api/python/reference/api/pyspark.ml.feature.MinHashLSH.html







