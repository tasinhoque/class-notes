## Parallel and Distributed Storage

### Parallel storage system requirements

- Storing large volume of data
- Processing time-consuming queries
- Providing high throughput
- High demand on scalability and availability

File system vs Data storage system vs Distributed database system

Horizontal Partitioning: Tuples of a relation are divided among many nodes such that some subset of the tuples resides on each node.

Vertical Partitioning: This partitioning involves creating tables with fewer columns and using additional tables to store the remaining columns.

Round-robin partitioning: **i**th tuple goes to node **i** % **n**.

---

[Taken from [Explore Database](https://www.exploredatabase.com/2014/02/data-partitioning-strategies-in.html)]

### Round-robin

It is the simplest form of partitioning strategy. Here, the data are distributed into various disks in the fashion, first record into first disk, second record into second disk, and so on. If the number of available disks n is 10, then first record goes to D1 (1 mod 10 = 1), second record goes to D2 (2 mod 10 =2), and so on and 10th record goes to D0 (10 mod 10 = 0), 11th record goes to D1 (11 mod 10 = 1). This scheme distributes data evenly in all the disks.

### Hash partitioning

This strategy identifies one or more attributes as partitioning attributes (which is not required in Round-Robin partitioning). We need a hash function which is carefully chosen (careful to avoid data skewness) which takes the identified partitioning attributes as input to hash function.

For example, consider the following table;

> EMPLOYEE(ENo, EName, DeptNo, Salary, Age)

If we choose DeptNo attribute as the partitioning attribute and if we have 10 disks to distribute the data, then the following would be a hash function;

> h(DeptNo) = DeptNo mod 10

If we have 10 departments, then according to the hash function, all the employees of department 1 will go into disk 1, department 2 to disk 2 and so on.

As another example, if we choose the EName of the employees as partitioning attribute, then we could have the following hash function;

> h(EName) = (Sum of ASCII value of every character in the name) mod n,

where n is the number of disks/partitions needed.

### Range partitioning

In Range Partitioning we identify one or more attributes as partitioning attributes. Then we choose a range partition vector to partition the table into n disks. The vector is the values present in the partitioning attribute.
For example, for the EMPLOYEE relation given above, if the partitioning attribute is Salary, then the vector would be one as follows;

> [5000, 15000, 30000],

where every value means the individual range of salaries. That is, 5000 represents the first range (0 – 5000), 15000 represents the range (5001 – 15000), 30000 represents the third range (15001 – 30000), and it includes the final range which is (30001 – rest). Hence, the vector with 3 values represents 4 disks/partitions.

The above discussed partition strategies must be chosen carefully according to the workload of your parallel database system. The workload may involve many components like, which attribute is frequently used in any queries as filtering condition, the number of records in a table, the size of the database, approximate number of incoming queries in a day, etc.

---

### Question 4-1

Total tuples: 40000  
Total N (=n) = 40  
Two racks

NID % 40  
Increases sequentially

### Question 4-2

Total tuples: 40000  
Total N (=n) = 40  
Two racks

h(NID)  
Hash function dictates where each NID goes. Range of hash function is [0, n - 1].

h(street, city, district)  
Hash function dictate where each tuple goes. Range of hash function is [0, n - 1].

### Skewing

Data skew primarily refers to a non uniform distribution in a dataset.

A data is called as skewed when curve appears distorted or skewed either to the left or to the right, in a statistical distribution. In a normal distribution, the graph appears symmetry meaning that there are about as many data values on the left side of the median as on the right side.

### Range Partitioning

Vector = [v`0`, v`1`, ..., v`n-2`] (size = n - 1)  
If v <= v`0`, go to node 0  
Else if, v`n-2` < v, go to node `n - 1`  
Else if, v`i` < v <= v`i+1`, go to the node `i + 1`

### Question 4-3

Tuples = 400  
Id range = [202_105_001, 202_105_400]  
N = 20

Partition vector = [202_105_020, 202_105_040, ..., 202_105_380] (size = 19)

P`0` = [202_105_001, ..., 202_105_020]  
P`1` = [202_105_021, ..., 202_105_040]  
P`19` = [202_105_381, ..., 202_105_400]
