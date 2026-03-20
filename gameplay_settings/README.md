# DIFFICULTY AND GAMEPLAY SETTINGS

[Enshrouded Server](../README.md) > Gameplay Settings

> [!WARNING]
> Only when `"gameSettingsPreset"` is set to `"Custom"`, can individual gameplay settings can be adjusted. All other options restrict the game settings to the Enshrouded configuration for that preset.

The settings in here are the difficulty and gameplay customization settings provided by Enshrouded.
Each section contains the setting's value type, default value, value options, and description.


[Reference table](./gameplay_settings/settings_table.md)

---

## Contents

- [DIFFICULTY AND GAMEPLAY SETTINGS](#difficulty-and-gameplay-settings)
  - [Contents](#contents)
  - [Player Settings](#player-settings)
    - [Player Health](#player-health)
      - [Player Health Description](#player-health-description)
    - [Player Mana](#player-mana)
      - [Player Mana Description](#player-mana-description)
    - [Player Stamina Factor](#player-stamina-factor)
      - [Player Stamina Factor Description](#player-stamina-factor-description)
    - [Player Body Heat Factor](#player-body-heat-factor)
      - [Player Body Heat Factor Description](#player-body-heat-factor-description)
    - [Player Diving Time Factor](#player-diving-time-factor)
      - [Player Diving Time Factor Description](#player-diving-time-factor-description)
  - [Difficulty Settings](#difficulty-settings)
    - [Enable Durability](#enable-durability)
      - [Enable Durability Description](#enable-durability-description)
    - [Enable Starving Debuff](#enable-starving-debuff)
      - [Enable Starving Debuff Description](#enable-starving-debuff-description)
    - [Food Buff Duration Factor](#food-buff-duration-factor)
      - [Food Buff Duration Factor Description](#food-buff-duration-factor-description)
    - [From Hunger To Starving](#from-hunger-to-starving)
      - [From Hunger To Starving Description](#from-hunger-to-starving-description)
    - [Shroud Time Factor](#shroud-time-factor)
      - [Shroud Time Factor Description](#shroud-time-factor-description)
    - [Tombstone Mode](#tombstone-mode)
      - [Tombstone Mode Description](#tombstone-mode-description)
    - [Enable Glider Turbulences](#enable-glider-turbulences)
      - [Enable Glider Turbulences Description](#enable-glider-turbulences-description)
    - [Weather Frequency](#weather-frequency)
      - [Weather Frequency Description](#weather-frequency-description)
    - [Fishing Difficulty](#fishing-difficulty)
      - [Fishing Difficulty Description](#fishing-difficulty-description)
    - [Mining Damage Factor](#mining-damage-factor)
      - [Mining Damage Factor Description](#mining-damage-factor-description)
    - [Plant Growth Speed Factor](#plant-growth-speed-factor)
      - [Plant Growth Speed Factor Description](#plant-growth-speed-factor-description)
    - [Resource Drop Stack Amount Factor](#resource-drop-stack-amount-factor)
      - [Resource Drop Stack Amount Factor Description](#resource-drop-stack-amount-factor-description)
    - [Factory Production Speed Factor](#factory-production-speed-factor)
      - [Factory Production Speed Factor Description](#factory-production-speed-factor-description)
    - [Perk Upgrade Recycling Factor](#perk-upgrade-recycling-factor)
      - [Perk Upgrade Recycling Factor Description](#perk-upgrade-recycling-factor-description)
    - [Perk Cost Factor](#perk-cost-factor)
      - [Perk Cost Factor Description](#perk-cost-factor-description)
  - [Experience Settings](#experience-settings)
    - [Experience Combat Factor](#experience-combat-factor)
      - [Experience Combat Factor Description](#experience-combat-factor-description)
    - [Experience Mining Factor](#experience-mining-factor)
      - [Experience Mining Factor Description](#experience-mining-factor-description)
    - [Experience Exploration Factor](#experience-exploration-factor)
      - [Experience Exploration Factor Description](#experience-exploration-factor-description)
  - [Enemy Settings](#enemy-settings)
    - [Random Spawner Amount](#random-spawner-amount)
      - [Random Spawner Amount Description](#random-spawner-amount-description)
    - [Aggro Pool Amount](#aggro-pool-amount)
      - [Aggro Pool Amount Description](#aggro-pool-amount-description)
    - [Enemy Damage Factor](#enemy-damage-factor)
      - [Enemy Damage Factor Description](#enemy-damage-factor-description)
    - [Enemy Health Factor](#enemy-health-factor)
      - [Enemy Health Factor Description](#enemy-health-factor-description)
    - [Enemy Stamina Factor](#enemy-stamina-factor)
      - [Enemy Stamina Factor Description](#enemy-stamina-factor-description)
    - [Enemy Perception Range Factor](#enemy-perception-range-factor)
      - [Enemy Perception Range Factor Description](#enemy-perception-range-factor-description)
    - [Boss Damage Factor](#boss-damage-factor)
      - [Boss Damage Factor Description](#boss-damage-factor-description)
    - [Boss Health Factor](#boss-health-factor)
      - [Boss Health Factor Description](#boss-health-factor-description)
    - [Threat Bonus](#threat-bonus)
      - [Threat Bonus Description](#threat-bonus-description)
    - [Pacify All Enemies](#pacify-all-enemies)
      - [Pacify All Enemies Description](#pacify-all-enemies-description)
  - [Animal Settings](#animal-settings)
    - [Taming Startle Repercussions](#taming-startle-repercussions)
      - [Taming Startle Repercussions Description](#taming-startle-repercussions-description)
  - [Time Settings](#time-settings)
    - [Day Time Duration](#day-time-duration)
      - [Day Time Duration Description](#day-time-duration-description)
    - [Night Time Duration](#night-time-duration)
      - [Night Time Duration Description](#night-time-duration-description)
  - [Shroud Settings](#shroud-settings)
    - [Curse Modifier](#curse-modifier)
      - [Curse Modifier Description](#curse-modifier-description)

---

## Player Settings

### Player Health

| Type           | Default | Options        |
| -------------- | ------- | -------------- |
| number (float) | `1`     | `0.25` - `4.0` |

```json
"gameSettings": {
    ...,
    "playerHealthFactor": 1, // <-- this
    ...,
}
```

#### Player Health Description

Scales the max health for players "by a factor".


### Player Mana

| Type           | Default | Options        |
| -------------- | ------- | -------------- |
| number (float) | `1`     | `0.25` - `4.0` |

```json
"gameSettings": {
    ...,
    "playerManaFactor": 1, // <-- this
    ...,
},
```

#### Player Mana Description

Scales the max health for players "by a factor".
Ingame, the factor is represented by a percentage.

For eample, the default value of `1` scales a player's max health by 100% (no change).



### Player Stamina Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `4.0` |

```json
"gameSettings": {
    ...,
    "playerStaminaFactor": 1, // <-- this
    ...,
}
```

#### Player Stamina Factor Description

Scales players max stamina by the given percentage.

### Player Body Heat Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

```json
"gameSettings": {
    ...,
    "playerBodyHeatFactor": 1, // <-- this
    ...,
}
```

#### Player Body Heat Factor Description

Scales the max amount of *available body heat* in the player. The higher the factor the longer the player can stay in very cold areas before hypothermia sets in.

### Player Diving Time Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

```json
"gameSettings": {
    ...,
    "playerDivingTimeFactor": 1, // <-- this
    ...,
}
```

#### Player Diving Time Factor Description

Modifies the initial amount of player oxygen (*time available underwater*).

---

## Difficulty Settings

### Enable Durability

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `true`  | `true` or `false` |

```json
"gameSettings": {
    ...,
    "enableDurability": true, // <-- this
    ...,
}
```

#### Enable Durability Description

Toggle whether weapons should break or not.
`true` means weapons break, `false` means they don't.


### Enable Starving Debuff

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `false` | `true` or `false` |

```json
"gameSettings": {
    ...,
    "enableStarvingDebuff": false, // <-- this
    ...,
}
```

#### Enable Starving Debuff Description

Enables hunger and starvation. During starvation, the player loses health periodically until death if no food or drink is consumed.


### Food Buff Duration Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

```json
"gameSettings": {
    ...,
    "foodBuffDurationFactor": 1, // <-- this
    ...,
}
```

#### Food Buff Duration Factor Description

Scales food buff durations.



### From Hunger To Starving

| Type   | Default        | Options                          |
| ------ | -------------- | -------------------------------- |
| number | `600000000000` | `300000000000` - `1200000000000` |

```json
"gameSettings": {
    ...,
    "fromHungerToStarving": 600000000000, // <-- this
    ...,
}
```

#### From Hunger To Starving Description

This setting controls the length of the hungry state before starving, **in nanoseconds** (displayed in minutes).

### Shroud Time Factor

| Type       | Default | Options      |
| ---------- | ------- | ------------ |
| percentage | `1`     | `0.5 ` - `2` |

```json
"gameSettings": {
    ...,
    "shroudTimeFactor": 1, // <-- this
    ...,
}
```

#### Shroud Time Factor Description

Scales how long player characters can remain within the Shroud.


### Tombstone Mode

| Type | Default                  | Options                                                      |
| ---- | ------------------------ | ------------------------------------------------------------ |
| text | `"AddBackpackMaterials"` | `"AddBackpackMaterials"`, `"Everything"`, or `"NoTombstone"` |

```json
"gameSettings": {
    ...,
    "tombstoneMode": "AddBackpackMaterials" // <-- this
    ...,
}
```

#### Tombstone Mode Description

The players can either keep or lose all items from their backpack when dying. In the default setting, they only lose materials. Lost items are stored in a tombstone and can be recovered there.


### Enable Glider Turbulences

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `true`  | `true` or `false` |

```json
"gameSettings": {
    ...,
    "enableGliderTurbulences": true, // <-- this
    ...,
}
```

#### Enable Glider Turbulences Description

If turned off, the glider will not be affected by air turbulences, just as in previous versions of the game.


### Weather Frequency

| Type | Default    | Options                                          |
| ---- | ---------- | ------------------------------------------------ |
| text | `"Normal"` | `"Disabled"`, `"Rare"`, `"Normal"`, or `"Often"` |

```json
"gameSettings": {
    ...,
    "weatherFrequency": "Normal", // <-- this
    ...,
}
```

#### Weather Frequency Description

This setting allows defining how often new weather phenomena appear in the game world.


### Fishing Difficulty

| Type | Default    | Options                                                        |
| ---- | ---------- | -------------------------------------------------------------- |
| text | `"Normal"` | `"VeryEasy"`, `"Easy"`, `"Normal"`, `"Hard"`, and `"VeryHard"` |

```json
"gameSettings": {
    ...,
    "fishingDifficulty": "Normal", // <-- this
    ...,
}
```

#### Fishing Difficulty Description

This setting defines the strength of the fish during the fishing minigame. The stronger a fish is, the longer the minigame will proceed.


### Mining Damage Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

```json
"gameSettings": {
    ...,
    "miningDamageFactor": 1, // <-- this
    ...,
}
```

#### Mining Damage Factor Description

This scales the mining damage. A higher mining damage leads to increased terraforming and more yield of resources per hit.


### Plant Growth Speed Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

```json
"gameSettings": {
    ...,
    "plantGrowthSpeedFactor": 1, // <-- this
    ...,
}
```

#### Plant Growth Speed Factor Description

Scales the value of the plant growth speed.
Max value: 2


### Resource Drop Stack Amount Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

```json
"gameSettings": {
    ...,
    "resourceDropStackAmountFactor": 1, // <-- this
    ...,
}
```

#### Resource Drop Stack Amount Factor Description

Scales the amount of materials per loot stack in chests, defeated enemies etc.


### Factory Production Speed Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

```json
"gameSettings": {
    ...,
    "factoryProductionSpeedFactor": 1, // <-- this
    ...,
}
```

#### Factory Production Speed Factor Description

Scales the length of production times for workshop items.


### Perk Upgrade Recycling Factor

| Type       | Default    | Options   |
| ---------- | ---------- | --------- |
| percentage | `0.100000` | `0` - `1` |

```json
"gameSettings": {
    ...,
    "perkUpgradeRecyclingFactor": 0.100000, // <-- this
    ...,
}
```

#### Perk Upgrade Recycling Factor Description

Scales the amount of Runes that are returned to you when salvaging upgraded weapons.


### Perk Cost Factor

| Type       | Default | Options      |
| ---------- | ------- | ------------ |
| percentage | `1`     | `0.25` - `2` |

```json
"gameSettings": {
    ...,
    "perkCostFactor": 1, // <-- this
    ...,
}
```

#### Perk Cost Factor Description

Scales the amount of Runes required for upgrading weapons.

## Experience Settings

### Experience Combat Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

```json
"gameSettings": {
    ...,
    "experienceCombatFactor": 1, // <-- this
    ...,
}
```

#### Experience Combat Factor Description

Scales the amount of XP received through combat.


### Experience Mining Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.0` - `2.0` |

```json
"gameSettings": {
    ...,
    "experienceMiningFactor": 1, // <-- this
    ...,
}
```

#### Experience Mining Factor Description

Scales the amount of XP received by mining resources.


### Experience Exploration Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `2.0` |

```json
"gameSettings": {
    ...,
    "experienceExplorationQuestsFactor": 1, // <-- this
    ...,
}
```

#### Experience Exploration Factor Description

Scales the amount of XP received by exploring and completing quests

---

## Enemy Settings

### Random Spawner Amount

| Type | Default    | Options                                       |
| ---- | ---------- | --------------------------------------------- |
| text | `"Normal"` | `"Few"`, `"Normal"`, `"Many"`, or `"Extreme"` |

```json
"gameSettings": {
    ...,
    "randomSpawnerAmount": "Normal" // <-- this
    ...,
}
```

#### Random Spawner Amount Description

This setting controls the amount of enemies in the world.


### Aggro Pool Amount

| Type | Default    | Options                                       |
| ---- | ---------- | --------------------------------------------- |
| text | `"Normal"` | `"Few"`, `"Normal"`, `"Many"`, or `"Extreme"` |

```json
"gameSettings": {
    ...,
    "aggroPoolAmount": "Normal" // <-- this
    ...,
}
```

#### Aggro Pool Amount Description

This setting controls how many enemies are allowed to attack at the same time.

### Enemy Damage Factor

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `5.0` |

```json
"gameSettings": {
    ...,
    "enemyDamageFactor": 1, // <-- this
    ...,
}
```

#### Enemy Damage Factor Description

Scales all enemy damage *except for bosses*.

For example, the default value of `1` scales non-boss enemy damage to `100%` or `no change`.

### Enemy Health Factor

| Type | Default | Options |
| ---- | ------- | ------- |
| percentage | `1` | `0.25` - `4.0` |

```json
"gameSettings": {
    ...,
    "enemyHealthFactor": 1, // <-- this
    ...,
}
```

#### Enemy Health Factor Description

Scales all enemy health by this value - except for bosses. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 4

### Enemy Stamina Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

```json
"gameSettings": {
    ...,
    "enemyStaminaFactor": 1, // <-- this
    ...,
}
```
#### Enemy Stamina Factor Description

Scales all enemy stamina by this value. It will take longer to stun enemies with a higher enemy stamina. This excludes bosses.




### Enemy Perception Range Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.5` - `2.0` |

```json
"gameSettings": {
    ...,
    "enemyPerceptionRangeFactor": 1, // <-- this
    ...,
}
```

#### Enemy Perception Range Factor Description

Scales how far enemies can see and hear the player. This excludes bosses.


### Boss Damage Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.2` - `5.0` |

```json
"gameSettings": {
    ...,
    "bossDamageFactor": 1, // <-- this
    ...,
}
```

#### Boss Damage Factor Description

This setting scales the damage of boss attacks.



### Boss Health Factor

| Type       | Default | Options       |
| ---------- | ------- | ------------- |
| percentage | `1`     | `0.2` - `5.0` |

```json
"gameSettings": {
    ...,
    "bossHealthFactor": 1, // <-- this
    ...,
}
```

#### Boss Health Factor Description

Scales all health of bosses by this value.


### Threat Bonus

| Type       | Default | Options        |
| ---------- | ------- | -------------- |
| percentage | `1`     | `0.25` - `4.0` |

```json
"gameSettings": {
    ...,
    "threatBonus": 1, // <-- this
    ...,
}
```

#### Threat Bonus Description

Scales the frequency of enemy attacks. This *excludes* bosses. 



### Pacify All Enemies

| Type    | Default | Options           |
| ------- | ------- | ----------------- |
| boolean | `false` | `true` or `false` |

```json
"gameSettings": {
    ...,
    "pacifyAllEnemies": false, // <-- this
    ...,
}
```

#### Pacify All Enemies Description

If turned on, enemies won't attack the players until they are attacked. This excludes bosses.
Options: true / false


---

## Animal Settings

### Taming Startle Repercussions

> [!NOTE]
> Progress is visualized by hearts in the game.

| Type | Default              | Options                                                        |
| ---- | -------------------- | -------------------------------------------------------------- |
| Text | `"LoseSomeProgress"` | `"KeepProgress"`, `"LoseSomeProgress"`, or `"LoseAllProgress"` |

```json
"gameSettings": {
    ...,
    "tamingStartleRepercussion": "LoseSomeProgress", // <-- this
    ...,
}
```

#### Taming Startle Repercussions Description

This setting allows defining how the game reacts when the player startles the wildlife during taming.

---

## Time Settings

### Day Time Duration

| Type   | Default         | Options                          |
| ------ | --------------- | -------------------------------- |
| number | `1800000000000` | `120000000000` - `3600000000000` |

```json
"gameSettings": {
    ...,
    "dayTimeDuration": 1800000000000, // <-- this
    ...,
}
```

#### Day Time Duration Description

Scales the length of daytime **in nanoseconds** (displayed in minutes).

### Night Time Duration

| Type   | Default        | Options                          |
| ------ | -------------- | -------------------------------- |
| number | `720000000000` | `120000000000` - `3600000000000` |

```json
"gameSettings": {
    ...,
    "nightTimeDuration": 720000000000, // <-- this
    ...,
}
```

#### Night Time Duration Description

Scales the length of nightime **in nanoseconds** (displayed in minutes).

---

## Shroud Settings

### Curse Modifier

> [!NOTE]
> the `"Easy"` option turns off the modifier completely.

| Type | Default    | Options                         |
| ---- | ---------- | ------------------------------- |
| text | `"Normal"` | `"Easy"`, `"Normal"`, `"Hard"`, |

```json
"gameSettings": {
    ...,
    "curseModifier": "Normal" // <-- this
    ...,
}
```

#### Curse Modifier Description

This setting allows switching the Shroud curse off or modifying the chance for receiving the curse when being attacked by the corresponding enemies.
