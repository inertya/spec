# `inertya:hello` &nbsp; <small>(Bi-Directional)</small>

This is the first message sent on the connection after it is established.

| Type            | Name          | Description                                                                                    |
|-----------------|---------------|------------------------------------------------------------------------------------------------|
| [`string`]      | `impl_name`   | The name and version of the library implementing inertya’s protocol (similar to a user agent). |
| [`string`]      | `brand_name`  | The name and version of the application.                                                       |
| [`plugin_hash`] | `plugin_hash` | The hash of the plugin set installed on the peer.                                              |

[`string`]: ../custom-data/string.md
[`plugin_hash`]: ../../plugins/hashes.md
