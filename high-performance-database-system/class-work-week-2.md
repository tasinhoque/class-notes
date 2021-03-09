# Week 2 Class Works

### Question 4-1

There are 40 nodes and 40,000 tuples. Here is how the tuples will be distributed:  
N`0` = [T`0`, T`40`, ..., T`39960`]  
N`1` = [T`1`, T`41`, ..., T`39961`]  
.  
.  
.  
N`39` = [T`39`, T`79`, ..., T`39999`]

### Question 4-2

There are 40 nodes and 40,000 tuples. Here is how the tuples will be distributed:

a. N`h(NID_i)` = [T`i`] (for all `i`)  
 Explanation: We'll put the `i`th tuple in the node having id equal to the result of the hash of NID`i`.  
b. N`h(street_i, city_i, district_i)` = [T`i`] (for all `i`)  
 Explanation: We'll put the `i`th tuple in the node having id equal to the result of the hash of NID`i`.

### Question 4-3

a. Partition vector = [202,105,021, 202,105,041, ..., 202,105,381]  
b. The required partitions are:  
 P`0` = [202,105,001, ..., 202,105,020]  
 P`1` = [202,105,021, ..., 202,105,040]  
 P`19` = [202,105,381, ..., 202,105,400]

### Question 4-4

a. If there are n tuples in Person DB and m tuples in Parents DB, then with brute force technique we need to perform n \* m operations in the worst case. But with range partitioning, we can search the DB in the following manner:

Search for all pair from Partition`1, Person` and Partition`1, Parents` (n \* m / 16 operations in the worst case). Then for Partition`2, Person` and Partition`2, Parents` and so on.

b. For four nodes, the speed-up is four, since time elapsed has decreased four-fold. The scale-up depends on the problem size. If the problem size is unchanged, the scale-up is four-fold. But if the problem size is also increased as much as the time is decreased, the scale-up is one.

### Question 5-1

a. Good, since all nodes have almost an equal number of tuples.  
b. Good  
c. Bad, since we wouldn't get any range from such partitioning.

### Question 5-2

a. Good when the hash function is good and partitioning attributes form a key, since tuples will be equally distributed between nodes.  
b. Good for point queries on partitioning attributes.  
c. Bad, since for range queries, all nodes must be processed.

### Question 5-3

a. Good, since it provides data clustering.  
b. Good for point queries on partitioning attributes.  
c. Good if the result tuples are from a few blocks.

### Question 6-1

a. These skews can occur:

1.  Attribute-value skew: Due to skew inherent in the dataset.

b. These skews can occur:

1.  Attribute-value skew: Due to skew inherent in the dataset.
1.  Partition skew: When the partition vector is badly chosen.
1.  Execution skew

### Question 6-2

a. The type of the histogram is Equi-width.  
b.

- Total frequencies = 5 \* (45 + 35 + 25 + 50 + 15) = 850 = 4 \* 212.5
- Partition vector, V = [5, 10, 17]
- Partitions:
  - P`0` = [1, ..., 4]  
    Sum: 180  
    Average freq: 180 / 4 = 45
  - P`1` = [5, ..., 9]  
     Sum: 185  
     Average freq: 185 / 5 = 37
  - P`2` = [10, ..., 16]  
    Sum: 210  
    Average freq: 210 / 7 = 30
  - P`3` = [17, ..., 25]  
    Sum: 275  
    Average freq: 275 / 9 = 30.6

c. ![img](https://i.imgur.com/3ZqVmQR.png)
