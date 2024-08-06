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

## Transactions

## Availability

## Query Features

- it is advised to make the cloumns and column families optimized for reading the data since it doesn't have a rich query language.

## Suitable Use Cases

- Event logging, content management systsm, blogging platforms, counters, expiring usages.

## When to Avoid

- not great for ACID transactions for writes and reads, aggregate data (SUM, AVG) (this has to be done on client side)
- early prototypes where queries will change
