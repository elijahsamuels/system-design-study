# Chapter 8 - KEY-VALUE DATABASES

Primarily used when all access to the database is via primar key

Simplest NoSQL data stores to to from an API perspective.
- value is a blob

Popular NoSQL databases:
- Redis
- Riak
- Memcached
- HamsterDB
- AWS DynamoDB (not open-source)
- Project Voldemort (open source version of DynamoDB)

Buckets store specific data.
Domain buckets allowing the serialization and deserialization to be handled by the client driver.

## Key-Value Store Features
### Consistency
	- only applicable to single key
	- use eventual consistency
	- buckets are just a way to namespacekeys so that key collisons can be reduced

### Transactions
	- no gaurantees on writes
	- Riak allows transactions via "Quorums"

### Query Features
  - All key-value stores can query by the key
  - most do not provide a list of the keys, so you can't walk the list of keys
  - "Riak Search" - allows you to query the data simliar to querying using Lucene indexes

### Struture of Data
	- Key-value databases don't care what is stored in the value

### Scaling
	- many key-value stores scale by using sharding
  	- the value of the key determines on which node the key stored

## Suitable Use Cases
	- web sessions / using session IDs
	- storing user preferences, userIDs, etc...
	- product profiles
	- shopping carts tied to a user

## When Not to Use

	- if you have have relationships betwen different sets of data
	- saving multiple keys and there is a failture ot save any on of them, and you want to revert or roll back the operations
	- search the keys based on something found in the value part of the key-value pairs
