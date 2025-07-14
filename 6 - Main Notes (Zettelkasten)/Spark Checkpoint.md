2025-07-11 09:46

### Status:  #baby

### Tags: [[data-engineering]] [[spark]]

# What is checkpointing in Spark?

It is a mechanism to **truncate lineage** of the DataFrame/RDD via materializing it to a durable storage (disk or S3). I aims to prevent:
- stack overflow/out-of-memory in long lineage chains
- improving fault tolerance
- enabling iterative algorithims (such as connectedComponnents(), which is the current usecase at B Lab)

# Why [[GraphFrames]] needs it

1. iterative, it traverse the graph to find connected subgroups
2. each iteration is built on top of the previous one, which make the lineage increase
3. it avoinds infinite DAGs (or deep planning)
4. 




# References









