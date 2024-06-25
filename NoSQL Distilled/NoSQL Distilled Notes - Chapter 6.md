# Version Stamps
- avoid update conflicts
- also useful for providing session consistency
- detect concurrency conflicts. When you read data, then update it, you can check the version stamp to ensure nobody updated the data between your read and write


- aggregate-oriented NoSQL databases do support atomic updates within an aggregate

**Optimistic Offline Lock** - a form of conditional update where a client operation rereads any information that the business transaction relies on and checks that it hasn’t changed since it was originally read and displayed to the user

**version stamp** - a field that changes every time the underlying data in the record changes

**CAS** - compare-and-set operation

Four common ways to construct version stamps

1. counter

2. create a GUID, a large random number that’s guaranteed to be unique
	- never duplicated
	- large, and can't compare recentness

3. hash of the contents of the resource
	- deterministic
	- can’t be directly compared for recentness
	- can be lengthy

4. timestamp of the last update
	- Multiple machines can generate timestamps
	- clocks must be kept in sync

## Vector Stamps

- **vector stamp** - a set of counters, one for each node
	- `[blue: 43, green: 54, black: 12]`

**vector clocks** and **version vectors** - specific forms of vector stamps that differ in how they synchronize
