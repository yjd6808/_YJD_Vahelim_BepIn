﻿# ColorfulLights

  * You can color any torch, firepit, stone hearth and bonfire using RGB and HTML color codes!
  * Fireworks launched from bonfires will also be colored **AND** visible to others with the mod.
  * Those without the mod will still see yellow torches, green guck torches and standard yellow fireworks.

## Installation

### Manual

  * Un-zip `ColorfulLights.dll` to your `/Valheim/BepInEx/plugins/` folder.

### Thunderstore (manual install)

  * **Uninstall** any older versions of `ColorfulLights`.
  * Go to Settings > Import local mod > Select `ColorfulLights_v1.6.0.zip`.
  * Click "OK/Import local mod" on the pop-up for information.

## Instructions

  * In-game, press F1 to bring up the ConfigurationManager and navigate to the ColorfulLights section.
    * Change the target color using the RGB sliders or using an HTML color code.
  * Hover or any torch or fireplace and a prompt to change its color will appear.
    * This prompt can be hidden by disabling the `showChangeColorHoverText` setting.
    * Prompt font-size can be configured with the `colorPromptFontSize` setting.
  * Hit the hot-key `LeftShift + E` (configurable) to change the color.

## Changelog

### 1.6.0

  * Move action check from `Fireplace.Interact()` prefix to Player.TakeInput() transpiler delegate.
    * Can now configure the hot-key to change the color.
  * Convert spawn colored fireworks code from `Fireplace.UseItem()` prefix to a transpiler.

### 1.5.0

  * Added an option to change the font-size for the text prompt on hover.

### 1.4.0

  * Updated for Hearth & Home.
  * Renamed `LastColoredByPlayerId` ZDO key to `LightLastColoredBy`.

### 1.3.0

  * Fixed colors not applying to the Light component in the `Point light` GameObject.
  * Now writes the PlayerId to a new ZDO field: `LastColoredByPlayerId`.

### 1.2.0

  * Fixed a memory leak when caching lights/fires. Now starts a coroutine to clean-up the cache.

### 1.1.0

  * Adding configuration setting to hide the 'change color' prompt over a torch or fireplace.
  * Now saves the target color's **alpha** value to the ZDO and reads/uses this alpha value if present in the ZDO.

### 1.0.0

  * Initial release.