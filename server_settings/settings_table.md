

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

## `gameSettingsPreset` Options

| Value          | Use-Case                                    | Description                                       |
| -------------- | ------------------------------------------- | ------------------------------------------------- |
| `"Default"`    | First-time players                          | Enshrouded default                                |
| `"Relaxed"`    | Base-building and light-hearted adventuring | more loot, less enemies                           |
| `"Hard"`       | Tougher combat experience                   | more enemies, higher enemy aggression             |
| `"Survival"`   | Those who seek some punishment              | Hard \+ survival mechanics                        |
| **`"Custom"`** | **Fully custom gameplay and difficulty**    | **see [Gameplay Settings](./gameplay/README.md)** |
