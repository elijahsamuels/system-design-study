Instead of trying to memorize all the features of various relational database service (RDS) (~60), it's probably better to learn about what features a RDS can offer (or can't offer).

## Things to consider:
- what operating systems can it run on? 
	ex. MySQL and PostgreSQL can run on Windows, macOS, Linux, BSD, UNIX, AmigaOS, z/OS, and Android, but EXASolution ONLY runs on Linux.
	Most will run on Windows > Linux > UNIX > macOS

## Fundamental features
- ACID (atomicity, consistency, isolation, durability)
	- atomicity: guarantees that each transaction is treated as a single "unit", which either succeeds completely or fails completely: if any of the statements constituting a transaction fails to complete, the entire transaction fails and the database is left unchanged
	- consistency: ensures that a transaction can only bring the database from one consistent state to another, preserving database invariants: any data written to the database must be valid according to all defined rules
	- isolation: ensures that concurrent execution of transactions leaves the database in the same state that would have been obtained if the transactions were executed sequentially
	- durability: guarantees that once a transaction has been committed, it will remain committed even in the case of a system failure
- Referential integrity: property of data stating that all its references are valid (ex. a foriegn key cannot point to a primary key that doesn't exist.)
- Transactions: symbolizes a unit of work, performed within a database management system (or similar system) against a database, that is treated in a coherent and reliable way independent of other transactions. Allow correct recovery from failures and keep a database consistent even in cases of system failure. Provide isolation between programs accessing a database concurrently
- Fine-grained locking: a synchronization primitive that prevents state from being modified or accessed by multiple threads of execution at once. A locking strategy in which locks are applied at a more granular level, allowing greater flexibility and concurrency in database operations. Fine-grained locking lets you lock smaller sections, such as specific rows, columns, or even individual data items.
- Multiversion concurrency control (MVCC): point-in-time consistent views, usually from a timestamp or transaction ID. New data will not overwrite the original data item, but instead creates a newer version of the data item. Thus there are multiple versions stored.
- Unicode: does the database use unicode? Most do. Unicode is the standardization of characters, (numerals, punctuation, etc...)
- Interface: SQL, API, GUI, are most commmon, but a database might not have all three.
- Type inference: most do this

## Limits (size)
- Max DB size
- Max table size
- Max row size
- Max columns per row
- Max Blob/Clob size
- Max CHAR size
- Max NUMBER size
- Min DATE value
- Max DATE value
- Max column name size

## Indexes
- R-/R+ tree (rectangle tree, rectangle tree)
- Hash
- Expression
- Partial
- Reverse
- Bitmap
- GiST (Generalized Search Tree)
- GIN (Generalized Inverted Index)
- Full-text
- Spatial
- FOT (Field-Oriented Table)
- Duplicate index prevention

## Database capabilities
- Union
- Intersect
- Except
- Inner joins
- Outer joins
- Inner selects
- Merge joins
- Blobs and clobs
- Common table expressions
- Windowing functions
- Parallel query
- System-versioned tables

## Data types
- Type system
- Integer
- Floating point
- Decimal
- String
- Binary
- Date/Time
- Boolean
- Other (ENUM, SET, GIS data types, XML, JSON, and tons more.. ).

## Other objects
- Data Domain
- Cursor
- Trigger
- Function (internal routines written in SQL and/or procedural language like PL/SQL)
- Procedure (internal routines written in SQL and/or procedural language like PL/SQL)
- External routine

## Partitioning
- Range (zipcodes: 90000-99999)
- Hash (states: California, Oregon, Washington)
- Composite (Range+Hash) (California && 90000-94999)
- List (A table called orders with a region column indicating the geographical region where an order was placed. Partition this table by 'region')
- Expression (Divides a table into partitions based on a custom expression.)
- Round Robin (each partition takes a turn getting new data. dataA -> partition1, dataB -> partition2, etc... )

## Access control
- Native network encryption
- Brute-force protection
- Enterprise directory compatibility
- Password complexity rules
- Patch access
- Run unprivileged
- Audit
- Resource limit
- Separation of duties (RBAC)
- Security Certification
- Attribute-Based Access Control (ABAC)