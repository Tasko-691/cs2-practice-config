# CS2 Practice Config

## Description

Ce fichier de configuration est conçu pour optimiser votre environnement d'entraînement sur Counter-Strike 2 (CS2). Il automatise l'activation de paramètres essentiels pour la pratique, notamment la visualisation des trajectoires de grenades avec prévisualisation en temps réel, les impacts de balles prolongés, les munitions infinies et la gestion simplifiée des bots. L'objectif principal est de supprimer les contraintes du jeu compétitif standard pour vous permettre de vous concentrer exclusivement sur le perfectionnement de vos mécaniques, l'apprentissage de smokes, flashbangs, molotovs, et l'affinement de votre aim sans interruption.

## Installation

### Installation automatique

Pour simplifier l'installation, utilisez l'une des commandes ci-dessous selon votre système d'exploitation. Elle téléchargera automatiquement le fichier de configuration et le placera au bon endroit.

**Linux (Bash) :**
```bash
mkdir -p ~/.steam/steam/steamapps/common/Counter-Strike\ Global\ Offensive/game/csgo/cfg/ && curl -s -o ~/.steam/steam/steamapps/common/Counter-Strike\ Global\ Offensive/game/csgo/cfg/practice.cfg https://raw.githubusercontent.com/Tasko-691/cs2-practice-config/main/practice.cfg && echo "Installation terminée avec succès. Exécutez 'exec practice' dans la console du jeu." || echo "Erreur : Vérifiez que le chemin d'installation de CS2 est correct."
```

**Windows (PowerShell - Exécuter en tant qu'administrateur) :**
```powershell
$path = "${env:ProgramFiles(x86)}\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg"; if (Test-Path $path) { try { Invoke-WebRequest -Uri "https://raw.githubusercontent.com/Tasko-691/cs2-practice-config/main/practice.cfg" -OutFile "$path\practice.cfg" -ErrorAction Stop; Write-Host "Installation terminée avec succès. Exécutez 'exec practice' dans la console du jeu." -ForegroundColor Green } catch { Write-Host "Erreur : Permissions insuffisantes. Lancez PowerShell en tant qu'administrateur." -ForegroundColor Red } } else { Write-Host "Erreur : Le répertoire CS2 n'a pas été trouvé. Vérifiez votre installation." -ForegroundColor Red }
```

### Méthode manuelle

Le fichier `practice.cfg` doit être placé dans le répertoire de configuration de Counter-Strike 2 :

**Windows :**
```
C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\
```

**Linux :**
```
~/.steam/steam/steamapps/common/Counter-Strike\ Global\ Offensive/game/csgo/cfg/
```

Une fois le fichier copié, exécutez la commande suivante dans la console du jeu :
```
exec practice
```

## Raccourcis clavier

### Gestion des grenades

| Touche | Action | Description |
|--------|--------|-------------|
| **ALT** | Relancer la dernière grenade | Reproduit instantanément le dernier lancer de grenade effectué, idéal pour perfectionner un smoke ou un flash spécifique sans avoir à se repositionner |
| **K** | Supprimer toutes les grenades actives | Élimine immédiatement tous les projectiles présents sur la map (smokes, molotovs, incendies), permet de nettoyer rapidement la zone d'entraînement |

### Loadout rapide

| Touche | Loadout | Contenu |
|--------|---------|---------|
| **F1** | AWP | AWP + Desert Eagle + Flashbang + Couteau |
| **F2** | AK-47 | AK-47 + Desert Eagle + Flashbang + Couteau |
| **F3** | M4A1-S | M4A1-S Silencieux + Desert Eagle + Flashbang + Couteau |

*Ces raccourcis permettent de switcher instantanément entre les configurations d'armes précisées ci-dessus.*

### Contrôle du temps

| Touche | Vitesse |
|--------|---------|
| **F4** | Vitesse normale (1x) |
| **↓**  | Ralenti extrême (0.1x) |
| **←**  | Ralenti (0.3x) |
| **↑**  | Ralenti modéré (0.5x) |
| **→**  | Légèrement ralenti (0.7x) |

### Gestion des bots

| Touche | Action | Description |
|--------|--------|-------------|
| **F5** | Expulser tous les bots | Retire tous les bots de la partie *(Note : En mode Deathmatch, la nécessité de maintenir 2 adversaires minimum empêche l'expulsion complète si vous êtes seul)* |
| **F6** | Ajouter un bot | Fait spawn un bot aléatoire dans l'équipe adverse |
| **P**  | Placer un bot | Positionne instantanément un bot à l'emplacement de votre viseur, pratique pour simuler des angles de tir spécifiques ou des situations de clutch |

---