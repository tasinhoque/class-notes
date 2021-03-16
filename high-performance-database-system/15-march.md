## Question 7-1

Distribution skew is eliminated since there's more virtual nodes than real nodes. Since we're using Round-Robin partitioning technique to distribute the virtual nodes, partition skew doesn't occur, since the partitions are almost of same size.

In this partitioning, virtual nodes can be moved from a heavily loaded (real) node to a less loaded node. In this way, the total load is balanced and execution skew is handled.

## Question 7-2

In a parallel storage system, the partitioning table is usually stored in the master node. The table is usually replicated and distributed among routers and client nodes for faster query processing.

This particular table helps routers to map virtual nodes to real nodes for a particular query. When a router accepts a read/write request from a client, it forwards the request to the appropriate real node.

Also, dynamic partitioning consistently changes the partitioning table, which means each update is applied to all instances of the table. Thus, query diversion is achieved.
