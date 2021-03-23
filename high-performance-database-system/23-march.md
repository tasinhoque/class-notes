## Question 11-1

intraoperation: a single delta

pipeline: between two deltas

divide 30 nodes in 3 groups

we'll create a scheme with 10 nodes

there will be 3 schemes running parallel

there will be 3 pipelines, each of the pipeline will execute the query in the sequence N1 -> N2 -> ... -> N30

or we can use only one pipeline

one of these scheme is inter-operation pipeline parallelism and another one is intra-operation parallelism for individual join

repartition r1, r2, r3 and r4

## Question 11-2

### Independent parallelism

N1  
temp1 = s1 join s2

N2  
temp2 = s3 join s4

N3  
temp3 = s5 join s6

N4  
temp4 = temp1 join temp2

N5  
temp5 = temp3 join temp4

### Pipelined parallelism

N1  
temp1 = s1 join s2

N2  
temp2 = s3 join temp1

N3  
temp3 = s4 join temp2

N4  
temp4 = s5 join temp3

N5  
temp5 = s6 join temp4

### Comparison:

Independent parallelism will be faster than the pipelined version since the query tree of independent parallelism is shallower than the other. When we're computing the time complexity for independent parallelism, we're taking the max time among the child nodes for computing the time for the parent. But time accumulates linearly in case of pipelined parallelism.

Best: combination of independent and pipelined is most efficient
