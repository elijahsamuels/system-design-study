# Chapter 13. Polyglot Persistence

- the idea that applications should be written in a mix of languages to take advantage ofthe fact that different languages are suitable for tackling different problems

- service wrapping of different databases. basically, create a microservice that communicates with a different database type

Some NoSQL data store products, such as Riak and Neo4J,actually provide out-of-the-box REST API’s

Extract, transform, and load (ETL) is the process of combining data from multiple sources into a large, central repository called a data warehouse.

with Polyglot Persistence, deployment complexity increases
application now needs alldatabases in production at the same time.
You will need to have these databases in your Stage, QA, and Dev environments.
