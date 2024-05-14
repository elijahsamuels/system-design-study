data model can mean:
- the model of the specific data in an application
- an entity-relationship diagram of their database and refer to that as their data model
- the model by which the database organizes data (formally called a metamodel)

Four categories
- key-value
- document
- column-family
- graph

key-value, document, column-family are all aggregate-orientation data models
graph is aggregate-ignorant

Aggregate is  aterm that comes from Domain-Driven Design. 
Aggregate - a collection of related objects treated as a unit

Relational databases have no concept of aggregate within their data model (aggregate-ignorant)

ACID transactions: 
- Atomic
- Consistent
- Isolated
- Durable

Atomicity - Many rows spanning many tables are updated as a single operation. This operation either succeeds or fails in its entirety, and concurrent operations are isolated from each other so they cannot see a partial update


### key-value database
- the aggregate is opaque to the database 
- we can store whatever we like in the aggregate. 
- may impose some general size limit, but other than that we have complete freedom. 
- look up aggregates using a key

### document database
- a structure in the aggregate
- imposes limits on what we can place in it, defining allowable structures and types
- submit some form of a query based on the internal structure of the document
- submit queries to the database based on the fields in the aggregate, we can retrieve part of the aggregate rather than the whole thing, and database can create indexes based on the contents of the aggregate

### Column-Family Stores
- a two-level aggregate structure
	- first row: a map of more detailed values. 
	- second row: values are referred to as columns
- column family defines a record type, each row is a record, and each column is a field.
- Skinny rows - few columns with the same columns used across the many different rows
- Wide row - many columns (perhaps thousands), with rows having very different columns. 
- Wide column - each column being one element in that list.

![Column-Family Structure](<images/column-family-structure.png>)
