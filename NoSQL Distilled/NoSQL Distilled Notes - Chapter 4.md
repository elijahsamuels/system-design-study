# Distribution Models

the primary driver of interest in NoSQL has been its ability to run databases on a large cluster
- run the datase on a cluster of servers
  
two paths to data distribution
- replication
- sharding

**Replication** - the same data and copies it over multiple nodes
**Sharding** - different data on different nodes

	Two forms of Replication 
		- master-slave
		- peer-to-peer

simple to complex
- single-server
- sharding
- master-slave
- peer-to-peer

## Single Server
- no replication
- always choose this if you can get away with it (super easy)

## Sharding
- puts different data in different parts
- a busy data store is busy because different people are accessing different parts
- **Auto-Sharding** - database takes on responsibilty of allocating data to shards and ensuring that data access goes to the right shard
- can improve both read and write performance
- provides a way to horizontonally scales writes
- some databases are intended to use sharding from the beginning
- use sharding well before you need it

## Master-Slave (Primary-Secondaries) Replication

- replicate data across multiple nodes
- use for scalling a read-intensive dataset
- read resilence (if the primary fails, the secondaries can fill in)
- primary can be assigned manually or automatically
  - manually - you have to make a new primary if the original primary fails
  - automatically - one of the secondaries elects themselves to be the new primary - reduces downtime
- leads to more frequent inconsistient data

## Peer-to-Peer Replication
- all replicas have equal weight
- all accept writes
- if one fails, all of the data store is available
- can lead to write-write conflicts
- 

