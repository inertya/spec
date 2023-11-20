# Keys

A *key* is a namespaced resource identifier of the form `namespace:value`.

Keys have 2 parts, the *namespace* and the *value*.
They are seperated by a colon (`:`).

Each part is between 1-16 characters long, and consists of `a-z`, `0-9`, and `_`.

~~~admonish info title="Reserved Namespaces"
Do not use the following namespaces:

- `inertya` (used for inertya defined resources)
- `example` (used for examples)
- `test` (used for testing)
- `debug`
- `nr`
- `core`
- `std`
- `stdlib`
- `root`
- `key`
- `plugin`
- `mod`
- `server`
- `client`
- `env`
- `id`
- `namespace`
- `template`
- `_`

Additionally, do not use keys that only consist of underscores.
~~~


### Codec
Keys are encoded similar to strings by first writing the length as a single byte, then writing the raw string bytes.

~~~admonish example title="Examples"
- `inertya:key` => `0B 69 6E 65 72 74 79 61 3A 6B 65 79`
- `a:b` => `03 61 3A 62`
~~~

~~~admonish tip title="Custom Data Feature Type"
Keys have [custom data] feature type id [`inertya:key`].

[custom data]: features/custom-data.md
[`inertya:key`]: typedefs/custom-data/key.md
~~~

