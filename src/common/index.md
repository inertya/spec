---
nav:
  - versioning.md
  - networking.md
  - queries.md
---

# Inertya Common Protocol

The inertya common protocol provides a ~~minimum stable interface~~, and 
consists of two main things:
1. A versioning system (Protocol Versions), to allow the protocol to evolve 
with breaking changes
2. A query system, to enable checking of the server's protocol version (and 
other statuses).

Concepts in the common protocol are considered *protocol version independent*.

The common protocol does not change, to ensure that all past, present, and 
future protocol version can co-exist.
