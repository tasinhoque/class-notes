## Question 8-1

Advantages:

- Reliability and Availability: We are storing the same data in different locations. Hence, failure of any single site (server) does not make the data unavailable.
- Fast Response: Queries requesting replicated copies of data are always faster (especially read queries).
- Less communication overhead: If a read query requires local data, we don't need to contact other sites.

Disadvantages:

- Update: Keeping all data current can be a challenge. The more locations we use to store our data, the more we’ll have to implement complex systems to keep track of what’s what.
- Storage: We’ll need more storage space as our data continues to grow.

## Question 8-2

Using 64 MB block size, we can store the 10 GB file in (10 GB / 64 MB) ~~ 160 blocks

If we allocate 16 blocks for a DataNode, we'll need 10 DataNodes. Additionally, two more sets of 10 DataNodes will be needed. Each of those 10 DataNodes will store replicas of the blocks. Hence, total 30 DataNodes will be required for the job which can be distributed among 3 racks (10 DataNodes per rack).

There will be 160 entries in the NameNode

The NameNode will contain 160 blockId entries against the given file name.
