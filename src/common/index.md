---
nav:
  - versioning.md
  - networking.md
  - queries.md
---

# Inertya Common Protocol

The inertya common protocol provides two main things:
1. A [versioning] system (Protocol Versions), to allow the protocol to evolve 
with breaking changes, and
2. A [query][queries] system, to enable checking of the server's protocol 
version (and other statuses).

Concepts in the common protocol are considered *protocol version independent*.

The common protocol does not have breaking changes (minor additions may 
happen, like the planned protocol version ranges), to ensure that all 
protocol versions can co-exist.

[versioning]: versioning.md
[queries]: queries.md
