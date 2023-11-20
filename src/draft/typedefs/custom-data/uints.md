# `inertya:uint{8,16,32,64}`

Inertya defines 4 fixed-width unsigned integer [custom data types]:

[custom data types]: ../../features/custom-data.md

| ID               | Size          | Minimum Value | Maximum Value |
|------------------|---------------|---------------|---------------|
| `inertya:uint8`  | 8-bit/1-byte  | 0             | 2^8^-1        |
| `inertya:uint16` | 16-bit/2-byte | 0             | 2^16^-1       |
| `inertya:uint32` | 32-bit/4-byte | 0             | 2^32^-1       |
| `inertya:uint64` | 64-bit/8-byte | 0             | 2^64^-1       |

See also: the [signed](ints.md) integer types.


## Codec

Integers are encoded little endian and full/fixed width.

### Errors { #codec-errors }

None (all values are valid for these types)
