# `inertya:string`

The `inertya:string` [custom data type] is a variable length UTF-8 string.

The maximum length of any string is 2<sup>24</sup> (16,777,216) bytes.

[custom data type]: ../../features/custom-data.md


### Codec

The string type is encoded as an unsigned [varint] length and then the raw bytes.

[varint]: ../../concepts/varint.md

~~~admonish example title="Examples"
`"Hello" => 05 48 65 6C 6C 6F`

`"" => 00` (empty string)
~~~

~~~admonish error title="Errors" id="codec-errors"
- Length [varint errors]
- Invalid UTF-8 bytes
- Length greater than 16,777,216

[varint errors]: ../../concepts/varint.md#errors
~~~
