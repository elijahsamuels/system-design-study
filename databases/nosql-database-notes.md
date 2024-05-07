# Things to consider:
- what operating systems can it run on? 
	ex. MySQL and PostgreSQL can run on Windows, macOS, Linux, BSD, UNIX, AmigaOS, z/OS, and Android, but EXASolution ONLY runs on Linux.
	Most will run on Windows > Linux > UNIX > macOS


# Types of NoSQL Databases

## Key–value database (key–value store)
- data storage paradigm designed for storing, retrieving, and managing associative arrays, and a data structure known as a dictionary (hash table)
- often use far less memory to store the same data compared to RDBS

## Wide-column store (extensible record store)
- uses tables, rows, and columns, but unlike a relational database, the names and format of the columns can vary from row to row in the same table

## Column-oriented DBMS (columnar DBMS)
- stores data tables by column rather than by row
- efficient for queries that perform analytics, aggregation, or summaries over large datasets
- Better compression & efficient data retrieval

## Graph database
- uses graph structures for semantic queries with nodes, edges, and properties to represent and store data
- graph relates the data items in the store to a collection of nodes and edges, the edges representing the relationships between the nodes

## Document Store (document-oriented database)
- designed to manage and query data in a flexible, semi-structured format
- typically use formats like JSON, BSON, or XML
- can contain nested structures, lists, and varied types of data, offering greater flexibility compared to traditional row-column databases

## Standard Column Family
- object that contains columns of related data

## Super Column Family
- has a set of super columns, each containing its own set of columns
- creates a multi-level nesting where each super column acts like a primary key for its inner columns

## Time Series Database (TSDB)
- designed to handle data organized by time, with each data point typically associated with a timestamp
- optimized for high insert rates

## Other types

- Key–value cache
- Key–value store (eventually consistent)
- Key–value store (ordered)
- Tuple store
- Triplestore
- Object database
- Native multi-model database
- Multivalue database



Persistent data structure: always preserves the previous version of itself when it is modified. Effectively immutable; always yield a new updated structure.
	- Techniques 
		- Copy-on-write
		- Fat node
		- Path copying



## Keyspace (distributed data store)
- a top-level container/namespace in a distributed data store. 
- serves as a namespace and organizational boundary for related data, similar to a database in a relational database management system (RDBMS)
- helps organize your data
- defines replication and consistency strategies
- sets boundaries for access control and security






### 2-element tuple (pair):
- aka "pair." ex: (1, "apple")

### 3-element tuple (triple):
- aka "triple" ex: (1, "apple", 3.14)

### 4-element tuple:
- no special name. Ex.: (1, "apple", 3.14, True)






## Types of NoSQL


## Fundamental features

















# list of NoSQL Products
- Aerospike (database)
- Amazon DynamoDB
- Apache Accumulo
- Apache Cassandra
- Apache Druid
- Apache HBase
- Apache Solr
- ArangoDB
- Basho Technologies
- Berkeley DB
- Clusterpoint
- Column (data store)
- Column family
- Compose.io
- Cosmos DB
- Couchbase Server
- Couchbase, Inc.
- Apache CouchDB
- Cypher (query language)
- DataStax
- Datomic
- Db4o
- Dynamo (storage system)
- Fluidinfo
- FoundationDB
- Hibari (database)
- DBOMP
- IBM Information Management System
- HCL Notes
- JanusGraph
- Keyspace (distributed data store)
- LevelDB
- Lightning Memory-Mapped Database
- MarkLogic Server
- MLab
- MongoDB
- Multi-model database
- MultiValue database
- Neo4j
- NoSQLz
- ObjectDB
- Ontotext GraphDB
- Oracle NoSQL Database
- Ordered Key-Value Store
- OrientDB
- Qizx
- Rasdaman
- RavenDB
- Redis
- RethinkDB
- Riak
- Rocket U2
- RocksDB
- SciDB
- ScyllaDB
- SequoiaDB
- Standard column family
- Super column family
- Tarantool
- TerminusDB
- Valkey
- Virtuoso Universal Server
- Voldemort (distributed data store)
- Wide-column store
- WiredTiger
- Xeround