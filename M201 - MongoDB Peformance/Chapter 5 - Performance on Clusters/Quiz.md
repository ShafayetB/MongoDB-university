# Quiz

## Performance Considerations in Distributed Systems Part 2

**Problem:**

From a performance standpoint, when working with a distributed database it's important to consider...

- [ ] Reading from secondaries only
- [x] **Routed Queries**
- [x] **Latency**

## Increasing Write Performance with Sharding Part 2

**Problem:**

Which of the following is/are true?

- [ ] Vertical scaling is generally cheaper than horizontal scaling.
- [x] **Picking a good shard key is one of the most important parts of sharding.**
- [ ] Ordered bulk operations are faster than unordered.

## Reading from Secondaries

**Problem:**

When should you ever read from secondaries?

- [ ] To increase performance in a write-heavy system.
- [x] **When doing ad-hoc queries and analytic jobs.**
- [x] **To provide reads with lower latency.**


**Problem:**

Should you ever read from secondaries on a sharded cluster?

- **Select this answer and read the detailed answer section for more information.**

## Replica Sets with Differing Indexes Part 3

**Problem:**

Which of the following conditions apply when creating indexes on secondaries?

- [x] **A secondary should never be allowed to become primary**
- [ ] These indexes can only be set on secondary nodes
- [ ] We can create specific indexes on secondaries, even if they are not running in standalone mode

## Aggregation Pipeline on a Sharded Cluster

**Problem:**

What operators will cause a merge stage on the primary shard for a database?

- [x] **$out**
- [ ] $group
- [x] **$lookup**
