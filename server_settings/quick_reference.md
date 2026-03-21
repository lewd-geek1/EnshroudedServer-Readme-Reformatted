# Reference Tables

Quick-reference tables of settings.

- [Server Settings](#server-settings)
- [Allowed Tags](#allowed-tags)
- [Game Settings Preset Options](#game-settings-preset-options)
- [Gameplay Settings](#gameplay-settings)
- [User Group Settings](#user-group-settings)

## Server Settings

| Setting              | Type         | Default                                                                     | Options                                                       | Example                                            |
| -------------------- | ------------ | --------------------------------------------------------------------------- | ------------------------------------------------------------- | -------------------------------------------------- |
| `name`               | text         | `"Enshrouded Server"`                                                       | any text                                                      | `"Lewd Geeks Gaming"`                              |
| `saveDirectory`      | path         | `"./savegame"`                                                              | The full path to any folder                                   | `"C:/Enshrouded/GameData"` `                       |
| `logDirectory`       | path         | `"./logs"`                                                                  | The full path to any folder                                   | `"C:/Enshrouded/GameData/Logs"` `                  |
| `ip`                 | text         | `"0.0.0.0"`                                                                 | Any IP address (typically the address assigned to the device) | `"192.168.1.224"`                                  |
| `queryPort`          | number       | Any available port (best practice use an unregistered port `49152`-`65535`) | `15637`                                                       | `56481`                                            |
| `slotCount`          | number       | `1` - `16`                                                                  | `16`                                                          | `4`                                                |
| `tags`               | list of text | `"[]"` (empty)                                                              | See [Allowed Tags](#allowed-tags)                             | `["LookingForPlayers", "English", "BaseBuilding"]` |
| `voiceChatMode`      | text         | `"Proximity"`                                                               | `"Proximity"` or `"Global"`                                   | `"Global"`                                         |
| `enableVoiceChat`    | boolean      | `false`                                                                     | `true` or `false`                                             | `true`                                             |
| `enableTextChat`     | boolean      | `false`                                                                     | `true` or `false`                                             | `true`                                             |
| `gameSettingsPreset` | text         | `"Default"`                                                                 | see [gameSettingsPreset Options](#gamesettingspreset-options) | `"Custom"`                                         |

## Allowed Tags

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

## Game Settings Preset Options

| Value          | Use-Case                                    | Description                              |
| -------------- | ------------------------------------------- | ---------------------------------------- |
| **`"Custom"`** | **Fully custom gameplay and difficulty**    | **see [Gameplay Settings](./README.md)** |
| `"Default"`    | First-time players                          | Enshrouded default                       |
| `"Relaxed"`    | Base-building and light-hearted adventuring | more loot, less enemies                  |
| `"Hard"`       | Tougher combat experience                   | more enemies, higher enemy aggression    |
| `"Survival"`   | Those who seek some punishment              | Hard \+ survival mechanics               |


## Gameplay Settings

| Value                                 | Type           | Default                  | Options                                                        |
| ------------------------------------- | -------------- | ------------------------ | -------------------------------------------------------------- |
| `"playerHealthFactor"`                | number (float) | `1`                      | `0.25` - `4.0`                                                 |
| `"playerManaFactor"`                  | number (float) | `1`                      | `0.25` - `4.0`                                                 |
| `"playerStaminaFactor"`               | percentage     | `1`                      | `0.25` - `4.0`                                                 |
| `"playerBodyHeatFactor"`              | percentage     | `1`                      | `0.5` - `2.0`                                                  |
| `"playerDivingTimeFactor"`            | percentage     | `1`                      | `0.5` - `2.0`                                                  |
| `"enableDurability"`                  | boolean        | `true`                   | `true` or `false`                                              |
| `"enableStarvingDebuff"`              | boolean        | `false`                  | `true` or `false`                                              |
| `"foodBuffDurationFactor"`            | percentage     | `1`                      | `0.5` - `2.0`                                                  |
| `"fromHungerToStarving"`              | number         | `600000000000`           | `300000000000` - `1200000000000`                               |
| `"shroudTimeFactor"`                  | percentage     | `1`                      | `0.5 ` - `2`                                                   |
| `"tombstoneMode"`                     | text           | `"AddBackpackMaterials"` | `"AddBackpackMaterials"`, `"Everything"`, or `"NoTombstone"`   |
| `"enableGliderTurbulences"`           | boolean        | `true`                   | `true` or `false`                                              |
| `"weatherFrequency"`                  | text           | `"Normal"`               | `"Disabled"`, `"Rare"`, `"Normal"`, or `"Often"`               |
| `"fishingDifficulty"`                 | text           | `"Normal"`               | `"VeryEasy"`, `"Easy"`, `"Normal"`, `"Hard"`, and `"VeryHard"` |
| `"miningDamageFactor"`                | percentage     | `1`                      | `0.5` - `2.0`                                                  |
| `"plantGrowthSpeedFactor"`            | percentage     | `1`                      | `0.25` - `2.0`                                                 |
| `"resourceDropStackAmountFactor"`     | percentage     | `1`                      | `0.25` - `2.0`                                                 |
| `"factoryProductionSpeedFactor"`      | percentage     | `1`                      | `0.25` - `2.0`                                                 |
| `"perkUpgradeRecyclingFactor"`        | percentage     | `0.100000`               | `0` - `1`                                                      |
| `"perkCostFactor"`                    | percentage     | `1`                      | `0.25` - `2`                                                   |
| `"experienceCombatFactor"`            | percentage     | `1`                      | `0.25` - `2.0`                                                 |
| `"experienceMiningFactor"`            | percentage     | `1`                      | `0.0` - `2.0`                                                  |
| `"experienceExplorationQuestsFactor"` | percentage     | `1`                      | `0.25` - `2.0`                                                 |
| `"randomSpawnerAmount"`               | text           | `"Normal"`               | `"Few"`, `"Normal"`, `"Many"`, or `"Extreme"`                  |
| `"aggroPoolAmount"`                   | text           | `"Normal"`               | `"Few"`, `"Normal"`, `"Many"`, or `"Extreme"`                  |
| `"enemyDamageFactor"`                 | percentage     | `1`                      | `0.25` - `5.0`                                                 |
| `"enemyHealthFactor"`                 | percentage     | `1`                      | `0.25` - `4.0`                                                 |
| `"enemyStaminaFactor"`                | percentage     | `1`                      | `0.5` - `2.0`                                                  |
| `"enemyPerceptionRangeFactor"`        | percentage     | `1`                      | `0.5` - `2.0`                                                  |
| `"bossDamageFactor"`                  | percentage     | `1`                      | `0.2` - `5.0`                                                  |
| `"bossHealthFactor"`                  | percentage     | `1`                      | `0.2` - `5.0`                                                  |
| `"threatBonus"`                       | percentage     | `1`                      | `0.25` - `4.0`                                                 |
| `"pacifyAllEnemies"`                  | boolean        | `false`                  | `true` or `false`                                              |
| `"tamingStartleRepercussion"`         | Text           | `"LoseSomeProgress"`     | `"KeepProgress"`, `"LoseSomeProgress"`, or `"LoseAllProgress"` |
| `"dayTimeDuration"`                   | number         | `1800000000000`          | `120000000000` - `3600000000000`                               |
| `"nightTimeDuration"`                 | number         | `720000000000`           | `120000000000` - `3600000000000`                               |
| `"curseModifier"`                     | text           | `"Normal"`               | `"Easy"`, `"Normal"`, `"Hard"`,                                |

## User Group Settings

| Name                   | Type    | Options           |
| ---------------------- | ------- | ----------------- |
| `canKickBan`           | boolean | `true` or `false` |
| `canAccessInventories` | boolean | `true` or `false` |
| `canEditWorld`         | boolean | `true` or `false` |
| `canEditBase`          | boolean | `true` or `false` |
| `canExtendBase`        | boolean | `true` or `false` |
| `reservedSlots`        | number  | 1 - `slotCount`   |
