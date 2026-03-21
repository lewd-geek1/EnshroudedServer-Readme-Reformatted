
# User Groups

[Enshrouded Server](./README.md) > User Groups

Player permissions for playing on dedicated servers are handled via user groups.
Each group can be set up in the `enshrouded_server.json` settings file with a unique configuration of permissions and access granted to the logged-in player. 


---

- [Group Options](#group-options)
  - [Reserved Slots](#reserved-slots)
  - [Can Edit World](#can-edit-world)
  - [Can Access Inventories](#can-access-inventories)
  - [Can Edit Base](#can-edit-base)
  - [Can Extend Base](#can-extend-base)
  - [Can Kick / Ban](#can-kick--ban)
- [User Groups](#user-groups-1)
  - [Preset groups](#preset-groups)
  - [Custom groups](#custom-groups)
- [User Group Example](#user-group-example)
---

## Group Options

```json

"userGroups" = [
    ...
],

```

There are 6 settings configured for user groups.

> [!NOTE]
> These settings are ordered according to my personal workflow,
> not the default order they appear in `enshrouded_settings.json`.

### Reserved Slots

Limits a portion of the server's `slotCount` to login as this group only

| Type   | Options                 |
| ------ | ----------------------- |
| number | 1 - `slotCount` setting |

```json
"userGroups": [
    ...,
    "reservedSlots": 0, // <-- this
    ...,
]
```

### Can Edit World

Terraform or destroy areas in the open world

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

```json
"userGroups": [
    ...,
    "canEditWorld": false, // <-- this
    ...,
]
```

### Can Access Inventories

> [!warning]
>`canAccessInventories` refers to **objects in player bases**, it does *not* prevent access to treasure chests in the open world.

Storage chests, factories, collections and other containers with potentially valuable items

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |


```json
"userGroups": [
    ...,
    "canAccessInventories": false, // <-- this
    ...,
]
```

### Can Edit Base

Terraforming, building and removing constructions in player bases (also includes adding and removing water)

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

```json
"userGroups": [
    ...,
    "canEditBase": false, // <-- this
    ...
]
```

### Can Extend Base

*add*, *remove*, and *upgrade* Flame Altars

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

```json
"userGroups": [
    ...,
    "canExtendBase": false // <-- this
    ...
]
```

### Can Kick / Ban

> [!warning]
> `canKickBan` is only recommended for trusted admin groups

Kick / ban other players from the server

| Type    | Options           |
| ------- | ----------------- |
| boolean | `true` or `false` |

```json
"userGroups": [
    ...,
    "canKickBan": false // <-- this
    ...,
]
```

## User Groups

In addition to these groups, [custom groups](#custom-permission-groups) can be added to the `userGroups` list in `server_settings.json`.

> [!NOTE]
> When a fresh enshrouded_server.json is created in the current version, randomized passwords are set to prevent unwanted players from joining the server.

### Preset groups

Enshrouded's dedicated server comes with 4 player permission groups preconfigured.
They can be modified or completely removed and replaced with groups more suitable to the condition.

The default groups and their permissions include:

| `name`      | `password` | `reservedSlots` | `canEditWorld` | `canAccessInventories` | `canEditBase` | `canExtendBase` | `canKickBan` |
| ----------- | ---------- | --------------- | -------------- | ---------------------- | ------------- | --------------- | ------------ |
| **Admin**   | Auto       | `true`          | `true`         | `true`                 | `true`        | `true`          | `true`       |
| **Friend**  | Auto       | `true`          | `true`         | `true`                 | `false`       | `false`         | `false`      |
| **Guest**   | Auto       | `true`          | `false`        | `false`                | `false`       | `false`         | `false`      |
| **Visitor** | Auto       | `false`         | `false`        | `false`                | `false`       | `false`         | `false`      |

> [!NOTE]
> By default, all of the preset groups except `"Visitor"` have **full access** to interact with the game world **oudide of a Flame Alter's perimeter** including the ability to: *engage in combat*; *collect materials*; *dig for resources*; *solve quests*; etc

### Custom groups 

The Enshrouded server settings also allow custom user groups to define each option individually.

To add a cust permission group, use a unique name and passoword in a new group block (`{...}`) under `userGroups`.

> [!TIP]
> Always limit untrusted *visitor* groups to `canEditWorld` to proctect againts grieving attempts.

#### Custom group template

```json
{
    ... // other settings
    "userGroups": [
        {  // other group(s)
            ...
        },  // end of other group(s) <-- add comma to the last group
        { // start of custom group
            "name": "name",
            "password": "password",
            "reservedSlots": 0,
            "canEditWorld": false,
            "canAccessInventories": false,
            "canEditBase": false,
            "canExtendBase": false
        } // end of custom group
    ], // end of userGroups
    ... // other settings
}
```

## User Group Example

A Guild group that shares inventory and crafting items but cannot redecorate the base(s):

| `name`    | `password`       | `reservedSlots` | `canEditWorld` | `canAccessInventories` | `canEditBase` | `canExtendBase` | `canKickBan` |
| --------- | ---------------- | --------------- | -------------- | ---------------------- | ------------- | --------------- | ------------ |
| **Guild** | @dventure_Aw4!ts | 4               | `true`         | `true`                 | `false`       | `false`         | `false`      |

```json
{
    ...,
    "userGroups": [
        ..., // <-- Preset groups (keep or delete)
        {  // <-- Guild group start
            "name": "Guild",
            "password": "@dventure_Aw4!ts",
            "reservedSlots": 4,
            "canEditWorld": true,
            "canAccessInventories": true,
            "canEditBase": false,
            "canExtendBase": false,
            "canKickBan": false
        }  // <-- Guild group end
    ],
    ...
}
```
