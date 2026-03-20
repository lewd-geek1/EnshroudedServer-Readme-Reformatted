DIFFICULTY- AND GAMEPLAY SETTINGS


Update 0.7.3.0 (Released 2024-07-29) introduced a number of difficulty- and gameplay settings that can be configured for the dedicated server via the enshrouded_server.json - file.
Note: when no enshrouded_server.json config file is found, then a fresh file is created with the start of the enshrouded_server.exe.


Difficulty setting presets

"gameSettingsPreset":

The options are:
"Default” - The “Default” difficulty setting configures all values to default. It is the direct continuation of how Enshrouded was configured up until update 0.7.3.0 and is the recommended setting for first-time players.
“Relaxed” - The “Relaxed” preset reduces the amount of enemies and provides players with more resources and loot. This mode targets players who are most interested in base-building and light-hearted adventuring.
“Hard” - The “Hard” preset increases the amount of enemies and makes them more aggressive to give players a tougher combat experience.
“Survival” - The “Survival” preset is for those who seek some punishment with additional survival mechanics on top of more aggressive enemies.
“Custom” - When “Custom” is selected, a long list of individual settings can be tweaked. 


Individual Custom Settings incl. Default values:
Updated with new settings from version `0.9.0.0`!

Player Health
"gameSettings": {
"playerHealthFactor": 1,
}
Scales the max health for players by a factor. Ingame, the factor is represented by a percentage.
Min value: 0.25
Max value: 4


Player Mana
"gameSettings": {
"playerManaFactor": 1,
}
Scales the max mana for players by a factor. Ingame, the factor is represented by a percentage.
Min value: 0.25
Max value: 4


Player Stamina
"gameSettings": {
"playerStaminaFactor": 1,
}
Scales the max stamina for players by a factor. Ingame, the factor is represented by a percentage.
Min value: 0.25
Max value: 4


Player body heat against cold weather
"gameSettings": {
"playerBodyHeatFactor": 1,
}
Scales the max amount of available body heat in the player. The higher the factor the longer the player can stay in very cold areas before hypothermia sets in. 
Min value: 0.5
Max value: 2


NEW! Diving time
"gameSettings": {
"playerDivingTimeFactor": 1,
}
Modifies the initial amount of oxygen for players and therefore the time available underwater.
Min value: 0.5
Max value: 2


Weapon Durability
"gameSettings": {
"enableDurability": true,
}
If this setting is set to “false”, weapons don't break anymore.
Options: true / false


Hunger and Starvation
"gameSettings": {
"enableStarvingDebuff": false,
}
Enables hunger and starvation. During starvation, the player loses health periodically until death if no food or drink is consumed.
Options: true / false


Food Buff Duration
"gameSettings": {
"foodBuffDurationFactor": 1,
}
Scales food buff durations. Ingame, the factor is represented by a percentage.
Min value: 0.5
Max value: 2


Hungry State Duration
"gameSettings": {
"fromHungerToStarving": 600000000000,
}
This setting controls the length of the hungry state before the starving sets in. The unit in this setting is nanoseconds. Ingame the time is displayed in minutes.
Min value: 5 minutes
Max value: 20 minutes


Shroud time duration modifier
"gameSettings": {
"shroudTimeFactor": 1,
}
Scales how long player characters can remain within the Shroud. Ingame, the factor is represented by a percentage.
Min value: 0.5 
Max value: 2


Tombstone Mode
"gameSettings": {
"tombstoneMode": "AddBackpackMaterials"
}
The players can either keep or lose all items from their backpack when dying. In the default setting, they only lose materials. Lost items are stored in a tombstone and can be recovered there.
Options: AddBackpackMaterials / Everything / NoTombstone 


Air turbulences while gliding
"gameSettings": {
"enableGliderTurbulences": true,
}
If turned off, the glider will not be affected by air turbulences, just as in previous versions of the game.
Options: true / false


Weather phenomena frequency
"gameSettings": {
"weatherFrequency": "Normal",
}
This setting allows defining how often new weather phenomena appear in the game world.
Options: Disabled / Rare / Normal / Often


NEW! Fishing difficulty
"gameSettings": {
"fishingDifficulty": "Normal",
}
This setting defines the strength of the fish during the fishing minigame. The stronger a fish is, the longer the minigame will proceed.
Options: VeryEasy, Easy, Normal, Hard, VeryHard


Mining Effectiveness
"gameSettings": {
"miningDamageFactor": 1,
}
This scales the mining damage. A higher mining damage leads to increased terraforming and more yield of resources per hit. Ingame, the factor is represented by a percentage.
Min value: 0.5 
Max value: 2


Plant Growth Speed
"gameSettings": {
"plantGrowthSpeedFactor": 1,
}
Scales the value of the plant growth speed. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 2


