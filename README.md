# The Blue Witch

*[Version française](README.fr.md)*

A 2D top-down action game: a witch clears each level of enemies to reach the next teleporter, then spends her loot on upgrades.
Solo academic project made with **Unity 2022.3** and **C#** (September – November 2023) for a game engines course.

## Features

- **Three weapons** (fire, ice, lightning) the player can switch between during play. Ice freezes enemies for 2 seconds; fire deals damage over time.
- **Mana**: every attack costs mana, which the player recharges by holding Q while standing still.
- **Two enemy types** with their own movement and animations: the slime and the hunter.
- **Random loot**: a loot table with a drop rate per item, defined in ScriptableObjects.
- **Shop and permanent progression**: 3 upgrade levels for health and mana, plus the ice and lightning weapons and the burn effect to buy.
- **Saving** progress to JSON (player name, stats, purchases).
- **NPCs** and teleporters between levels, UI, visual effects and sound.
- **Content**: main menu, 3 levels, shop and credits.

## Architecture

| Folder | Contents |
| --- | --- |
| `Scripts/Player` | Controller, movement, weapons, projectiles, loot, upgrades |
| `Scripts/Enemy` | Slime and hunter (AI, movement, animation), status effects |
| `Scripts/SO` | ScriptableObjects: weapons, enemies, loot, upgrades |
| `Scripts/Interface` | Shared interfaces (`IBaseCharacter`, `IMoveEnemy`, `IObserver`…) |
| `Scripts/DataManager.cs` | JSON save and load |

## Controls

| Key | Action |
| --- | --- |
| W A S D | Move |
| Left click | Attack |
| 1 / 2 / 3 | Switch weapon (fire, ice, lightning) |
| Q (hold) | Recharge mana |
| E | Talk to an NPC, use a teleporter |
| P / L | Save / load |

## Running the project

1. Open the `Midterm` folder with **Unity 2022.3.8f1**.
2. Open `Assets/Scenes/MainMenu.unity` and press Play.

<details>
<summary>Assignment requirements</summary>

| Required system | Status |
| --- | --- |
| Health system | Done |
| At least 5 scenes | Done |
| User interface | Done |
| Visual effects | Done |
| At least 5 collectibles | Done |
| At least 5 different animations | Done |
| 2 different enemies | Done |
| Experience system (replaced by a mana system, approved in class) | Done |
| Permanent progression system | Done |
| System of my choice: effects added to attacks, using ScriptableObjects | Done |

</details>
