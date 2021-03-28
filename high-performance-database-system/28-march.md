## Question 12-1

a. Because we're querying a single value of district.

b. Same processing time.

## Question 12-2

It's given that the schema has been partitioned on NID. Hence, selection will be performed at only the nodes where partition of the node overlaps with the specified range of values. We'll take the overlapping region for each node.

## Question 12-3

- Step 1: Partition the relation on the grouping attributes
- Step 2: Compute the aggregate values locally at each node
