# The Blue Witch

*[English version](README.md)*

Jeu d'action 2D en vue de dessus : une sorcière élimine les ennemis de chaque niveau pour atteindre le téléporteur suivant, puis dépense son butin en améliorations.
Projet académique solo réalisé avec **Unity 2022.3** et **C#** (septembre – novembre 2023), dans le cadre du cours de moteurs de jeux.

## Fonctionnalités

- **Trois armes** (feu, glace, foudre) interchangeables en partie. La glace gèle les ennemis pendant 2 secondes, le feu inflige des dégâts sur la durée.
- **Mana** : chaque attaque consomme du mana, que le joueur recharge en maintenant Q, immobile.
- **Deux types d'ennemis** avec leurs propres déplacements et animations : le slime et le chasseur.
- **Butin aléatoire** : table de butin avec taux d'apparition par objet, définie en ScriptableObjects.
- **Boutique et progression permanente** : 3 niveaux d'amélioration pour la vie et le mana, achat des armes de glace et de foudre et de l'effet de brûlure.
- **Sauvegarde** de la progression en JSON (nom du joueur, statistiques, achats).
- **PNJ** et téléporteurs entre les niveaux, interface, effets spéciaux et sons.
- **Contenu** : menu principal, 3 niveaux, boutique et crédits.

## Architecture

| Dossier | Contenu |
| --- | --- |
| `Scripts/Player` | Contrôleur, déplacement, armes, projectiles, butin, améliorations |
| `Scripts/Enemy` | Slime et chasseur (IA, déplacement, animation), effets de statut |
| `Scripts/SO` | ScriptableObjects : armes, ennemis, butin, améliorations |
| `Scripts/Interface` | Interfaces communes (`IBaseCharacter`, `IMoveEnemy`, `IObserver`…) |
| `Scripts/DataManager.cs` | Sauvegarde et chargement JSON |

## Commandes

| Touche | Action |
| --- | --- |
| W A S D | Se déplacer |
| Clic gauche | Attaquer |
| 1 / 2 / 3 | Changer d'arme (feu, glace, foudre) |
| Q (maintenir) | Recharger le mana |
| E | Parler à un PNJ, utiliser un téléporteur |
| P / L | Sauvegarder / charger |

## Lancer le projet

1. Ouvrir le dossier `Midterm` avec **Unity 2022.3.8f1**.
2. Ouvrir la scène `Assets/Scenes/MainMenu.unity` et appuyer sur Play.

<details>
<summary>Exigences du travail</summary>

| Système demandé | Statut |
| --- | --- |
| Système de vie | Complété |
| Minimum de 5 scènes | Complété |
| Interface utilisateur | Complété |
| Effets spéciaux | Complété |
| Minimum de 5 objets à collectionner | Complété |
| Minimum de 5 animations différentes | Complété |
| 2 ennemis différents | Complété |
| Système d'expérience (remplacé par un système de mana, approuvé en classe) | Complété |
| Système de progression permanent | Complété |
| Système au choix : effets ajoutés aux attaques, avec ScriptableObjects | Complété |

</details>
