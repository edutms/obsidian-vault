2025-07-15 18:30

### Status:  #baby

### Tags: [[Spark]] [[data-engineering]]

# GraphFrames

GraphFrames is a Spark library that allows the building of vertex and edges dataframes in Spark. This is useful to understand and compute the similarity between one to more records.

### Capabilities

- allows to run [[graph]] algorithims such as connectedComponents()
- pattern matching 
- Leverages SparkSQL

#### Usecases

At BLab, I used it to deduplicate and create links between similar company names (trying to solve garbage-in garbage-out) by adding a fuzzymatch with [[Levenshtein]] and create links of users, assessment completion etc.




Vertices:
[a] Alice       [b] Bob       [c] Charlie

Edges:
a ---> b (friend)
b ---> c (coworker)
c ---> a (neighbor)

Together:
      (Alice)
         |
         v
      (Bob)
         |
         v
     (Charlie)
         ^
         |
         |
     back to Alice
![[Pasted image 20250715183545.png]]


# References









