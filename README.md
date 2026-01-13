# Paxos-Based Distributed State Machine
A Java-based implementation of the Paxos Consensus Protocol used to build a fault-tolerant, replicated state machine. This project demonstrates distributed systems fundamentals by synchronizing game state across multiple nodes in a strict total order.

# Key Features
Paxos Consensus: Implements Proposer, Acceptor, and Learner roles to reach agreement in an asynchronous network.
Total Order Multicast: Ensures all distributed nodes process move requests in the exact same sequence.
Fault Tolerance: Maintains system availability as long as a majority of nodes=are functional.
Graceful State Recovery: Features a custom "Shutdown Drain" mechanism that recovers in-flight messages during process termination to ensure 100% data consistency.

# Technicalities
Language: Java
Networking: Custom Group Communication Layer (GCL) for message passing.
Concurrency: Multi-threaded architecture utilizing ConcurrentHashMap, ReentrantLock and custom thread signaling for high-performance message processing.