Resources Gain Modifier
"gameSettings": {
"resourceDropStackAmountFactor": 1,
}
Scales the amount of materials per loot stack in chests, defeated enemies etc. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 2


Workstation Effectiveness
"gameSettings": {
"factoryProductionSpeedFactor": 1,
}
Scales the length of production times for workshop items. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 2


Weapon Recycling Yield Modifier
"gameSettings": {
"perkUpgradeRecyclingFactor": 0.100000,
}
Scales the amount of Runes that are returned to you when salvaging upgraded weapons. Ingame, the factor is represented by a percentage.
Min value: 0 
Max value: 1


Weapon Upgrading Costs
"gameSettings": {
"perkCostFactor": 1,
}
Scales the amount of Runes required for upgrading weapons. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 2


Combat Experience Modifier
"gameSettings": {
"experienceCombatFactor": 1,
}
Scales the amount of XP received through combat. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 2


Mining Experience Modifier
"gameSettings": {
"experienceMiningFactor": 1,
}
Scales the amount of XP received by mining resources. Ingame, the factor is represented by a percentage.
Min value: 0 
Max value: 2


Exploration Experience Modifier
"gameSettings": {
"experienceExplorationQuestsFactor": 1,
}
Scales the amount of XP received by exploring and completing quests. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 2


Enemy Amount
"gameSettings": {
"randomSpawnerAmount": "Normal"
}
This setting controls the amount of enemies in the world. 
Options: Few / Normal / Many / Extreme 


Modifier for simultaneous Enemy Attacks
"gameSettings": {
"aggroPoolAmount": "Normal"
}
This setting controls how many enemies are allowed to attack at the same time. Ingame, the factor is represented by a percentage.
Options: Few / Normal / Many / Extreme


Enemy Damage
"gameSettings": {
"enemyDamageFactor": 1,
}
Scales all enemy damage by this value - except for bosses. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 5


Enemy Health
"gameSettings": {
"enemyHealthFactor": 1,
}
Scales all enemy health by this value - except for bosses. Ingame, the factor is represented by a percentage.
Min value: 0.25 
Max value: 4


Enemy Stun Modifier
"gameSettings": {
"enemyStaminaFactor": 1,
}
Scales all enemy stamina by this value. It will take longer to stun enemies with a higher enemy stamina. This excludes bosses. Ingame, the factor is represented by a percentage.
Min value: 0.5 
Max value: 2


Enemy Perception Modifier
"gameSettings": {
"enemyPerceptionRangeFactor": 1,
}
Scales how far enemies can see and hear the player. This excludes bosses. Ingame, the factor is represented by a percentage.
Min value: 0.5 
Max value: 2


Boss Damage Modifier
"gameSettings": {
"bossDamageFactor": 1,
}
This setting scales the damage of boss attacks. Ingame, the factor is represented by a percentage.
Min value: 0.2 
Max value: 5


Boss Health Modifier
"gameSettings": {
"bossHealthFactor": 1,
}
Scales all health of bosses by this value. Ingame, the factor is represented by a percentage.
Min value: 0.2 
Max value: 5


Enemy Attacks Modifier
"gameSettings": {
"threatBonus": 1,
}
Scales the frequency of enemy attacks. This excludes bosses. Ingame, the factor is represented by a percentage.
Min value: 0.25
Max value: 4


Pacified Enemies
"gameSettings": {
"pacifyAllEnemies": false,
}
If turned on, enemies won't attack the players until they are attacked. This excludes bosses.
Options: true / false


Taming failure repercussions
"gameSettings": {
"tamingStartleRepercussion": "LoseSomeProgress",
}
This setting allows defining how the game reacts when the player startles the wildlife during taming. Progress is visualized by hearts in the game.
Options: KeepProgress / LoseSomeProgress / LoseAllProgress


Daytime 
"gameSettings": {
"dayTimeDuration": 1800000000000
}
Scales the length of daytime. A smaller value equals shorter daytime. The unit is nanoseconds. Ingame, the time is displayed in minutes.
Min value: 2 minutes
Max value: 60 minutes


Nighttime 
"gameSettings": {
"nightTimeDuration": 720000000000
}
Scales the length of daytime. A smaller value equals a shorter nighttime. The unit is nanoseconds. Ingame, the time is displayed in minutes.
Min value: 2 minutes
Max value: 60 minutes


Modify Shroud curse
"gameSettings": {
"curseModifier": "Normal"
}
This setting allows switching the Shroud curse off or modifying the chance for receiving the curse when being attacked by the corresponding enemies.
Options: Easy (which turns the feature off) / Normal / Hard (which doubles the chance relative to normal)

