# SERVER SETTINGS

[Enshrouded Server](./README.md) > Server Settings

Server settings refer to settings which affect communication between the host computer/server and Enshrouded services.

> [!TIP]
Be a decent person, **don't use offensive language**.

---
- [`name`](#name)
- [`saveDirectory`](#savedirectory)
- [`logDirectory`](#logdirectory)
- [`ip`](#ip)
- [`slotCount`](#slotcount)
- [`tags`](#tags)
  - [Allowed Tags](#allowed-tags)
  - [tags Examples](#tags-examples)
- [`voiceChatMode`](#voicechatmode)
- [`enableVoiceChat`](#enablevoicechat)
- [`enableTextChat`](#enabletextchat)
- [Settings Example](#settings-example)

---

>[!WARNING]
>Changes to `ip` and `queryPort` will directly affect access to the server


## `name` 

```json
"name": "Enshrouded Server",
```

A custom name displayed on the server join menu and in-game

| Type | Default               |
| ---- | --------------------- |
| text | `"Enshrouded Server"` |


## `saveDirectory`

```json
"saveDirectory": "./savegame",
```

The full path to where Enshrouded should store save files

| Type | Default        |
| ---- | -------------- |
| path | `"./savegame"` |

## `logDirectory`

```json
"logDirectory": "./logs",
```

The full path to where Enshrouded should store log files

| Type | Default    |
| ---- | ---------- |
| path | `"./logs"` |


## `ip`

```json
"ip": "0.0.0.0",
```

The IP address allowed t0o interact with the Enshrouded server

| Type | Default     |
| ---- | ----------- |
| text | `"0.0.0.0"` |


| `queryPort`

```json
"queryPort": 15637,
```

The device communications port for the Enshrouded server

| Type   | Default |
| ------ | ------- |
| number | `15637` |


## `slotCount`

> [!NOTE]
> The maximum number of players Enshrouded allows on a server is 16.

```json
"slotCount": 16,
```

Controls the maximum number of players allowed on the server *at the same time*.

| Type   | Default |
| ------ | ------- |
| number | `16`    |

## `tags`

```json
"tags": [
],
```

Tags help other players find a fitting server to join by using currated options to describe:

- if the server is happy to have new players
- what languages are spoken on the server and 
- if there is a main gameplay focus

| Type         | Default        |
| ------------ | -------------- |
| list of text | `"[]"` (empty) |

### Allowed Tags

Tags are not freeform.
A tag must be one of the following in order to be visible by players.

#### Looking for tags

`"LookingForPlayers"`

#### Gameplay tags

`"BaseBuilding"`, `"Exploration"`, `"Roleplay"`

#### Language tags

`"Chinese"`, `"English"`, `"French"`, `"German"`,
`"Italian"`, `"Japanese"`, `"Korean"`, `"Polish"`,
`"Portuguese"`, `"Russian"`, `"Spanish"`, `"Thai"`,
`"Taiwanese"`, `"Turkish"`, `"Ukrainian"`

### tags Examples

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

## `voiceChatMode`

```json
"voceChatMode": "Proximity",
```

If voice chat should be heard by everyone or just nearby players.
Choices are `"Proximity"` or `"Global"`.

| Type | Description   |
| ---- | ------------- |
| text | `"Proximity"` |

## `enableVoiceChat`

```json
"enableVoiceChat": false,
```

Allow or deny voice chat on the server. Choices are `true` or `false`.

| Type    | Description |
| ------- | ----------- |
| boolean | `false`     |


## `enableTextChat`

```json
"enableTextChat": false,
```

Allow or deny text chat on the server. Choices are `true` or `false`.

| Type    | Description |
| ------- | ----------- |
| boolean | `false`     |


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
  "gameSettings": {}, // See Gameplay Settings
  "userGroups": [], // See User Groups
  "bannedAccounts": [] // See Banned Accounts
}
```