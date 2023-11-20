# `inertya:string`

The `inertya:string` [custom data type] is a variable length UTF-8 string.

The maximum length of any string is 2<sup>24</sup> (16,777,216) bytes.

[custom data type]: ../../features/custom-data.md


## Codec

The string type is encoded as a [uint32] length and then the raw bytes.

[uint32]: uints.md

### Errors { #codec-errors }

- Invalid UTF-8
- Length greater than 16,777,216
