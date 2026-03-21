
# Banned Accounts

[Enshrouded Server](./../README.md) > Banned Accounts

> [!TIP]
> The list of banned players can be accessed in-game via the `Social` tab where players can be added or removed.
>
> Unless you already have a list of players to ban, its best to manage players in-game.

```json
"bannedAccounts": []
```

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
    "accountIDHash": "SomeHash",
    "displayName": "Lewd-Geek1",
    "characterName": "Peaches",
    "banDate": 1767256380
}
```

