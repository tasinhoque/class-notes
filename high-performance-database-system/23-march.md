## Question 11-1

a. Intra-operation parallelism: There will be a single join operation running in multiple processors in parallel.

Inter-operation parallelism: We'll divide the 30 nodes into 3 groups. If we assume they are m1, m2 and m3, the execution will look like this:

temp1 = m1 join m2

res = temp1 join m3

## Question 11-2

a. The operations at each of the nodes are:

(independent parallelism)  
N1: temp1 = s1 join s2  
N2: temp2 = s3 join s4  
N3: temp3 = s5 join s6

(pipelined parallelism)  
N4: temp4 = temp1 join temp2  
N5: result = temp3 join temp4

After execution of both N1 and N2 are finished, execution of N4 will begin and will run in parallel with N3. Execution of N5 will begin only after both N3 and N4 have finished executing.

b. Pipeline parallelism is faster than independent parallelism.

Execution takes place in stages for independent parallelism. At first, only the leaf nodes are allowed to run. After all of them are finished, the parent nodes can start running. This wastes a lot of CPU time since many parent nodes have to stay idle even when their children have finished executing.

Even though pipeline parallelism is slower than the combined one, it's still faster than the independent one since a group of nodes don't block out other nodes here. As soon as the node in control finishes execution, the next node takes control.
