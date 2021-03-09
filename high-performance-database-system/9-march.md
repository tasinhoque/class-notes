### Types of skews

- Data-distribution skew
  - Attribute-value skew
- Partition skew: Less likely in hash partitioning

### Question 6-1

a. Hash partitioning: Partition skew occurs since workload may not be evenly distributed between nodes, even when input data is uniformly distributed.
b. Range partitioning: Attribute-value skew occurs, since if there's any data skew at all, it'd be due to the skew inherent in the dataset.

---

[Taken from [Springer](https://link.springer.com/referenceworkentry/10.1007%2F978-0-387-39940-9_1555)]

### Execution skew

Execution skew is a phenomenon observed in the parallel evaluation of a database query. It arises when there are imbalances in the execution of the operators running in parallel, resulting in some of the operators running for a longer time than others. The differences in execution times may cause some of the processors to remain idle while others still compute a part of the query. Execution skew can be a consequence of other forms of skew within a query, e.g., data skew, or arise because of temporally unavailable resources that affect the execution speed of a unit of work. The database system can minimize execution skew through the careful allocation of processors to operators and the selection of the appropriate parallel query plan. Execution skew arises in both operator-level parallelism as well as intra-operator parallelism. The interested reader is referred to [1] which presents a classification of skew effects in parallel database systems.

---

---

[Taken from [Springer](https://link.springer.com/referenceworkentry/10.1007%2F978-0-387-39940-9_1088)]

### Attribute-value and partition skew

Walton et al. [2] classify the effects of skewed data distribution on a parallel execution, distinguishing intrinsic skew from partition skew. Intrinsic skew is skew inherent in the dataset (e.g., there are more citizens in Paris than in Waterloo) and is thus called Attribute value skew (AVS).Partition skew occurs on parallel implementations when the workload is not evenly distributed between nodes, even when input data is uniformly...

---

### Histogram

- Equi-width
- Equi-depth

### Question 6-2

a. Type: Equi-width histogram  
b. Total frequencies = 5 \* (45 + 35 + 25 + 50 + 15) = 850 = 4 \* 212.5

- Partition vector, V = [5, 10, 17]
- Partitions:  
  P`0` = [1, ..., 4], Sum: 180, Average freq: 180 / 4 = 45  
  P`1` = [5, ..., 9], Sum: 185, AF: 185 / 5 = 37  
  P`2` = [11, ..., 16], Sum: 210, AF: 210 / 6 = 35  
  P`3` = [17, ..., 25], Sum: 275, AF: 275 / 9 = 30.6
