Small mod only. Simple stops rain from damaging structures without roofs.

UPDATED: You can now configure what is affected by this mod using the new Damage Filter:
	ALL - Mod affects all pieces
	INCLUSIVE - Mod protects only pieces that match one or more filters
	EXCLUSIVE - Mod protects all pieces except those that match one or more filters

This mod is now configurable. You can choose max damage from rain and also rain damage value per minute

Rain damage is clientside - to work on server, everyone in your immediate area on the server requires the mod, otherwise rain will still effect.

###Changes
v1.2.1:
- Added configuration to enable and disable mod
- Fixed issue with structures being treated as foundations and never getting destroyed. Found a GAME bug where on restart all structures are treated as foundations for almost a minute, but then they do break.
v1.2.0:
- Added new Damage Filter. Allows user to choose whether everything is affected by this mod, certain pieces are affected by this mod, or certain pieces are NOT affected by this mod.
- New file added that is a text file list of most available piece names for use in the comma-separated filter list part of the config for the new setting.
v1.1.1:
- Added Vortex Support
v1.1.0
- Added configuration for max damage and damage per minute that rain deals
v1.0.2
- Updated README
v1.0.1
- Updated short description
v1.0.0
- Fixed compatibility issues with ValheimPlus
- Fixed issue where rain could still affect structures in certain conditions
v0.0.1
- Made mod