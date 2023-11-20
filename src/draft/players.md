# Players

Players (clients) are 


### Usernames
All players have a username.
Usernames are between 2-16 characters long (inclusive) and can only contain
`a-z`, `A-Z`, `0-9`, `-`, `_`.

Username Regex: `^[a-zA-Z0-9-_]{2,16}$` ([view on regex101][regex])

The client chooses it's and sends to the server in the [`inertya:login`][login]
packet.

[regex]: https://regex101.com/?regex=^[a-zA-Z0-9-_]{2,16}$&testString=Sky9
[login]: typedefs/message/login.md
