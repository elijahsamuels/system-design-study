# Column-Family Stores

- Popular document databases: Cassandra, HBase, Hypertable, Amazon SimpleDB

| RDBMS                      | Cassandra                         |
| -------------------------- | --------------------------------- |
| database instances         | cluster                           |
| database                   | keyspace                          |
| table                      | column family                     |
| row                        | row                               |
| column (same for all rows) | column (can be different per row) |

- Column-Family databases store data in column familes as rows that have many columans associated with a row key.

| **Row Key** | **Column Family (Column Names)** | **Values**          |
| ----------- | -------------------------------- | ------------------- |
| `user123`   | `name`                           | `Alice`             |
|             | `email`                          | `alice@example.com` |
|             | `age`                            | `30`                |
| `user456`   | `name`                           | `Bob`               |
|             | `email`                          | `bob@example.com`   |
|             | `address`                        | `123 1st St.`       |

## Features

- basic unit of storage is a column
- each column consists of a name-value pair where the name also behaves as the key.
- each name-value pair is a single column and is alaways stored with a timestamp value
- the timestampe is used to expire data, resolve write conflicts, deal with stale, and do other things.

```
{
  name: "firstName",
  value: "Alice",
  timestamp: 1234567890,
}
```

**Super column** - consists of a name and a value which is a map of columns

```
{
  name: "book:123456",
  value: {
	author: "JR Tolkien",
	title: "The Hobbit",
	isbn: "978-0345391802",
  }
}
```

**Super Column family** - consists of a name and a map of super columns.

## Consistency

- When a write is received by Cassandra, the data is first recorded in a commit log, then written to an in-memory structure known as memtable. A write operation is considered successful once it’s written to the commit log and the memtable. Writes are batched in memory and periodically written out to structures known as SSTable. SSTables are not written to again after they are flushed; if there are changes to the data, a new SSTable is written. Unused SSTables are reclaimed by compactation.
- If the data is stale, subsequent reads will get the latest (newest) data; this process is known as read repair. The low consistency level is good to use when you do not care if you get stale data and/or if you have high read performance requirements.
- During write operations, theQUORUM consistencysettingmeansthatthewritehastopropagatetothe majority of the nodes before it is considered successful and the client is notified.
- While a node is down, the data that was supposed to be stored by that node is handed off to other nodes. As the node comes back online, the changes made to the data are handed back to the node. This technique is known as hinted handoff. Hinted handoff allows for faster restore of failed nodes.

## Transactions

- atomic at row level
- Writes are first written to commit logs and memtables, and are only considered good when the write to commit log and memtable was successful

## Availability

- highly available

## Scaling

- Scaling an existing cluster is a matter of adding more nodes
-

## Query Features

- it is advised to make the cloumns and column families optimized for reading the data since it doesn't have a rich query language.

## Suitable Use Cases

- Event logging, content management systsm, blogging platforms, counters, expiring usages.

## When to Avoid

- not great for ACID transactions for writes and reads, aggregate data (SUM, AVG) (this has to be done on client side)
- early prototypes where queries will change
