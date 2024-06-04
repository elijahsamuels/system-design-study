# Consistency

**write-write conflict** - two people are updating the same data item at the same time
**serialize writes** - decide to apply one write, then another write in the case of a write-write conflict
**lost update** - data is overwritten without concurrency control

**pessimistic approach** - prevents write conflicts
**optimistic approach** - allows write conflicts but handles them and sorts it out

## Optimistic Approaches - 
- **conditional update** - any client that does an update test the value just before updating it to see if it's changed since the last read
- **unknown name** - save both updates and record there is a conflict, then let the user decide how to sort it out.

Pessimistic approaches
- generally degrade the responsivenesss of a system
- leads to deadlocks (hard to prevent and hard to debug)
  
## Read Consistency
**read-write conflict** - data in state 1 is updated by user A, data in state 1 is read by user B, and updated to state 2 again by user A
**logical consistency** - ensuring that different data items make sense together
**inconsistency window** - length of time an inconsistency is presnet
**replication consistency** - ensuring that the same data item has the same value whenread from different replicas
**eventually consistent** - at any time nodes may have replication inconsistencies but if ther are no further updates, eventually all nodes will be updated to the same value.
**stale (data)** - data that is out of date

**sticky session (aka session affinity)** - a session thats tied to one node

## CAP Theorem
**Consistency, Availability and Partition tolerance** - you only get 2

- **Consistency** - *see above*
- **Availablity** - if you can talk to a node, it can read and write
- **Partition Tolerance** - the cluster can survive communcation failues in the cluster that separate the cluster into multiple partitions unable to communicate with each other (a situation known as **split brain**)

