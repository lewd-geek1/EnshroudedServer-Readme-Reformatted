# Enshrouded Server Settings

Enshrouded server settings are stored in a text file named `enshrouded_server.json` inside the main Enshrouded server folder.
This is a reformated revision of the original `README.txt` file in the same folder.


> [!NOTE]
> To make editing the file easier,
use a code editor like *Codium*, *VSCode*, *notepad++*, etc...
These editors color code settings to help pinpoint which areas should be altered,
vs which need to be left alone.

---

## [Quick Reference](./server_settings/quick_reference.md)

Tables of settings without the extra text.

## [Server Settings](./server_settings/server_settings.md)

Display name, networking, and communication settings.

## [User Groups](./server_settings/user_groups.md)

Kinda like, Role Based Access Control (RBAC).
Used for limiting player ability through group membership related to the logon password.

## [Gameplay Settings](./server_settings/gameplay_settings.md)

When using the `"Custom"` gameplay preset, these settings are unlocked and customizable.

## [Banned Accounts](./server_settings/banned_accounts.md)

Allow or deny account-based access.

## [Default Server Settings](./enshrouded_server.json)

> [!NOTE]
> When no `enshrouded_server.json` config file is found, running `enshrouded_server.exe` will create it with the following defaults:

```json
{
    "name": "Enshrouded Server",
    "saveDirectory": "./savegame",
    "logDirectory": "./logs",
    "ip": "0.0.0.0",
    "queryPort": 15637,
    "slotCount": 16,
    "tags": [
    ],
    "voiceChatMode": "Proximity",
    "enableVoiceChat": false,
    "enableTextChat": false,
    "gameSettingsPreset": "Default",
    "gameSettings": {
        "playerHealthFactor": 1,
        "playerManaFactor": 1,
        "playerStaminaFactor": 1,
        "playerBodyHeatFactor": 1,
        "playerDivingTimeFactor": 1,
        "enableDurability": true,
        "enableStarvingDebuff": false,
        "foodBuffDurationFactor": 1,
        "fromHungerToStarving": 600000000000,
        "shroudTimeFactor": 1,
        "tombstoneMode": "AddBackpackMaterials",
        "enableGliderTurbulences": true,
        "weatherFrequency": "Normal",
        "fishingDifficulty": "Normal",
        "miningDamageFactor": 1,
        "plantGrowthSpeedFactor": 1,
        "resourceDropStackAmountFactor": 1,
        "factoryProductionSpeedFactor": 1,
        "perkUpgradeRecyclingFactor": 0.500000,
        "perkCostFactor": 1,
        "experienceCombatFactor": 1,
        "experienceMiningFactor": 1,
        "experienceExplorationQuestsFactor": 1,
        "randomSpawnerAmount": "Normal",
        "aggroPoolAmount": "Normal",
        "enemyDamageFactor": 1,
        "enemyHealthFactor": 1,
        "enemyStaminaFactor": 1,
        "enemyPerceptionRangeFactor": 1,
        "bossDamageFactor": 1,
        "bossHealthFactor": 1,
        "threatBonus": 1,
        "pacifyAllEnemies": false,
        "tamingStartleRepercussion": "LoseSomeProgress",
        "dayTimeDuration": 1800000000000,
        "nightTimeDuration": 720000000000,
        "curseModifier": "Normal"
    },
    "userGroups": [
        {
            "name": "Admin",
            "password": "Admin4ZPS25CL",
            "canKickBan": true,
            "canAccessInventories": true,
            "canEditWorld": true,
            "canEditBase": true,
            "canExtendBase": true,
            "reservedSlots": 0
        },
        {
            "name": "Friend",
            "password": "Friende_Kazu--",
            "canKickBan": false,
            "canAccessInventories": true,
            "canEditWorld": true,
            "canEditBase": true,
            "canExtendBase": false,
            "reservedSlots": 0
        },
        {
            "name": "Guest",
            "password": "GuestIK-Pwtbq",
            "canKickBan": false,
            "canAccessInventories": false,
            "canEditWorld": true,
            "canEditBase": false,
            "canExtendBase": false,
            "reservedSlots": 0
        },
        {
            "name": "Visitor",
            "password": "VisitoryJYp0I)-",
            "canKickBan": false,
            "canAccessInventories": false,
            "canEditWorld": false,
            "canEditBase": false,
            "canExtendBase": false,
            "reservedSlots": 0
        }
    ],
    "bannedAccounts": [
    ]
}
```