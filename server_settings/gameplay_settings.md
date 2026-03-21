# GAMEPLAY SETTINGS

[Enshrouded Server](../README.md) > Gameplay Settings


The settings in here affect in-game features and mechanics.
They include settings for
player stats,
enemy stats,
environment features,
and more.

---
- [Game Settings Preset](#game-settings-preset)
  - [`gameSettingsPreset`](#gamesettingspreset)
- [Gameplay Settings](#gameplay-settings-1)
  - [Player Settings](#player-settings)
  - [Difficulty Settings](#difficulty-settings)
  - [Experience Settings](#experience-settings)
  - [Enemy Settings](#enemy-settings)
  - [Animal Settings](#animal-settings)
  - [Time Settings](#time-settings)
  - [Shroud Settings](#shroud-settings)
- [Game Settings Example](#game-settings-example)

---

## Game Settings Preset

Before any customizing can be performed, a settings preset needs to be selected.
**The selected preset overrides individually configured settings.**

### `gameSettingsPreset`

> [!WARNING]
> Only when `"gameSettingsPreset"` is set to `"Custom"`, can individual gameplay settings can be adjusted.
> All other options restrict the game settings to the Enshrouded configuration for that preset.

```json
"gameSettingsPreset": "Default",
```

A named game setting option.
Any settings preconfigured in the preset will overrule individually configured game settings.

| Type | Default     |
| ---- | ----------- |
| text | `"Default"` |

#### `gameSettingsPreset` Options

##### **`"Custom"`**

> [!TIP]
> This is probably what you want.

**Use case**: **Fully custom gameplay and difficulty**

**Details**: **see [Gameplay Settings](#gameplay-settings)**

##### `"Default"`

```json
"gameSettingsPreset": "Default",
```

**Use case**: First-time players

**Details**: Enshrouded default

##### `"Relaxed"`

**Use case**: Base-building and light-hearted adventuring

**Details**: more loot, less enemies

##### `"Hard"`

**Use case**: Tougher combat experience

**Details**: more enemies, higher enemy aggression

##### `"Survival"`

**Use case**: Those who seek some punishment

**Details**: Hard \+ survival mechanics

## Gameplay Settings

When using `"Custom"` - and only when using `"Custom"` - the following settings are
available for modification.

They control all aspects of gameplay mechanics and difficulty offered by Enshrouded.

### Player Settings

#### Player Health

```json
    "playerHealthFactor": 1,
```

Scales the max health for players "by a factor".

| Type           | Default | Options        |
| -------------- | ------- | -------------- |
| number (float) | `1`     | `0.25` - `4.0` |

#### Player Mana

```json
    "playerManaFactor": 1,
```

Scales the max mana for players.

| Type           | Default | Options        |
| -------------- | ------- | -------------- |
| number (float) | `1`     | `0.25` - `4.0` |

#### Player Stamina Factor

```json
    "playerStaminaFactor": 1,
```

Scales players max stamina by the given percentage.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `4.0` |

#### Player Body Heat Factor

```json
    "playerBodyHeatFactor": 1,
```

Adjusts the max amount of time a player can withstand frost.

> Scales the max amount of *available body heat* in the player.
> 
> The higher the factor the longer the player can stay in very cold areas before hypothermia sets in.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

#### Player Diving Time Factor

```json
    "playerDivingTimeFactor": 1,
```

Modifies the initial amount of player oxygen (*time available underwater*).

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

---

### Difficulty Settings

#### Enable Durability

```json
    "enableDurability": true,
```

Toggle whether weapons should break or not.
`true` means weapons break, `false` means they don't.

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `true`  | `true` or `false` |

#### Enable Starving Debuff

```json
    "enableStarvingDebuff": false,
```

Enables hunger and starvation. During starvation, the player loses health periodically until death if no food or drink is consumed.

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `false` | `true` or `false` |

#### Food Buff Duration Factor

```json
    "foodBuffDurationFactor": 1,
```

Scales food buff durations.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

#### From Hunger To Starving

```json
    "fromHungerToStarving": 600000000000,
```

This setting controls the length of the hungry state before starving, **in nanoseconds** (displayed in minutes).

| Type   | Default        | Options                          |
| ------ | -------------- | -------------------------------- |
| number | `600000000000` | `300000000000` - `1200000000000` |

#### Shroud Time Factor

```json
    "shroudTimeFactor": 1,
```

Scales how long player characters can remain within the Shroud.

| Type       | Default | Options      |
| ---------- | ------- | ------------ |
| percentage | `1`     | `0.5 ` - `2` |

#### Tombstone Mode

```json
    "tombstoneMode": "AddBackpackMaterials"
```

The players can either keep or lose all items from their backpack when dying. In the default setting, they only lose materials. Lost items are stored in a tombstone and can be recovered there.

| Type | Default                  | Options                                                      |
| ---- | ------------------------ | ------------------------------------------------------------ |
| text | `"AddBackpackMaterials"` | `"AddBackpackMaterials"`, `"Everything"`, or `"NoTombstone"` |

#### Enable Glider Turbulences

```json
    "enableGliderTurbulences": true,
```

If turned off, the glider will not be affected by air turbulences, just as in previous versions of the game.

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `true`  | `true` or `false` |

#### Weather Frequency

```json
    "weatherFrequency": "Normal",
```

This setting allows defining how often new weather phenomena appear in the game world.

| Type | Default    | Options                                          |
| ---- | ---------- | ------------------------------------------------ |
| text | `"Normal"` | `"Disabled"`, `"Rare"`, `"Normal"`, or `"Often"` |

#### Fishing Difficulty

```json
    "fishingDifficulty": "Normal",
```

This setting defines the strength of the fish during the fishing minigame. The stronger a fish is, the longer the minigame will proceed.

| Type | Default    | Options                                                        |
| ---- | ---------- | -------------------------------------------------------------- |
| text | `"Normal"` | `"VeryEasy"`, `"Easy"`, `"Normal"`, `"Hard"`, and `"VeryHard"` |

#### Mining Damage Factor

```json
    "miningDamageFactor": 1,
```

This scales the mining damage. A higher mining damage leads to increased terraforming and more yield of resources per hit.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

#### Plant Growth Speed Factor

```json
    "plantGrowthSpeedFactor": 1,
```

Scales the value of the plant growth speed.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

#### Resource Drop Stack Amount Factor

```json
    "resourceDropStackAmountFactor": 1,
```

Scales the amount of materials per loot stack in chests, defeated enemies etc.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

#### Factory Production Speed Factor

```json
    "factoryProductionSpeedFactor": 1,
```

Scales the length of production times for workshop items.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

#### Perk Upgrade Recycling Factor

```json
    "perkUpgradeRecyclingFactor": 0.100000,
```

Scales the amount of Runes that are returned to you when salvaging upgraded weapons.

| Type       | Default    | Options   |
| ---------- | ---------- | --------- |
| percentage | `0.100000` | `0` - `1` |

#### Perk Cost Factor

```json
    "perkCostFactor": 1,
```

Scales the amount of Runes required for upgrading weapons.

| Type       | Default | Options      |
| ---------- | ------- | ------------ |
| percentage | `1`     | `0.25` - `2` |

---

### Experience Settings

#### Experience Combat Factor

```json
    "experienceCombatFactor": 1,
```

Scales the amount of XP received through combat.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

#### Experience Mining Factor

```json
    "experienceMiningFactor": 1,
```

Scales the amount of XP received by mining resources.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.0` - `2.0` |

#### Experience Exploration Factor

```json
    "experienceExplorationQuestsFactor": 1,
```

Scales the amount of XP received by exploring and completing quests

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

---

### Enemy Settings

#### Random Spawner Amount

```json
    "randomSpawnerAmount": "Normal"
```

This setting controls the amount of enemies in the world.

| Type | Default    | Options                                       |
| ---- | ---------- | --------------------------------------------- |
| text | `"Normal"` | `"Few"`, `"Normal"`, `"Many"`, or `"Extreme"` |

#### Aggro Pool Amount

```json
    "aggroPoolAmount": "Normal"
```

This setting controls how many enemies are allowed to attack at the same time.

| Type | Default    | Options                                       |
| ---- | ---------- | --------------------------------------------- |
| text | `"Normal"` | `"Few"`, `"Normal"`, `"Many"`, or `"Extreme"` |

#### Enemy Damage Factor

```json
    "enemyDamageFactor": 1,
```

Scales all enemy damage *except for bosses*.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `5.0` |

#### Enemy Health Factor

```json
    "enemyHealthFactor": 1,
```

Scales all enemy health by this value - except for bosses. Ingame, the factor is represented by a percentage.

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `4.0` |

#### Enemy Stamina Factor

```json
    "enemyStaminaFactor": 1,
```

Scales all enemy stamina by this value. It will take longer to stun enemies with a higher enemy stamina. This excludes bosses.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

#### Enemy Perception Range Factor

```json
    "enemyPerceptionRangeFactor": 1,
```

Scales how far enemies can see and hear the player. This excludes bosses.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

#### Boss Damage Factor

```json
    "bossDamageFactor": 1,
```

This setting scales the damage of boss attacks.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.2` - `5.0` |

#### Boss Health Factor

```json
    "bossHealthFactor": 1,
```

Scales all health of bosses by this value.

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.2` - `5.0` |

#### Threat Bonus

```json
    "threatBonus": 1,
```

Scales the frequency of enemy attacks. This *excludes* bosses. 

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `4.0` |

#### Pacify All Enemies

```json
    "pacifyAllEnemies": false,
```

If turned on, enemies won't attack the players until they are attacked. This excludes bosses.
Options: true / false

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `false` | `true` or `false` |

---

### Animal Settings

#### Taming Startle Repercussions

> [!NOTE]
> Progress is visualized by hearts in the game.

```json
    "tamingStartleRepercussion": "LoseSomeProgress",
```

This setting allows defining how the game reacts when the player startles the wildlife during taming.

| Type | Default              | Options                                                        |
| ---- | -------------------- | -------------------------------------------------------------- |
| Text | `"LoseSomeProgress"` | `"KeepProgress"`, `"LoseSomeProgress"`, or `"LoseAllProgress"` |

---

### Time Settings

#### Day Time Duration

```json
    "dayTimeDuration": 1800000000000,
```

Scales the length of daytime **in nanoseconds** (displayed in minutes).

| Type   | Default         | Options                          |
| ------ | --------------- | -------------------------------- |
| number | `1800000000000` | `120000000000` - `3600000000000` |

#### Night Time Duration

```json
    "nightTimeDuration": 720000000000,
```

Scales the length of nightime **in nanoseconds** (displayed in minutes).

| Type   | Default        | Options                          |
| ------ | -------------- | -------------------------------- |
| number | `720000000000` | `120000000000` - `3600000000000` |

---

### Shroud Settings

#### Curse Modifier

> [!NOTE]
> the `"Easy"` option turns off the modifier completely.

```json
    "curseModifier": "Normal"
```

This setting allows switching the Shroud curse off or modifying the chance for receiving the curse when being attacked by the corresponding enemies.

| Type | Default    | Options                         |
| ---- | ---------- | ------------------------------- |
| text | `"Normal"` | `"Easy"`, `"Normal"`, `"Hard"`, |

## Game Settings Example


```json
"gameSettingsPreset": "Custom",
"gameSettings": {
    "playerHealthFactor": 2.0,  // 2x original
    "playerManaFactor": 2.0,  // 2x original
    "playerStaminaFactor": 2.0,  // 2x original
    "playerBodyHeatFactor": 2.0,  // 2x original
    "playerDivingTimeFactor": 2.0,  // 2x original
    "enableDurability": false, // items don't break
    "enableStarvingDebuff": false, // no starving
    "foodBuffDurationFactor": 2.0, // 2x original
    "fromHungerToStarving": 600000000000, // doesn't matter, no starving
    "shroudTimeFactor": 2.0, // 2x original
    "tombstoneMode": "NoTombstone",  // nothing lost
    "enableGliderTurbulences": false, // smooth gliding
    "weatherFrequency": "Disabled", // no weather
    "fishingDifficulty": "VeryEasy", // as easy as possible
    "miningDamageFactor": 2.0, // 2x original
    "plantGrowthSpeedFactor": 2.0, // 2x original
    "resourceDropStackAmountFactor": 2.0, // 2x original
    "factoryProductionSpeedFactor": 2.0, // 2x original
    "perkUpgradeRecyclingFactor": 1.0, // max back
    "perkCostFactor": 0.25, // least cost
    "experienceCombatFactor": 2.0, // 2x original
    "experienceMiningFactor": 2.0, // 2x original
    "experienceExplorationQuestsFactor": 2.0, // 2x original
    "randomSpawnerAmount": "Few", // least amount
    "aggroPoolAmount": "Few", // least amount
    "enemyDamageFactor": 0.5, // 1/2 original
    "enemyHealthFactor": 0.5, // 1/2 original
    "enemyStaminaFactor": 0.5, // 1/2 original
    "enemyPerceptionRangeFactor": 0.5, // 1/2 original
    "bossDamageFactor": 0.5, // 1/2 original
    "bossHealthFactor": 0.5, // 1/2 original
    "threatBonus": 0.5, // 1/2 original
    "pacifyAllEnemies": true, // non-aggressive enemies
    "tamingStartleRepercussion": "KeepProgress", // least effort
    "dayTimeDuration": 3600000000000, // max daytime
    "nightTimeDuration": 120000000000, // min nighttime
    "curseModifier": "Easy" // no curse modifier
},
```