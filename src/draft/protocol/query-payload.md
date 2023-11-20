# Query Payload

This is the payload returned during [queries] to a server with this PV.

The query payload is a [JSON] object.

If the type ends with a question mark `?`, the field is optional and may be missing or null.

[queries]: ../../protocol/queries.md
[JSON]: https://www.json.org/json-en.html

#### Root

| Name             | Type      | Description                                                                                    |
|------------------|-----------|------------------------------------------------------------------------------------------------|
| `impl_name`      | `string`  | The name and version of the library implementing inertya’s protocol (similar to a user agent). |
| `brand_name`     | `string`  | The name and version of the application.                                                       |
| `name`           | `string`  | The server's name.                                                                             |
| `description`    | `string`  | The server's description.                                                                      |
| `motd`           | `string`  | The server's MOTD (message of the day). One line only.                                         |
| `online_players` | `uint?`   | The number of players currently online.                                                        |
| `max_players`    | `uint?`   | The maximum number of players that can be online at one time.                                  |
| `plugin_hash`    | `string`  | The [hash](../plugins/hashes.md) of the plugin set.                                            |
| `plugins`        | `array`   | An array of [plugin objects](#plugin-type) (see below)                                         |
| `icon`           | `string?` | A base64 encoded png image. Must be exactly 64x64 pixels, or it will not be displayed.         |                                                                                             |

~~~admonish help title="Description vs. MOTD"
The difference between `description` and `motd` is that description can be multiple lines and changes less often, while the motd can change frequently and is only one line.
~~~

#### Plugin Type

This is the type of the element in the `plugins` array.

| Name       | Type      | Description                                                                                       |
|------------|-----------|---------------------------------------------------------------------------------------------------|
| `id`       | `string`  | The [id](../plugins/index.md) of this plugin.                                                     |
| `name`     | `string`  | A friendly name for this plugin.                                                                  |
| `version`  | `string`  | A `major.minor` semver for this plugin. See [Plugins#versioning](../plugins/index.md#versioning). |
| `authors`  | `array?`  | A list of strings representing the authors of this plugin. One element per author.                |
| `homepage` | `string?` | A URL to a homepage for this plugin. Can also point to a repository or documentation.             |
| `required` | `bool`    | If clients must install this plugin before connecting. If so, versions must match exactly.        |


~~~admonish help title="Authors Field"
The optional `authors` field lists in an array the people or organizations that are considered the “authors” of the package.
The exact meaning is open to interpretation — it may list the original or primary authors, current maintainers, or owners of the package.
An optional email address may be included within angled brackets at the end of each author entry.<br>
<small>(description taken from the [Cargo book](https://doc.rust-lang.org/1.73.0/cargo/reference/manifest.html#the-authors-field))</small>
<!-- last updated: Nov 9, 2023 | last commit to source file: bfb5d1d -->

Example: `["John Doe", "Sky <sky@sky9.dev>"]`
~~~

<hr>

~~~admonish tip title="Design Suggestions"
#### Name/MOTD {#design-suggestion-name-motd}
The name and MOTD should generally be kept together, and the MOTD should generally be placed under the name.

#### MOTD/Description {#design-suggestion-motd-description}
The server's name and motd should be directly displayed on a server list, while the description can be relegated to either a server page or a hover.
~~~

~~~admonish caution title="Recoverable Errors/Optional Data" id="recoverable-errors-and-optional-data"
#### Player Counts {#missing-player-counts}
If online players is null, nothing should be displayed.

If only online players is present, display `<online>`.

If both are present, display `<online>/<max>`

#### Icons {#missing-icons}
Implementations may choose what to display if the icon is missing, null, or invalid (invalid png, not 64x64, etc).

Omitting the icon entirely is the suggested behavior.

#### Multiline MOTDs {#error-multiline-motds}
If the MOTD has multiple lines, everything after the first newline should be ignored.
~~~

~~~admonish error title="Errors"
- Not valid JSON
- JSON not conforming to payload format

Implementations should just display some kind of "Invalid Query Payload Response" error when this happens.
~~~
