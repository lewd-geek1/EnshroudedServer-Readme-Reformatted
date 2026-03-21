
# User Groups

[Enshrouded Server](./README.md) > User Groups

Player permissions for playing on dedicated servers are handled via user groups.
Each group can be set up in the `enshrouded_server.json` settings file with a unique configuration of permissions and access granted to the logged-in player. 

---

> [!NOTE]
> These settings are ordered according to my personal workflow,
> not the default order they appear in `enshrouded_settings.json`.


- [Group Options](#group-options)
  - [Reserved Slots](#reserved-slots)
  - [Can Edit World](#can-edit-world)
  - [Can Access Inventories](#can-access-inventories)
  - [Can Edit Base](#can-edit-base)
  - [Can Extend Base](#can-extend-base)
  - [Can Kick / Ban](#can-kick--ban)
- [Creating User Groups](#creating-user-groups)
  - [Preset User Groups](#preset-user-groups)
- [User Group Example](#user-group-example)
---

## Group Options

There are 6 settings configured for user groups.

### Reserved Slots

```json
"reservedSlots": 0
```

> [!CAUTION]
> Reserving 0 slots for an *admin* group could leave your server without the ability to kick/ban other players.

Limits a portion of the server's `slotCount` to login as this group only

| Type   | Options           |
| ------ | ----------------- |
| number | `1` - `slotCount` |

### Can Edit World

```json
"canEditWorld": false
```

Terraform or destroy areas in the open world

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

### Can Access Inventories

```json
"canAccessInventories": false
```

> [!warning]
>`canAccessInventories` refers to **objects in player bases**, it does *not* prevent access to treasure chests in the open world.

Storage chests, factories, collections and other containers with potentially valuable items.

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

### Can Edit Base

```json
"canEditBase": false
```

Terraforming, building and removing constructions in player bases (also includes adding and removing water)

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

### Can Extend Base

```json
"canExtendBase": false
```

*Add*, *remove*, and *upgrade* Flame Altars.

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

### Can Kick / Ban

> [!warning]
> `canKickBan` is only recommended for trusted *admin* groups

```json
"canKickBan": false
```

Kick / ban other players from the server

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

## Creating User Groups

```json
{
    "name": "Group Name",
    "password": "GroupPass",
    "reservedSlots": 0,
    "canEditWorld": false,
    "canAccessInventories": false,
    "canEditBase": false,
    "canExtendBase": false,
    "canKickBan": false
}
```

Use unique names and passwords for every user group.
The password is what determines which group membership is assigned to a player when they join the server.
The name is what they see in the join menu.

> [!TIP]
> Always limit untrusted *visitor* groups to `canEditWorld` to proctect againts grieving attempts.


### Preset User Groups

When `enshrouded.exe` is launched without `enshrouded_server.json`, 4 user groups are created *with ranzomized passwords*.
These user groups can be modified or completely removed and replaced with groups more suitable to the server's intent.

#### Admin

```json
{
    "name": "Admin",
    "password": "auto",
    "reservedSlots": 0,
    "canEditWorld": true,
    "canAccessInventories": true,
    "canEditBase": true,
    "canExtendBase": true,
    "canKickBan": true
}
```

> [!TIP]
> Reserve at least 1 slot for an admin-style group but play on your server with a regular group membership.
>
> This will help pinpoint administrative actions in Enshrouded's logs.

The preconfigured Admin group has unlimited permission. It should have a long, **strong** password to prevent unintended access.


| reservedSlots | canEditWorld | canAccessInventories | canEditBase | canExtendBase | canKickBan |
| ------------- | ------------ | -------------------- | ----------- | ------------- | ---------- |
| `0`             |  `true`         |  `true`                 |  `true`        |  `true`          |  `true`       |

#### Friend

```json
{
    "name": "Friend",
    "password": "auto",
    "reservedSlots": 0,
    "canEditWorld": true,
    "canAccessInventories": true,
    "canEditBase": false,
    "canExtendBase": false,
    "canKickBan": false
}
```

The Friend user group has access to interact with the world outside of player bases and access inventories.
Friend members cannot edit the base, modify Flame Altars, or kick/ban other players.

| reservedSlots | canEditWorld | canAccessInventories | canEditBase | canExtendBase | canKickBan |
| ------------- | ------------ | -------------------- | ----------- | ------------- | ---------- |
| `0`             |  `true`         |  `true`                 |  `false`       | `false`       |  `false`      |

#### Guest

```json
{
    "name": "Guest",
    "password": "auto",
    "canEditWorld": true,
    "canAccessInventories": false,
    "canEditBase": false,
    "canExtendBase": false,
    "canKickBan": false
}
```

The Guest user group limits members to interacting with the world outside of player bases.
They cannot access inventory, edit bases, modify Flame Altars, or kick/ban other players.

| reservedSlots | canEditWorld | canAccessInventories | canEditBase | canExtendBase | canKickBan |
| ------------- | ------------ | -------------------- | ----------- | ------------- | ---------- |
| `0`             |  `false`        |  `false`                |  `false`       |  `false`         |  `false`      |

#### Visitor

```json
{
    "name": "Visitor",
    "password": "auto",
    "canEditWorld": false,
    "canAccessInventories": false,
    "canEditBase": false,
    "canExtendBase": false,
    "canKickBan": false
}
```

The Visitor group is the most restrictive preset user group providing view-only style access.

Members of this group cannot interact with anything.
They are like a ghost that can take damage.

| reservedSlots | canEditWorld | canAccessInventories | canEditBase | canExtendBase | canKickBan |
| ------------- | ------------ | -------------------- | ----------- | ------------- | ---------- |
| `0`             |  `false`        |  `false`                |  `false`       |  `false`         |  `false`      |

## User Group Example

```json
"userGroups": [
    // Admin group (modified)
    {
        "name": "Admin",
        "password": "@dm!nR'Us",
        "reservedSlots": 1,
        "canEditWorld": true,
        "canAccessInventories": true,
        "canEditBase": true,
        "canExtendBase": true,
        "canKickBan": true
    },
    // Guild group
    {
        "name": "Guild",
        "password": "@dventure_Aw4!ts",
        "reservedSlots": 4,
        "canEditWorld": true,
        "canAccessInventories": true,
        "canEditBase": false,
        "canExtendBase": false,
        "canKickBan": false
    }
]
```

In addition to reserving 1 extra slot and updating the passord for the default `Admin` group, all other groups have been removed and a new `Guild` group has been added.

The `Guild` group is reserved for a minimum of 4 players,
shares inventory and crafting items,
and cannot redecorate or modify bases.
We've also ensured they cannot kick or ban each other when situations get heated.

| name      | password             | reservedSlots | canEditWorld | canAccessInventories | canEditBase | canExtendBase | canKickBan |
| --------- | -------------------- | ------------- | ------------ | -------------------- | ----------- | ------------- | ---------- |
| `"Admin"` | `"@dm!nR'Us"`        | `1`           | `true`       | `true`               | `true`      | `true`        | `true`     |
| `"Guild"` | `"@dventure_Aw4!ts"` | `4`           | `true`       | `true`               | `false`     | `false`       | `false`    |
