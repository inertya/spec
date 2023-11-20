# `inertya:int{8,16,32,64}`

Inertya defines 4 fixed-width signed integer [custom data types]:

[custom data types]: ../../features/custom-data.md

| ID              | Size          | Minimum Value   | Maximum Value    |
|-----------------|---------------|-----------------|------------------|
| `inertya:int8`  | 8-bit/1-byte  | -2<sup>7</sup>  | 2<sup>7</sup>-1  |
| `inertya:int16` | 16-bit/2-byte | -2<sup>15</sup> | 2<sup>15</sup>-1 |
| `inertya:int32` | 32-bit/4-byte | -2<sup>31</sup> | 2<sup>31</sup>-1 |
| `inertya:int64` | 64-bit/8-byte | -2<sup>63</sup> | 2<sup>63</sup>-1 |

See also: the [unsigned](uints.md) integer types.


### Codec

Integers are encoded *little* endian and full/fixed width.

Signed integers are encoded with [two's complement].

[two's complement]: https://en.wikipedia.org/wiki/Two%27s_complement

~~~admonish error title="Errors" id="codec-errors"
None (all values are valid for these types)
~~~
