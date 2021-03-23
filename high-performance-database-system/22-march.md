M = Memory size

N = Number of runs

## Question 10-1

a. There are 4 runs. If we take 5 as our memory size, we'll be able to keep an input buffer of size four (equal to the run count) and will be able to perform external sort in one pass.

b. If we take a memory size equal to the number of elements we need to sort, quicksort can be used.

c. If we increase memory size, number of merge pass will decrease and sort performance will increase consequently.

## Question 10-2

a. Since the relation has been range-partitioned on the attribute on which it is to be sorted, we can sort each partition separately and concatenate the results to get the full sorted relation.

b. We can do either of the two things below:

- We can range-partition the relation on the sort attributes and sort each partition separately.
- We can use a parallel version of the external merge sort algorithm.

---

Missing figure in the slide:

![img](https://i.imgur.com/zxwPHiH.png)
