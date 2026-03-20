# SERVER SETTINGS

[Enshrouded Server](./README.md) > Server Settings

Server settings refer to settings which affect communication between the host computer/server and Enshrouded services.

> [!TIP]
Be a decent person, **don't use offensive language**.

---

## Contents

- [SERVER SETTINGS](#server-settings)
  - [Contents](#contents)
  - [Settings Table](#settings-table)
  - [Additional Information](#additional-information)
    - [`tags` Details](#tags-details)
      - [Allowed Tags](#allowed-tags)
      - [tags Examples](#tags-examples)
        - [All tags on one line](#all-tags-on-one-line)
        - [One tag per line](#one-tag-per-line)
    - [`gameSettingsPreset` Details](#gamesettingspreset-details)
      - [`gameSettingsPreset` Options](#gamesettingspreset-options)
      - [`gameSettingsPreset` example](#gamesettingspreset-example)
    - [`bannedAccounts` Details](#bannedaccounts-details)
      - [`bannedAccounts` Example](#bannedaccounts-example)
  - [Settings Example](#settings-example)
---

## Settings Table

>[!WARNING]
>Changes to `ip` and `queryPort` will directly affect access to the server


| Setting              | Description                                                                                                                     | Type                                                               | Default                                   | Example                                            |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ----------------------------------------- | -------------------------------------------------- |
| `name`               | A custom name displayed on the server join menu and in game                                                                     | text                                                               | `"Enshrouded Server"`                     | `"Lewd Geeks Gaming"`                              |
| `saveDirectory`      | The full path to where Enshrouded should store save files                                                                       | path                                                               | `"./savegame"`                            | `"C:/Enshrouded/GameData"`                         |
| `logDirectory`       | The full path to where Enshrouded should store log files                                                                        | path                                                               | `"./logs"`                                | `"C:/Enshrouded/GameData/Logs"`                    |
| `ip`                 | The IP address allowed t0o interact with the Enshrouded server                                                                  | text                                                               | `"0.0.0.0"`                               | `"192.168.1.224"`                                  |
| `queryPort`          | The device communications port for the Enshrouded server                                                                        | number                                                             | `15637`                                   | `324211`                                           |
| `slotCount`          | Controls the maximum number of players allowed on the server *at the same time*                                                 | number (1 - 16)                                                    | `16`                                      | `4`                                                |
| `tags`               | Help other players find a fitting server to join by using currated search tags. [read more](#tags-details)                      | list of text                                                       | `"[]"` (empty)                            | `["LookingForPlayers", "English", "BaseBuilding"]` |
| `voiceChatMode`      | If voice chat should be heard by everyone or just nearby players. Choices are `"Proximity"` or `"Global"`                       | text                                                               | `"Proximity"`                             | `"Global"`                                         |
| `enableVoiceChat`    | Allow or deny voice chat on the server. Choices are `true` or `false`                                                           | boolean                                                            | `false`                                   | `true`                                             |
| `enableTextChat`     | Allow or deny text chat on the server. Choices are `true` or `false`                                                            | boolean                                                            | `false`                                   | `true`                                             |
| `gameSettingsPreset` | A named difficulty and gameplay option. [read more](#gamesettingspreset-details)                                                | text                                                               | `"Default"`                               | `"Custom"`                                         | see |
| `userGroups`         | Provide predefined and custom logon groups with individually selected player permissions. [read more](./permission_settings.md) | list of group settings                                             | `["Admin", "Friend", "Guest", "Visitor"]` | `["Admin", "Friend", "Guild"]`                     |
| `bannedAccounts`     | A list of players not allowed to join the server. [read more](#bannedaccounts-details)                                          | list of `accountIDHash`, `displayName`, `characterName`, `banDate` | `[]` (empty)                              |                                                    |

## Additional Information

### `tags` Details

Tags help other players find a fitting server to join by using currated options to describe:

- if the server is happy to have new players
- what languages are spoken on the server and 
- if there is a main gameplay focus

> [!IMPORTANT]
> When adding `tags` to your server settings, **do not** put a comma (`,`) after the last tag in the list.

#### Allowed Tags

| Name                  | Category    |
| --------------------- | ----------- |
| `"LookingForPlayers"` | Looking For |
| `"BaseBuilding"`      | Gameplay    |
| `"Exploration"`       | Gameplay    |
| `"Roleplay"`          | Gameplay    |
| `"Chinese"`           | Language    |
| `"Italian"`           | Language    |
| `"Portuguese"`        | Language    |
| `"Thai"`              | Language    |
| `"English"`           | Language    |
| `"Japanese"`          | Language    |
| `"Russian"`           | Language    |
| `"French"`            | Language    |
| `"Korean"`            | Language    |
| `"Spanish"`           | Language    |
| `"Turkish"`           | Language    |
| `"German"`            | Language    |
| `"Polish"`            | Language    |
| `"Taiwanese"`         | Language    |
| `"Ukrainian"`         | Language    |

#### tags Examples

##### All tags on one line

```javascript
{
    ...
    "tags": ["LookingForPlayers", "English", "BaseBuilding"],
    ...
}
```

##### One tag per line

```javascript
{
    ...
    "tags": [ // <-- add tags below this line
        "LookingForPlayers",
        "English",
        "BaseBuilding"
    ], // <-- add tags above this line
    ...
}
```

### `gameSettingsPreset` Details

> [!important]
> To customize gameplay, this settings should be set to `"Custom"`

#### `gameSettingsPreset` Options

| Value          | Use-Case                                    | Description                                         |
| -------------- | ------------------------------------------- | --------------------------------------------------- |
| `"Default"`    | First-time players                          | Enshrouded default                                  |
| `"Relaxed"`    | Base-building and light-hearted adventuring | more loot, less enemies                             |
| `"Hard"`       | Tougher combat experience                   | more enemies, higher enemy aggression               |
| `"Survival"`   | Those who seek some punishment              | Hard \+ survival mechanics                          |
| **`"Custom"`** | **Fully custom gameplay and difficulty**    | **see [Gameplay Settings](./gameplay_settings.md)** |

#### `gameSettingsPreset` example

```json
{
    ...
    "gameSettingsPreset": "Custom",
    ...
}
```

### `bannedAccounts` Details

> [!note]
> Update `0.9.0.0` introduced the option to permanently ban individual players from a server.

> [!TIP]
> The list of banned players can be accessed in-game via the `Social` tab where players can be added or removed.
>
> Unless you already have a list of players to ban, its best to manage players in-game.

`bannedAccounts` is a list of collections including:

1. `accountIDHash` (privacy protected Steam account identifier)
2. `displayName` (a.k.a Steam account name)
3. `characterName`
4. `banDate` (as unix timestamp)

#### `bannedAccounts` Example

> [!WARNING]
> This is my best guess - I have not seen a list of banned accounts.

```json
{
    ...,
    "bannedAccounts": [
        { // <-- Start of banned account
            "accountIDHash": "SomeHash",
            "displayName": "Lewd-Geek1",
            "characterName": "Peaches",
            "banDate": 1767256380
        } // <-- End of banned account
    ],
    ...
}
```

## Settings Example

```json
{
	"name": "Lewd Geeks Gaming",
	"saveDirectory": "C:/Enshrouded/GameData",
	"logDirectory": "C:/Enshrouded/GameData/History",
	"ip": "192.168.1.224",
	"queryPort": 32413,
	"slotCount": 4,
	"tags": ["LookingForPlayers", "English", "BaseBuilding"],
	"voiceChatMode": "Global",
	"enableVoiceChat": false,
	"enableTextChat": true,
	"gameSettingsPreset": "Custom",
    "gameSettings": {...}, // See Gameplay Settings
    "userGroups": [...], // See Permission Settings
    "bannedAccounts": []
}
```
