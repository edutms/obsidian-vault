2024-09-17 13:47

### Status: #baby

### Tags: [[data-engineering]]

# Backfill

##### What is backfill in a Data Engineering context?
It refers to processing and loading historical data into a data system or pipeline.
This is nedeed when:
1. A new pipeline is set and it needs historical data to be loaded to provide a complete backward vision from the past into the present
2. It can correct malprocesses data in the past
3. It can help with schema/structure changes on the dataset
4. when you migrate data from one system to another

It is a super resource-intensive as it process large volumes of data.

Apache Airflow can automate by re-running certain pipeline tasks for historical data.


##### Examples of backfill on B Lab









# References









