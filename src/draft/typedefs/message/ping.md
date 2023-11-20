# `inertya:ping`
> Direction: Bi-Directional

Sent by the server every second to ensure connection liveness and calculate ping.
The client should respond immediately.

| Type       | Name    | Description                                                                                                                                  |
|------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [`uint64`] | `nonce` | A nonce. Has no inherent meaning. Must be unique across this session.<br>Clients must use the same nonce when replying to the server’s ping. |

[`uint64`]: ../custom-data/uints.md

~~~admonish note
2<sup>64</sup> seconds is [~42 times][math :D] the age of the universe, so running out of nonces is practically impossible.

[math :D]: https://www.wolframalpha.com/input?i=2%5E64+seconds+to+years
~~~

~~~admonish tip title="Server Implementations"
This must be scheduled to be sent every 1s.

It is recommended that servers implement this with an incremental counter.
~~~
