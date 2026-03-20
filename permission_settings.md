
# PERMISSION SETTINGS

Enshrouded allows hosts to define permissions for groups of players. 
This document leads through the options and also highlights areas that hosts need to be aware of.

## Player permission groups

Player permissions for playing on dedicated servers are handled via user groups.
Each group can be set up in the `enshrouded_server.json` settings file with a unique configuration of permissions and access granted to the logged-in player. 

In addition to these groups, [custom groups](#custom-permission-groups) can be added to the `userGroups` list in `server_settings.json`.

```{note}
When a fresh enshrouded_server.json is created in the current version, randomized passwords are set to prevent unwanted players from joining the server.
```

## Permission group options

| Name                   | Description                                                                                                 | Type    | Options                 |
| ---------------------- | ----------------------------------------------------------------------------------------------------------- | ------- | ----------------------- |
| `canKickBan`           | kick / ban other players from the server                                                                    | boolean | `true` or `false`       |
| `canAccessInventories` | storage chests, factories, collections and other containers with potentially valuable items                 | boolean | `true` or `false`       |
| `canEditWorld`         | terraform or destroy areas in the open world                                                                | boolean | `true` or `false`       |
| `canEditBase`          | terraforming, building and removing constructions in player bases (also includes adding and removing water) | boolean | `true` or `false`       |
| `canExtendBase`        | *add*, *remove*, and *upgrade* Flame Altars                                                                 | boolean | `true` or `false`       |
| `reservedSlots`        | limits a portion of the server's `slotCount` to login as this group only                                    | number  | 1 - `slotCount` setting |

## Preset groups

Enshrouded's dedicated server comes with 4 player permission groups preconfigured.
They can be modified or completely removed and replaced with groups more suitable to the condition.

The default groups and their permissions include:

| `name`      | `password` | `reservedSlots` | `canEditWorld` | `canAccessInventories` | `canEditBase` | `canExtendBase` | `canKickBan` |
| ----------- | ---------- | --------------- | -------------- | ---------------------- | ------------- | --------------- | ------------ |
| **Admin**   | Auto       | `true`          | `true`         | `true`                 | `true`        | `true`          | `true`       |
| **Friend**  | Auto       | `true`          | `true`         | `true`                 | `false`       | `false`         | `false`      |
| **Guest**   | Auto       | `true`          | `false`        | `false`                | `false`       | `false`         | `false`      |
| **Visitor** | Auto       | `false`         | `false`        | `false`                | `false`       | `false`         | `false`      |

```{note}
  By default, all of the preset groups except `"Visitor"` have **full access** to interact with the game world **oudide of a Flame Alter's perimeter** including the ability to: *engage in combat*; *collect materials*; *dig for resources*; *solve quests*; etc
```

## Custom permission groups 

```{warning}

`canKickBan` is only recommended for trusted admin groups

`canAccessInventories` refers to **objects in player bases**, it does *not* prevent access to treasure chests in the open world.

```

The Enshrouded server settings also allow custom user groups to define each option individually.

```{hint}

Limit visitors to `canEditWorld` to proctect againts grieving attempts.

```

## Group Example

| `name`    | `password`       | `reservedSlots` | `canEditWorld` | `canAccessInventories` | `canEditBase` | `canExtendBase` | `canKickBan` |
| --------- | ---------------- | --------------- | -------------- | ---------------------- | ------------- | --------------- | ------------ |
| **Guild** | @dventure_Aw4!ts | 4               | `true`         | `true`                 | `false`       | `false`         | `false`      |

```json
// Add your custom group(s) to the end of the userGroups list
{
    ...,
    "userGroups": [
        {  // <-- Custom Group starts here
            "name": "Guild",
            "password": "@dventure_Aw4!ts",
            "reservedSlots": 4,
            "canEditWorld": true,
            "canAccessInventories": true,
            "canEditBase": false,
            "canExtendBase": false,
            "canKickBan": false
        }  // <-- Custom Group ends here
    ],
    ...
}
```
