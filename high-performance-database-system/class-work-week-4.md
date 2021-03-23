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

1. We'll repartition r1, r2, ..., r10 into new partitions r1', r2', ..., r6'. We'll do the same thing for s. Each new partition ri & si will contain entries having `yearAdmit` in partition Pi.

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

## Question 10-1

a. There are 4 runs. If we take 5 as our memory size, we'll be able to keep an input buffer of size four (equal to the run count) and will be able to perform external sort in one pass.

b. If we take a memory size equal to the number of elements we need to sort, quicksort can be used.

c. If we increase memory size, number of merge pass will decrease and sort performance will increase consequently.

## Question 10-2

a. Since the relation has been range-partitioned on the attribute on which it is to be sorted, we can sort each partition separately and concatenate the results to get the full sorted relation.

b. We can do either of the two things below:

- We can range-partition the relation on the sort attributes and sort each partition separately.
- We can use a parallel version of the external merge sort algorithm.

## Question 11-1

a. Intra-operation parallelism: There will be a single join operation running in multiple processors in parallel.

Inter-operation parallelism: We'll divide the 30 nodes into 3 groups. If we assume they are m1, m2 and m3, the execution will look like this:

temp1 = m1 join m2

res = temp1 join m3

## Question 11-2

a. The operations at each of the nodes are:

N1: temp1 = s1 join s2  
N2: temp2 = s3 join s4  
N3: temp3 = s5 join s6  
N4: temp4 = temp1 join temp2  
N5: temp5 = temp3 join temp4

After execution of both N1 and N2 are finished, execution of N4 will begin and will run in parallel with N3. Execution of N5 will begin only after both N3 and N4 have finished executing.

b. Pipeline parallelism is faster than independent parallelism.

Execution takes place in stages for independent parallelism. At first, only the leaf nodes are allowed to run. After all of them are finished, the parent nodes can start running. This wastes a lot of CPU time since many parent nodes have to stay idle even when their children have finished executing.

Even though pipeline parallelism is slower than the combined one, it's still faster than the independent one since a group of nodes don't block out other nodes here. As soon as the node in control finishes execution, the next node takes control.
