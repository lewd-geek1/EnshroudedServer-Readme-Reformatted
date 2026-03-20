# SERVER SETTINGS

Server settings refer to settings which affect communication between the host computer/server and Enshrouded services.
While permission and gameplay settings are technically part of server settings, they are excluded from this document.

```{tip}
Be a decent person, **don't use offensive language**.
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

## Settings Table

```{warning}

Changes `ip` and `queryPort` will directly affect access to the server:
```

| Setting | Description | Type | Default | Example |
| --- | --- | --- | --- | --- |
| `name` | A custom name displayed on the server join menu and in game | text | `"Enshrouded Server"` | `"Lewd Geeks Gaming"` |
| `saveDirectory` | The full path to where Enshrouded should store save files | path | `"./savegame"` | `"C:/Enshrouded/GameData"` |
| `logDirectory` | The full path to where Enshrouded should store log files | path | `"./logs"` | `"C:/Enshrouded/GameData/Logs"` |
| `ip` | The IP address allowed t0o interact with the Enshrouded server | text | `"0.0.0.0"` | `"192.168.1.224"` |
| `queryPort` | The device communications port for the Enshrouded server | number | `15637` | `324211` |
| `slotCount` | Controls the maximum number of players allowed on the server *at the same time* | number (1 - 16) | `16` | `4` |
| `tags` | Help other players find a fitting server to join by using currated search tags. [read more](#tags-details) | list of text | `"[]"` (empty) | `["LookingForPlayers", "English", "BaseBuilding"]` |
| `voiceChatMode` | If voice chat should be heard by everyone or just nearby players. Choices are `"Proximity"` or `"Global"` | text | `"Proximity"` | `"Global"` |
| `enableVoiceChat` | Allow or deny voice chat on the server. Choices are `true` or `false` | boolean | `false` | `true` |
| `enableTextChat` | Allow or deny text chat on the server. Choices are `true` or `false` | boolean | `false` | `true` |
| `gameSettingsPreset` | A named difficulty and gameplay option. [read more](#gamesettingspreset-details) | text | `"Default"` | `"Custom"` | see |
| `userGroups` | Provide predefined and custom logon groups with individually selected player permissions. [read more](./permission_settings.md) | list of group settings | `["Admin", "Friend", "Guest", "Visitor"]` | `["Admin", "Friend", "Guild"]` |
| `bannedAccounts` | A list of players not allowed to join the server. [read more](#bannedaccounts-details) | list of `accountIDHash`, `displayName`, `characterName`, `banDate` | `[]` (empty) | |

## Additional Information

### `tags` Details

```{important}
When adding `tags` to your server settings, **do not** put a comma (`,`) after the last tag in the list.
```

Tags help other players find a fitting server to join by using currated options to describe:

- if the server is happy to have new players
- what languages are spoken on the server and 
- if there is a main gameplay focus

#### Allowed Tags

| Name | Category |
| --------------------- | ----------- |
| `"LookingForPlayers"` | Looking For |
| `"BaseBuilding"` | Gameplay |
| `"Exploration"` | Gameplay |
| `"Roleplay"` | Gameplay |
| `"Chinese"` | Language |
| `"Italian"` | Language |
| `"Portuguese"` | Language |
| `"Thai"` | Language |
| `"English"` | Language |
| `"Japanese"` | Language |
| `"Russian"` | Language |
| `"French"` | Language |
| `"Korean"` | Language |
| `"Spanish"` | Language |
| `"Turkish"` | Language |
| `"German"` | Language |
| `"Polish"` | Language |
| `"Taiwanese"` | Language |
| `"Ukrainian"` | Language |

#### tags Examples

#### All tags on one line

```javascript

{
    ...
    "tags": ["LookingForPlayers", "English", "BaseBuilding"],
    ...
}

```

#### One tag per line

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

```{important}
To customize gameplay, this settings should be set to `"Custom"`
```
#### `gameSettingsPreset` Options

| Value | Use-Case  | Description |
| -------------- | ------------------------------------------- | --------------------------------------------------- |
| `"Default"` | First-time players | Enshrouded default |
| `"Relaxed"` | Base-building and light-hearted adventuring | more loot, less enemies |
| `"Hard"` | Tougher combat experience | more enemies, higher enemy aggression |
| `"Survival"` | Those who seek some punishment | Hard \+ survival mechanics |
| **`"Custom"`** | **Fully custom gameplay and difficulty** | **see [Gameplay Settings](./gameplay_settings.md)** |

### `bannedAccounts` Details

```{note}
On top of the previously available "kick"-option for server hosts, update `0.9.0.0` introduced the option to permanently ban individual players from a server.
```

The list of banned players can be accessed in-game via the `Social` tab where players can be added or removed.
The list can also be manually edited in `enshrouded_server.json` when the server is not running.

The information stored in `enshrouded_server.json` is `accountIDHash` (an identifier for the Steam account ID without violating the protected personal data of the player), `displayName` (a.k.a Steam account name), `characterName` and `banDate` (which is stored as unix timestamp).
