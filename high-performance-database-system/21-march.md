# Parallel Database Query Processing

- Inter-query parallelism: Multiple queries running in parallel
- Intra-query parallelism: Relational operations in a single query are running in parallel
  - Intra-operation
  - Inter-operation

Shared Nothing

Intraquery parallelism example explained: Instead of performing the join operation on the whole database, we partition the database and perform join on
corresponding pairs. In the slide, instead of performing join(r, s), we perform join(r1, s1), join(r2, s2), ..., join(rm, sm) respectively.

Let there be n partitions in r. We group those n partitions in m partitions. That means some partitions out of those m partitions can contain more than one partitions.

## Question 9-1

a. Partition vector, V = [2016, 2017, 2018, 2019, 2020]

Partitions:

P1 = [2015]  
P2 = [2016]  
.  
.  
.  
P6 = [2020, 2021]

b. We'll perform the join operation in the following way:

1. We'll repartition r1, r2, ..., r10 into new partitions r1', r2', ..., r6'. We'll do the same thing for s. Each new partition ri & si will contain entries in the partition Pi. For this, the old partitions can break up. For example, if entries with yearAdmit = 2015 is in both r1 and r2 then only those entries from these two old partitions will move to r1'.

2. We'll assign r1', r2', ..., r6' to nodes N1, N2, ..., N6. Again, same thing for s.

3. We'll

Perform r1' join s1' at node N1.  
Perform r2' join s2' at node N2.  
.  
.  
.  
Perform r6' join s6' at node N6.

## Question 9-2

Since number of partitioning nodes is equal to number of query nodes and the partitioning attribute and the query attribute are same, repartitioning is redundant.
