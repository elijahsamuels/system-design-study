# Chapter 14. Beyond NoSQL

## File Systems

**File Systems vs. Databases**: File systems are simple and effective for storing large files and handling sequential access but are less efficient for managing many small files and lack native query support. They are often used in conjunction with databases for indexing and additional functionality.

**Distributed File Systems**: Technologies like Google File System and Hadoop have evolved to support large-scale file processing and replication in clustered environments, facilitating efficient data manipulation and often serving as a precursor to NoSQL solutions.

## Event Sourcing

- **Event Persistence and State Reconstruction**: Event sourcing focuses on storing all changes to the application's state as discrete events in an event log, rather than storing the current state directly. This allows the system's state to be rebuilt at any time by replaying these events.

- **Snapshots for Efficiency**: Although the event log can theoretically recreate the entire application state, it may be inefficient. To optimize recovery, snapshots of the application state are taken periodically. These snapshots help speed up state reconstruction by reducing the number of events that need to be replayed.

- **Advantages and Challenges**: Event sourcing allows for flexible state analysis and system scalability by broadcasting events to multiple systems and supporting various read models. However, it adds complexity, requiring careful management of event capture and consideration of external system interactions to avoid issues during state reconstruction.

## Memory Image

- **Performance and Simplification**: With event sourcing, the event log serves as the persistent record, allowing the application state to be kept entirely in memory. This improves performance by avoiding disk I/O and simplifies programming by eliminating the need for mapping between disk and in-memory data structures.

- **Limitations and Challenges**: Storing all data in memory requires sufficient memory capacity and effective crash recovery mechanisms, such as reloading from the event log or using redundant systems. Additionally, managing concurrency and handling errors becomes more complex, often requiring careful design or custom solutions.

## Version Control

git

## XML Databases

## Object Databases
