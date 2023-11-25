# Networking

The specific networking protocol used for sessions is left up to the PV.

[Queries](queries.md) always use TCP.


## Magic Bytes

All connections (session and query) start with the client sending the magic 
bytes, `0x4E52` ('NR' in ASCII). This makes sure that the client and the 
server are on the same page, ie. this is inertya.

### Mode Indicators
The next byte sent is a mode indicator, telling the server if this is a 
query or a session.

- `0x51` ('Q' in ASCII): Indicates that this connection is a [query](queries.md).
- `0x53` ('S' in ASCII): Indicates that this connection is a session.


