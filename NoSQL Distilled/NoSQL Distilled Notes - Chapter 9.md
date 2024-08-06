# Document Databases

- think about document databases as key-value stores where the value is examinable
- Popular document databases: MongoDB, CouchDB, Terrastore, OrientDB, RavenDB, Lotus Notes.

| Oracle Database                               | MongoDB                      |
| --------------------------------------------- | ---------------------------- |
| Relational Database Management System (RDBMS) | NoSQL Document Database      |
| SQL (Structured Query Language)               | MongoDB Query Language (MQL) |
| database instances                            | MongoDB instance             |
| Schemas                                       | Databases                    |
| Tables                                        | Collections                  |
| Rows                                          | Documents                    |
| rowId                                         | \_id (primary key)           |
| joins                                         | DBRef                        |

Each MongoDB instance has multiple databases and each database can have multiple collections

## Consistency

- configured by using he replica sets and choosing to wiat for the writes to be replicated to all the slaves or a given number of slaves.
- inrecase the `w` value for stronger consistency, but suffer in write performance.
- a write is reported successful once the database receives it; you can change this so as to wait for the writes to be synced to disk or to propagaget to two or more slaves. Known as `WriteConcern`. You make sure that certain writes are written to the master and some slaves by setting `WriteConcern` to `REPLICAS_SAFE`.

## Transactions

- transactions at the single document level are known as **atomic transactions** (or atomic operations).
- transactinos involing multiple documents are not possible
- set level of `WriteConcern` - adjusts safety level during writes

## Availability

- **Replica Sets** - provides high availability through replication. Provides high availability. Used for data redundancy, automated failover, read scaling, server maintenance without downtime, and disaster receovery.
- if the master node goes down, the remaining nodes in the replica set vote among themselves to elect a new master

## Query Features

- can query data inside the document without having to retrieve the whole document by its key

## Suitable Use Cases

- Event logging, content management systsm, blogging platforms, web analytics and real time analytics, ecommerce systems.

## When to Avoid

- Complex transactions, queries against varying aggregation of data.
