
# `bannedAccounts`

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

## `bannedAccounts` Example

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
