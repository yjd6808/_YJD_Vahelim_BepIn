# Useful Paths for Valheim

Players run, jog, and walk faster and use less stamina when traversing leveled ground, paths, paved roads, wood, stone, iron, or hardwood . The movement boost and stamina drain decrease values can also be configured.

## Config Options
1. Going to Valheim\BepInEx\config and opening Menthus.bepinex.plugins.UsefulPaths.cfg.
2. Using the >>[BepInEx ConfigurationManager﻿](https://github.com/BepInEx/BepInEx.ConfigurationManager)<< plugin. Simply download it, put it in your Valheim\BepInEx\plugins folder, and press F1 when in-game.

## Installation (manual):
Place the UsefulPaths folder into the Valheim\BepInEx\plugins folder.

## ChangeLog

### Useful Paths 1.1.0 Release!
- Fixed issue where invalid value was being passed to Enum.Parse, causing an exception to be thrown.

### Useful Paths 1.2.0 Release!
- Added missing 'path' to list of ground types which boost movement speed and reduce stamina drain(levelground and pavedroad were already there).
- Increased default multipliers so the benefits of using different paths is more prominent.

### Useful Paths 1.3.0 Release!
- Movement bonus now applies to jogging/walking.
- Movement bonus now applies when walking on wood/stone flooring (defaults to the speed you move when walking on pavedroad).
- Improved terrain detection.

### Useful Paths 1.4.0 Release!
- Removed possible log spam to console.
- Added config options.
- Added bonus movement/stamina drain reduction to iron and hardwood materials.
- Refactored code.

### Useful Paths 1.5.0 Release!
- Fix for Null Reference Exception