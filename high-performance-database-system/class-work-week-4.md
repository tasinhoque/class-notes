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

2. We'll assign ri' to nodes Ni. Again, same thing for s.

3. We'll perform ri' join si' at node Ni.

## Question 9-2

a. We'll compute the join by performing ri join si at node Ni.  
b. Since number of partitioning nodes is equal to number of query nodes and the partitioning attribute and the query attribute are same, repartitioning is redundant.

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

a. Here, the query is:

r1 join r2 join r3 join r4 = [(r1 join r2) join r3] join r4 = (temp1 join r3) join r4 = temp2 join r4

In r1 join r2, intra-operation parallelism takes place. Inter-operation parallelism takes place in (temp1 join r3) and (temp2 join r4).

The 30 nodes can be assigned to process the following things:

N`1-10`: r1 join r2  
N`11-20`: temp1 join r3  
N`21-30`: temp2 join r4

We'll repartition r1 and r2 from the 30 nodes to N1, N2, ..., N10. We'll to do the same partitioning for the pairs (temp1, r3) and (temp2, r4).

b.

![img](https://i.imgur.com/VTyLxEF.png)

## Question 11-2

a. The operations at each of the nodes are:

N1: temp1 = s1 join s2 }  
N2: temp2 = s3 join s4 } Independent parallelism  
N3: temp3 = s5 join s6 }

N4: temp4 = temp1 join temp2 } Pipelined parallelism  
N5: result = temp3 join temp4 }

After execution of both N1 and N2 are finished, execution of N4 will begin and will run in parallel with N3. Execution of N5 will begin only after both N3 and N4 have finished executing.

b. Pipeline parallelism is faster than independent parallelism.

Execution takes place in stages in independent parallelism. At first, only the leaf nodes are allowed to run. After all of them are finished, the parent nodes can start running. This wastes a lot of CPU time since many parent nodes have to stay idle even when their children have finished executing.

Even though pipeline parallelism is slower than the combined one, it's still faster than the independent one since a group of nodes don't block out other nodes here. As soon as the node in control finishes execution, the next node takes control.
