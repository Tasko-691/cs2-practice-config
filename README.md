# CS2 Practice Config

## Description

This configuration file is designed to optimize your training environment on Counter-Strike 2 (CS2). It automates the activation of essential parameters for practice, including real-time grenade trajectory visualization with preview, extended bullet impact display, infinite ammunition, and simplified bot management. The main objective is to remove standard competitive game constraints to allow you to focus exclusively on perfecting your mechanics, learning smokes, flashbangs, molotovs, and refining your aim without interruption.

## Installation

### Automatic Installation

To simplify installation, use one of the commands below depending on your operating system. It will automatically download the configuration file and place it in the right location.

**Linux (Bash) :**
```bash
mkdir -p ~/.steam/steam/steamapps/common/Counter-Strike\ Global\ Offensive/game/csgo/cfg/ && curl -s -o ~/.steam/steam/steamapps/common/Counter-Strike\ Global\ Offensive/game/csgo/cfg/practice.cfg https://raw.githubusercontent.com/Tasko-691/cs2-practice-config/main/practice.cfg && echo "Installation completed successfully. Execute 'exec practice' in the game console." || echo "Error: Verify that the CS2 installation path is correct."
```

**Windows (PowerShell - Run as administrator) :**
```powershell
$path = "${env:ProgramFiles(x86)}\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg"; if (Test-Path $path) { try { Invoke-WebRequest -Uri "https://raw.githubusercontent.com/Tasko-691/cs2-practice-config/main/practice.cfg" -OutFile "$path\practice.cfg" -ErrorAction Stop; Write-Host "Installation completed successfully. Execute 'exec practice' in the game console." -ForegroundColor Green } catch { Write-Host "Error: Insufficient permissions. Run PowerShell as administrator." -ForegroundColor Red } } else { Write-Host "Error: CS2 directory not found. Verify your installation." -ForegroundColor Red }
```

### Manual Method

The `practice.cfg` file must be placed in the Counter-Strike 2 configuration directory:

**Windows :**
```
C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\
```

**Linux :**
```
~/.steam/steam/steamapps/common/Counter-Strike\ Global\ Offensive/game/csgo/cfg/
```

Once the file is copied, execute the following command in the game console :
```
exec practice
```

## Keybinds

### Grenade Management

| Key | Action | Description |
|-----|--------|-------------|
| **ALT** | Rethrow last grenade | Instantly reproduces the last grenade throw performed, ideal for perfecting a specific smoke or flash without repositioning |
| **K** | Remove all active grenades | Immediately eliminates all projectiles present on the map (smokes, molotovs, fires), allows quick cleanup of the training area |

### Quick Loadout

| Key | Loadout | Content |
|-----|---------|---------|
| **F1** | AWP | AWP + Desert Eagle + Flashbang + Knife |
| **F2** | AK-47 | AK-47 + Desert Eagle + Flashbang + Knife |
| **F3** | M4A1-S | M4A1-S Silencer + Desert Eagle + Flashbang + Knife |

*These keybinds allow instant switching between the weapon configurations specified above.*

### Time Control

| Key | Speed |
|-----|-------|
| **F4** | Normal speed (1x) |
| **↓** | Extreme slow motion (0.1x) |
| **←** | Slow motion (0.3x) |
| **↑** | Moderate slow motion (0.5x) |
| **→** | Slightly slowed (0.7x) |

### Bot Management

| Key | Action | Description |
|-----|--------|-------------|
| **F5** | Kick all bots | Removes all bots from the match *(Note: In Deathmatch mode, the requirement to maintain a minimum of 2 opponents prevents complete expulsion if you are alone)* |
| **F6** | Add a bot | Spawns a random bot in the opposing team |
| **P** | Place a bot | Instantly positions a bot at your crosshair location, useful for simulating specific shooting angles or clutch situations |

---