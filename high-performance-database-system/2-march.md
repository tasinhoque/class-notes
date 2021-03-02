### Interconnected Network Architectures

- Bus
- Mesh
- Hypercube
- Tree-like topology

### Question 3-1

---

[Taken from [Instrumentation Tools](https://instrumentationtools.com/advantages-and-disadvantages-of-network-topologies/)]

## Bus Topology

### Advantages of Bus Topology

- It is easy to set up, handle, and implement.
- It is best-suited for small networks.
- It costs very less.

### Disadvantages of Bus Topology

- The cable length is limited. This limits the number of network nodes that can be connected.
- This network topology can perform well only for a limited number of nodes. When the number of devices connected to the bus increases, the efficiency decreases.
- It is suitable for networks with low traffic. High traffic increases load on the bus, and the network efficiency drops.
- It is heavily dependent on the central bus. A fault in the bus leads to network failure.
- It is not easy to isolate faults in the network nodes.
- Each device on the network “sees” all the data being transmitted, thus posing a security risk.

## Mesh Topology

### Advantages of Mesh Topology

- The arrangement of the network nodes is such that it is possible to transmit data from one node to many other nodes at the same time.
- The failure of a single node does not cause the entire network to fail as there are alternate paths for data transmission.
- It can handle heavy traffic, as there are dedicated paths between any two network nodes.
- Point-to-point contact between every pair of nodes, makes it easy to identify faults.

### Disadvantages of Mesh Topology

- The arrangement wherein every network node is connected to every other node of the network, many connections serve no major purpose. This leads to redundancy of many network connections.
- A lot of cabling is required. Thus, the costs incurred in setup and maintenance are high.
- Owing to its complexity, the administration of a mesh network is difficult.

---

[Taken from [Wikipedia](https://en.wikipedia.org/wiki/Hypercube_internetwork_topology)]

## Hypercube Topology

In computer networking, hypercube networks are a type of network topology used to connect multiple processors with memory modules and accurately route data. Hypercube networks consist of 2m nodes, which form the vertices of squares to create an internetwork connection. A hypercube is basically a multidimensional mesh network with two nodes in each dimension. Due to similarity, such topologies are usually grouped into a k-ary d-dimensional mesh topology family, where d represents the number of dimensions and k represents the number of nodes in each dimension.

### Advantages

- Low degree of node: Each of the n nodes are connected to log(n) other nodes.
- Low diameter: Each node can reach any other node via at most log(n) links.
- Less communication delays.

---

[Taken from [Answers](https://www.answers.com/Q/What_are_the_disadvantages_of_hypercube_topology)]

### Advantages

- High fault tolerance.

---

## Fat Tree

### Advantages

- Bandwidth remains constant at each level
- High fault tolerance
- Low congestion

### Types of Architecture:

- Shared Memory Architecture
  - Common BUS
- Shared Disk Architecture
  - Every process can access common disk
  - Private memory for each process
  - Fault-tolerance
  - Bottleneck occurs at the interconnection at the disk
- Shared Nothing Architecture
  - Drawback is cost of communication and non-local disk access
  - Node consists of a processor, memory and one or more disks
- Hierarchical
  - Top level is shared nothing
  - Alternatively, top level can be shared-disk

### Solution of Question 3-1

<img src="https://i.imgur.com/Jb2XBHk.png" width="300px" />
