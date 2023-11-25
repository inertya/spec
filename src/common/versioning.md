# Versioning

To allow the protocol to evolve with breaking changes, it is versioned.

Every protocol version is **fully incompatible** with every other protocol 
version.

The protocol is versioned with a single number, the protocol version number.
This number is an unsigned 32-bit/4-byte integer.

For a full list of all released protocol versions, see the
[version history](../versions.md).

### Terminology

PV
: Protocol Version

PVN
: Protocol Version Number

pv{x}
: Protocol Version {x}.  
eg. pv12 is protocol version 12.

pvTEST
: The testing protocol version (`0x00000000`).


### Special PVNs

`0x00000000` - pvTEST
: Used for testing, snapshots, and drafts. Not stable.
