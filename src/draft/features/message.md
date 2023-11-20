# Message Feature

The message [feature] is the most commonly used feature.
Messages are the way that peers communicate with each other over the network.

[feature]: index.md

~~~admonish abstract title="Terminology"
- A *message type* is an instance of the message feature.
- A *message* is an instance of a message type.
~~~

All message types have a direction that indicates which way the message can be sent:
- `Clientbound` => Messages sent from the server to the client
- `Serverbound` => Messages sent from the client to the server
- `Bi-Directional` => Messages can that originate from either the client or the server


### Codec

When messages are sent on the wire, they are encoded by first writing the message id, then the message content.

~~~admonish tip
Inertya [defines] many message types.

[defines]: ../typedefs/messages.md
~~~
