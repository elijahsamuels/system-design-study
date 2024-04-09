# Chapter 5 - Dig for Architecturally Significant Requirements

ASR - architecturally significant requirement
- any requirement that strongly influences our choice of structures for the architecture


**Constraints** - Unchangeable design decisions, usually given, sometimes chosen.

**Quality** - Attributes Externally visible properties that characterize how the system operates in a specific context.

**Influential Functional Requirements** - Features and functions that require special attention in the architecture.

**Other Influencers** - Time, knowledge, experience, skills, office politics, your own geeky biases, and all the other stuff that sways your decision making.

![6 parts of a quality attribute](<images/6 parts of a quality attribute.png>)


# Chapter 6 - Choose an Architecture (Before It Chooses You)

![Diverge to See Options, Converge to Decide](<images/Diverge to See Options, Converge to Decide.png>)

**decision matrix** - tool for summarizing the trade-off analysis among architecture design options
![decision matrix](<images/decision matrix.png>)

To use a decision matrix, list properties you plan to use for the analysis in the first column of a table. Each row represents a particular property. Each column represents your analysis of a design option.

## Decision Matrix Example
![Decision Matrix Example](<images/Decision Matrix Example.png>)



# Chapter 7 - Create a Foundation with Patterns

**architecture pattern** - a reusable solution to a specific problem

**Layers Pattern** - Partitioning code into distinct and independent layers organized around a specific set of related concerns

![Layers Pattern Examples](<images/Layers Pattern Examples.png>)


**Ports and Adapters Pattern** - isolates core business logic so it can be used in a variety of contexts and tested in isolation from components that provide data and events

![Ports and Adapters Example](<images/Ports and Adapters Example.png>)

**Pipe-and-Filter Pattern** - each component called a filter is responsible for a single transformation or data operation. Data is streamed from one filter to the next as quickly as possible, and data operations occur in parallel. Loosely coupled filters can be reused and combined in different ways to create new pipelines

![Pipe-and-Filter Example](<images/Pipe-and-Filter Example.png>)

**batch sequential pattern** - similar to pipe-and-filter. Stages of a batch-sequential system operate in turn, one at a time instead of in parallel like in a pipe-and-filter system


**Service-Oriented Architecture Pattern** - independent components are implemented as services, which provide specific functionality


![Service-Oriented Architecture Example](<images/Service-Oriented Architecture Example.png>)


**Publish-Subscribe Pattern** - producers and consumers exist independently and unaware of one another. Consumers subscribe to events published by producers

![Publish-Subscribe Example](<images/Publish-Subscribe Example.png>)


**Shared-Data Pattern** - multiple components access data through a common data store. No single component is entirely responsible for the data or data store

![Shared-Data Pattern Example](<images/Shared-Data Pattern Example.png>)

**Multi-Tier Pattern** - runtime structures are organized into logical groups. These logical groups may be allocated to specific physical components, such as a server or cloud platform. similar to the layers pattern

![Multi-Tier Example](<images/Multi-Tier Example.png>)

**Center of Competence Pattern (CoC)** - a team of experts is charged with defining patterns, establishing best practices, developing support tools, and providing education for a subset of the architecture

![CoC Example](<images/CoC Example.png>)


**Open Source Contribution Pattern** - teams are given responsibility for developing specific architectural components but are not expected to be the only contributing developers. For this pattern to be successful, teams must know they are responsible for specific components and have a firm understanding of where their components fit within the larger context

**Big Ball of Mud Pattern** - no defined elements or relations











**Architectural mismatch** - occurs when the assumptions made about how a component will be used conflicts with that component’s current use