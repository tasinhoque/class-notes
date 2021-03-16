## Question 8-1

Advantages:

- Reliability and Availability: The data can be stored in different locations. Therefore, failure of any site does not affect the other transactions.
- Fast response : It gives the fast response to any type of query without any delay.
- Real time data: We can get the real time data any time which is then further used for reporting purpose.

Disadvantages:

- Update: Keeping all data current can be a challenge. The more locations we use to store our data, the more we’ll have to implement complex systems to keep track of what’s what.
- Storage: We’ll need more storage space as our data continues to grow.

## Question 8-2

64 MB block size, 10 GB file, so there'd be 10^10/(64x10^6) = (at least) 157 blocks ~ 160 blocks

We assume there's 1000 DataNodes

1 rack contains 40 DataNodes, so there's 25 racks

160 entries in the NameNode

10 DataNodes will contain the blocks and further 20 DataNodes will contain replicas

So, each DataNodes can contain ceil(160/30) = 6 blocks
