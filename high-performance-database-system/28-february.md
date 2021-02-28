Class taken by Latif sir

Two types of storage:

- Volatile
- Non-volatile: Persistent

Database management deals with primary and secondary storage mainly.

Main memory database system is used for high performance computation.

Disk based DBMS is used for general-purpose uses.

---

[Copied from [StackOverflow](https://stackoverflow.com/questions/25802521/difference-between-in-memory-databases-and-disk-memory-database#:~:text=Main%20memory%20databases%20are%20faster,more%20predictable%20performance%20than%20disk.)]

An in-memory database (IMDB; also main memory database system or MMDB or memory resident database) is a database management system that primarily relies on main memory for computer data storage. It is contrasted with database management systems that employ a disk storage mechanism. Main memory databases are faster than disk-optimized databases since the internal optimization algorithms are simpler and execute fewer CPU instructions. Accessing data in memory eliminates seek time when querying the data, which provides faster and more predictable performance than disk.  
Applications where response time is critical, such as those running telecommunications network equipment and mobile advertising networks, often use main-memory databases.  
The in memory database load all the data into RAM.

### On-Disk Databases

- All data stored on disk, disk I/O needed to move data into main memory when needed.
- Data is always persisted to disk.
- Traditional data structures like B-Trees designed to store tables and indices efficiently on disk.
- Virtually unlimited database size.
- Support very broad set of workloads, i.e. OLTP, data warehousing, mixed workloads, etc.

### In-Memory Databases

- All data stored in main memory, no need to perform disk I/O to query or update data.
- Data is persistent or volatile depending on the in-memory database product.
- Specialized data structures and index structures assume data is always in main memory.
- Optimized for specialized workloads; i.e. communications industry-specific HLR/HSS workloads.
- Database size limited by the amount of main memory.

---

- Parallel Database System Architecture
  - No transmission cost
  - High performance transaction proc
  - Multiple processors and disks connection by a fast interconnected network
  - Decision support on very large amount of data
- Distributed Database System Architecture
  - Notes are situated in different locations, so there's a transmission cost

Performance Measures:

- Throughput: Number of tasks done per second (output).
- Response time

Speed-up = (Small system elapsed time) / (Large system elapsed time)  
If the large system is N times larger, the speed-up is linear if it's proportional to N.

Linear speed-up is the ideal case, not the usual case.
