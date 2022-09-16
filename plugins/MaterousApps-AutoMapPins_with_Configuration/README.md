# AutoMapPins with Configuration for Valheim

This is [AMP-Configuration 1.2.0](https://www.nexusmods.com/valheim/mods/744) for Valheim.

After using the AutoMapPins mod by Bdew, I found that I needed a bit of configuration for it (as well as many other people).  I reached out and asked if they wouldn't mind if I tried my hand at adding some configuration.  With their permission I have added a configuration file for the mod.

Changes from original Mod:
Added configuration file
Added option to use colored pins (the dot) or the sprite for the item. Copper nodes will show Copper Ore, Berry bushes will show Berries.
Added option to each pin to be able to show it, it's name, and to save it.  ~~The save isn't permanent. It is only for that session. They will vanish if you log out. However they will stay if you move away from the area.~~
Added option to disable multiple pins of the same type within a certain radius. Larger number means less pins in an area. (this is useful for berries)
Added scaling options for each pin. By default they will be smaller than the other pins on the map, just so everything isn't clustered.

ToDo:
Add ability to upload custom images for each pin
~~Add other spawn types (crypts, spawners, chitin, etc.) - if there is interest~~

## Changes from original Mod

*Added configuration file
*Added option to use colored pins (the dot) or the sprite for the item. Copper nodes will show Copper Ore, Berry bushes will show Berries.
*Added option to each pin to be able to show it, it's name, and to save it.  The save isn't permanent. It is only for that session. They will vanish if you log out. However they will stay if you move away from the area.
*Added option to disable multiple pins of the same type within a certain radius. Larger number means less pins in an area. (this is useful for berries)
*Added scaling options for each pin. By default they will be smaller than the other pins on the map, just so everything isn't clustered.

## Installation (manual)

If you are installing this manually, do the following

1. Extract the archive into a folder.
2. Move the AMP_Configurable.dll from `AMP_Configurable` folder into `<Steam Location>\steamapps\common\Valheim\BepInEx\Plugins` folder.
3. Run the game however you would normally

At this moment, you can use the following channels to ask for help

* [NexusMods Posts](https://www.nexusmods.com/valheim/mods/744?tab=posts)
* [NexusMods Bugs](https://www.nexusmods.com/valheim/mods/744?tab=bugs) 

## Changelog

#### 1.2.2
* Disabled commands as they were not working.  Will need to set aside time to look into them and get them working. In the meantime, right clicking should work to remove any pins.

#### 1.2.1
* Accidentally uploaded .7z zip instead of .dll in the .zip on Thunderstore only. Corrected

#### 1.2.0
* Fixed issue with related to release of H&H

#### 1.1.1

* Added nexus Id to config file
* Fixed issue with being able to remove death pin - was preventing new death pins from appearing. As of now it cannot be removed.
* Fixed issue with pins not reappearing around character after log out and back in

#### 1.1.0

* Fixed issue with cloudberries not following config options to turn on/off
* Fixed issue with being able to remove starting pin showing where the boss mounting racks are
* Stopped pins from appearing in dungeons

#### 1.0.9

* Reduced min range to 5
* Added Serpent tracking

#### 1.0.8

* Fixed issue with checking off pins (if it appears behind the current pin, you have more than one pin in that location. Remove the 'X' and right click to remove a pin, then try again.)
* Fixed issue with Pin Not saving correctly after the Range functionality was added

#### 1.0.7

* Slight change around the filter code to potentially stop from encountering a NulLReferenceException.

#### 1.0.6

* Changed the /AMP-Clear console command to accept a single pin name so you can clear specific types of pins.
* Added /AMP-FilterList to list the currently filtered pins.


#### 1.0.5

* Added console command to clear all saved pins.
* Added console command to clear all AMP pins (temporary pins will come back once you start moving).
* Added console command to filter pins (current session only, all pins will be visible once you log out and back in).
* Added Leviathans & Flametal.

Right clicking a pin now removes it correctly, if it is within range of your character.  The default way the game was designed to handle this was to check if the pin saved or not, and if it was saved, then it would remove. Since the temporary pins are not, by default, being saved, it wouldn't attempt to remove it, but moving out of range would cause the pin to remove.

Some small optimization tweaks to how pins are updated when loading in.  This may have an impact for some people with weaker machines.

#### 1.0.4

More updates to the optimizations for the pinRange feature.  Hopefully these make a difference and don't have such a large impact on performance.
If you encounter a large cluster of pins in one area, you may still see some drops, however once it has finished processing them initially, it should clear up anytime you go back to that area.

Also added a configuration option to allow you to define your own name for each pin type.

#### 1.0.3

Optimizations have been made to the pinRange feature added in 1.0.2. Please let me know if these have made any improvements in your FPS. I tested for about 30 minutes and didn't see any drops in frames.

#### 1.0.2

* Fixed issue with Troll Cave config entries being the same as the Dragon Egg entries.
* Fixed issue with character logging out then back in, not causing the pins to update to the proper icons.  They were showing the circle icon that appears when a character first logs into the game.

New Feature

* Pin Range Support. You can now specify how far away you want the pins to begin appearing/disappearing from your character.  Yes, this works both ways.  When you move within range of something, it will show a pin on your map, and when you move out of range of that item, the pin is removed (unless you've specified to save it).

The config has a min (10) and max (450) value specified.  450 is larger than the items actually begin appearing, they don't begin appearing until around the 150-200 mark, which is defined in the game and we can't control that. I went much higher than needed to ensure we were getting everything we could if people wanted to do so. If we find that 10 is still too large of a range, I can lower the min, but I wanted it to be a circle around the player, and not directly under the player, otherwise you'd never see the items popping up on your map.


#### 1.0.1

* Ability to save pin was added.  
It should also reload and update the icon to the sprite that the mod uses.  As long as the pin was created by the mod. This will NOT update any existing pins to use the sprites in this mod.

New pins added

* Red Mushrooms
* Carrot Seeds
* Turnip Seeds
* Troll Caves
* Burial Chambers
* Sunken Crypts
* Fire Holes (Surtling spawners in swamps)
* Draugr Spanwers
* Skeleton Spawners
* Grewarf Spawners
* Muddy piles in Swamps (Iron)

You will see configuration options for Serpent spawns, however that is not currently functional. It is unable to locate the actual name for the serpent spawners.  I left the configure options in so that it would become active once I get it working correctly. 

There is also a configuration option for pinRange.  That is a work in progress as well.  The original version of it wasn't working as intended, so the code behind it was removed, but I left the configuration option, as sort of a sneak peak into what is coming!

Also, the only new icons that were added, were the in game sprites.  I have not added any colored pins (Icon option 2). If anyone is using these, let me know and I will work on getting them updated. 
I'm actually thinking of removing this option completely and just leave it using the in-game sprites. So please, if anyone uses the colored pins let me know.

#### 1.0.0

* Initial release