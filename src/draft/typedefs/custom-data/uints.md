# `inertya:uint{8,16,32,64}`

Inertya defines 4 fixed-width unsigned integer [custom data types]:

[custom data types]: ../../features/custom-data.md

| Key              | Size          | Minimum Value | Maximum Value    |
|------------------|---------------|---------------|------------------|
| `inertya:uint8`  | 8-bit/1-byte  | 0             | 2<sup>8</sup>-1  |
| `inertya:uint16` | 16-bit/2-byte | 0             | 2<sup>16</sup>-1 |
| `inertya:uint32` | 32-bit/4-byte | 0             | 2<sup>32</sup>-1 |
| `inertya:uint64` | 64-bit/8-byte | 0             | 2<sup>64</sup>-1 |

See also: the [signed](ints.md) integer types.


### Codec

Integers are encoded *little* endian and full/fixed width.

~~~admonish error title="Errors" id="codec-errors"
None (all values are valid for these types)
~~~
