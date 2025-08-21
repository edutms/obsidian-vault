2025-08-21 10:49

### Status: #baby

### Tags: [[data-engineering]] [[pyspark]]

# What is  a spill in PySpark?

A spill in PySpark happens when Spark has more intermediate data that it can hold in memory during a given stage of the process, for example during a data shuffle, join, sort or aggregation. Instead of crashing, Spark will **"spill"** bits of this data from RAM into disk to keep it going.

Per ChatGPT:
	“My backpack (RAM) is full, so I’ll dump some notes into a locker (disk) until I need them again.”


##### Spills happen when:
- shuffle operations, when data is repartitioned across the cluster (during a groupBy, join or orderBy)
- Aggregations: big groupBy's with lots of keys
- Large sorts
## Descriptions





# References









