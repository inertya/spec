# `inertya:login` &nbsp; <small>(Serverbound)</small>

Sent by the client after the hellos to set its username.

| Type            | Name          | Description                                                                                             |
|-----------------|---------------|---------------------------------------------------------------------------------------------------------|
| [`string`]      | `username`    | The client's chosen [username]. Length between 2-16, and can only contain `a-z`, `A-Z`, `0-9`, `-`, `_` |

[`string`]: ../custom-data/string.md
[username]: ../../players.md#usernames
