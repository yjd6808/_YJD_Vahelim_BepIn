# Freefly

A simple mod that enables freefly, a feature which is originally only accessible via cheatmode.

This is a great feature for screenshots and video's so I wanted it to be accessible for everyone, therefore, you can use it on multiplayer servers or singleplayer.

Here is a small [video](https://streamable.com/fcr4x8) I created by using the freefly feature. I hope freefly will be useful for you like it was for me. :)

## Controls
Default keybinds can be edited in the config file `BepInEx/config/Slinky_Freefly.cfg` after the initial load of the mod.

|Control|Feature|
|---|---|
|F10|Toggle Freefly|
|Page Up|Increase Camera Smoothness|
|Page Down|Decrease Camera Smoothness|
|Scroll Wheel|Increase/Decrease Camera Speed|
|Left Click|Lock camera to a target|
|Right Click|Screenshot|
|JoyTabRight (Controller?)|Increase FOV|
|JoyTabLeft (Controller?)|Decrease FOV|

Most of these are the default game binds which I may add an option to the config file in the future.

## Installation (manual)

If you are installing this manually, do the following

1. Extract the archive into a folder. **Do not extract into the game folder.**
2. Move the contents of `plugins` folder into `<GameDirectory>\Bepinex\plugins`.
3. Run the game.


## Changelog
##### 1.0.0
- Initial release
##### 1.0.1
- Fixed an issue where you could not interact with anything, noobie mistake by using the wrong patch method, sorry!
- Made it keycode based rather than string input.


### Credit

I'd like to say a big thank you to @MrPurple6411 for providing the community with an easy to get started template for modding Valheim, can be found in the [Valheim Modding Discord](https://discord.gg/RBq2mzeu4z).