How range partitioning is used.

[a, b) type ranges

[21, 41, ..., 381] would be the partition vector for previous day's question

### Question 4-4

- a. Apply brute force (take all pair) in partition i of person and partition i of parents.
- b. Time now 1/4 (speed-up)  
  Scale up is linear.

### Comparison of Partitioning Techniques

1. Scanning the entire relation
2. Locating a tuple associativity - point queries.
   e.g. r.A = 25
3. Range queries
   e.g. 20 < r.A < 30

### Question 5-1

a. Very good performance  
b. Inter query travel. Not that bad.

---

[Taken from [Springer](https://link.springer.com/referenceworkentry/10.1007%2F978-0-387-39940-9_1556)]

Inter-query parallelism is a form of parallelism in the evaluation of database queries, in which several different queries execute concurrently on multiple processors to improve the overall throughput of the system.

---

c. Bad, since we wouldn't get any range from such partitioning.

### Question 5-2

a. Good  
b. Good  
c. Bad

### Execution Skew

---

[Taken from [Springer](https://link.springer.com/referenceworkentry/10.1007%2F978-0-387-39940-9_1555)]

Execution skew is a phenomenon observed in the parallel evaluation of a database query. It arises when there are imbalances in the execution of the operators running in parallel, resulting in some of the operators running for a longer time than others. The differences in execution times may cause some of the processors to remain idle while others still compute a part of the query. Execution skew can be a consequence of other forms of skew within a query, e.g., data skew, or arise because of temporally unavailable resources that affect the execution speed of a unit of work. The database system can minimize execution skew through the careful allocation of processors to operators and the selection of the appropriate parallel query plan.

---

### Question 5-3

a. Bad  
b. Bad  
c. Good
