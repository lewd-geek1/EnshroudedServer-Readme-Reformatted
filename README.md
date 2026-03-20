# Enshrouded Server Settings

Enshrouded server settings are stored in a text file named `enshrouded_server.json`
inside the main Enshrouded server folder.

To make editing the file easier,
use a code editor like *Codium*, *VSCode*, *notepad++*, etc...
These editors color code settings to help pinpoint which areas should be altered,
vs which need to be left alone.

## Settings Configuration

### [Server Settings](./server_settings.md)

Display name, networking, and access settings.

### [Permission Settings](./permission_settings.md)

Role Based Access Control (RBAC) for limiting player permissions based on the provided password.

### [Custom Difficulty and Gameplay Settings](./difficulty_and_gameplay_settings.md)

## [Default Server Settings](./enshrouded_server.json)

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