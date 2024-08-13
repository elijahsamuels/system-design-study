# Chater 1 - Software Engineering at Google

- Hyrum’s Law: with a sufficient number of users of an API, it does not matter
  what you promise in the contract: all observable behaviors of your system will be
  depended on by somebody.

- “Because I said so” is a terrible reason to do things.

### Policies That Don’t Scale

- **Churn Rule** - infrastructure teams must do the work to move their internal users to new versions themselves or do the update in place, in backward-compatible fashion.

Development branches: Using separate dev branches for every team or feature can lead to scaling problems as the organization grows. This approach can result in an ever-increasing amount of overhead work, such as resyncing and testing.

### Policies That Scale Well

- **The Beyoncé Rule** - If you liked it, you should have put a CI test on it

- Knowledge is viral, experts are carriers

### Shifting Left

finding and fixing problems earlier in the developer workflow to reduce costs

- Cost reduction: Fixing problems early on reduces the cost of resolving them.
- Security benefits: Catching security issues before deployment can save a lot of work and money.
- Developer efficiency: Fixing issues before code is committed to version control saves time and effort for developers.

### Trade-offs and Costs

trade-offs and costs, which go beyond just financial expenses.

- Types of costs: financial, resources, personnel, transactions, opportunity, and societal.
- Societal costs: Large tech companies like Google have a significant impact on society, and ignoring societal costs can lead to negative consequences.
- Biases: Decision-makers should be aware of their own biases, such as status quo bias and loss aversion.
- Personnel cost: In software engineering, personnel cost (i.e., the cost of keeping engineers happy, focused, and engaged) is often a significant factor in decision-making.

- Consensus is key: Good decisions are made through consensus, not unanimity.
- Reasoning is essential: Every decision should have a clear reason behind it, and "because I said so" or "because everyone else does it this way" are not valid reasons.
- Efficiency gains matter: Small improvements in efficiency can add up to significant benefits over time.

### Software Engineering vs Programming

- represent two different problem domains with distinct constraints, values, and
  best practices

- management of code over time, the impact of time on scale, and decision making in
  the face of those ideas.
- **Programming** - the immediate act of producing code.
- **Software engineering** - the set of policies, practices, and tools necessary to make
  that code useful for as long as it needs to be used
