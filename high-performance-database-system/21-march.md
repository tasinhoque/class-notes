# Parallel Database Query Processing

- Interquery parallelism: Multiple queries running in parallel
- Intraquery parallelism: Relational operations in a single query are running in parallel
  - Intraoperation
  - Interopereation

Shared Nothing

Intraquery parallelism example explained: Instead of performing the join operation on the whole database, we partition the database and perform join on
corresponding pairs. In the slide, instead of performing join(r, s), we perform join(r1, s1), join(r2, s2), ..., join(rm, sm) respectively.

Let there be n partitions in r. We group those n partitions in m partitions. That means some partitions out of those m partitions can contain more than one partitions.

## Question 9-1

yearAdmit (all values) = [2015, 2016, 2017, 2018, 2019, 2020, 2021]

Partition vector, V = [2016, 2017, 2018, 2019, 2020]

P`1` = [2015]
P`2` = [2016]
.
.
.
P`6` = [2020, 2021]

We'll get 6 nodes.

Each new partition ri & si will contain entries in the partition Pi. For this, the old partitions can break up. For example, if entries with yearAdmit = 2015 is in both r_old`1` and r_old`2` then only those entries from these two old partitions will move to r_new`1`.

## Question 9-2

Since number of partitioning node is equal to number of query node and partitioning attribute and query attribute are same, repartitioning is redundant.
