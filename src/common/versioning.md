# Versioning

To allow the protocol to evolve with breaking changes, it is versioned.

Every protocol version is *fully incompatible* with every other protocol 
version.

The protocol is versioned with a single number, the protocol version number.
This number is an unsigned 32-bit/4-byte integer.

### Terminology

PV
: Protocol Version

PVN
: Protocol Version Number

pv{x}
: Protocol Version {x}.  
eg. pv12 is protocol version 12.

pvTEST
: The testing protocol version (`0xFFFFFFFF`)


### Special PVNs

`0x00000000`
: Used for [queries]. Not a valid PVN.

`0xFFFFFFFF` (pvTEST)
: Used for testing, snapshots, and drafts. Not stable.

[queries]: querying.md

