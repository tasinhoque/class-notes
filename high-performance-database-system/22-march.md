## Question 10-1

M = Memory size

N = Number of runs

a. (Sir said, wrong in my opinion: M = 4, 3 runs, 1 merge pass)

There are 4 runs. If we take 5 as our memory size, we'll be able to keep a input buffer of size four (equal to the run count).

b. Memory size = number of elements

c. If we increase memory size, number of run will decrease.

## Question 10-2

a. Since the relation has been range-partitioned on the attributes on which it is to be sorted, we can sort each partition separately and concatenate the results to get the full sorted relation.

b. We can do either of the two things below:

- We can range-partition the relation on the sort attributes, and then sort each partition separately.
- We can use a parallel version of the external sort-merge algorithm.

---

Missing figure in the slide:

![img](https://i.imgur.com/zxwPHiH.png)
