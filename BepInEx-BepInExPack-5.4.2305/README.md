![BepInEx logo](https://avatars2.githubusercontent.com/u/39589027?s=256)

# BepInExPack

This is [BepInEx 5.4.23.5](https://github.com/BepInEx/BepInEx) pack.

The exact version is `BepInEx_win_x64_5.4.23.5.zip` from https://github.com/BepInEx/BepInEx/releases/tag/v5.4.23.5

BepInEx is a general purpose framework for Unity modding.
BepInEx includes tools and libraries to

* load custom code (hereafter *plugins*) into the game on launch;
* patch in-game methods, classes and even entire assemblies without touching original game files;
* configure plugins and log game to desired outputs like console or file;
* manage plugin dependencies.

BepInEx is currently [one of the most popular modding tools for Unity on GitHub](https://github.com/topics/modding?o=desc&s=stars).

## This pack's contents

This pack is preconfigured and usable for Unity games that use Mono.
In particular, this pack comes with preconfigured `BepInEx.cfg` that enables the BepInEx console and more extensive logging.

## Installation (game, automated)

This is the recommended way to install BepInEx on the game.

1. Download and install [Thunderstore Mod Manager](https://www.overwolf.com/app/Thunderstore-Thunderstore_Mod_Manager) or another compatible mod manager.
2. Click **Install with Mod Manager** button on top of the page.
3. Run the game via the mod manager.

## Installation (manual)

If you are installing this manually, do the following:

1. Extract the archive into a folder. **Do not extract into the game folder.**
2. Move the contents of `BepInExPack` folder into the game folder (where the game executable is located).
3. Run the game. If everything runs correctly, you will see BepInEx console pop up on your desktop.

## Useful links

* [BepInEx: writing basic plugin walkthrough](https://docs.bepinex.dev/articles/dev_guide/plugin_tutorial/index.html)
* [BepInEx: useful plugins for modding](https://docs.bepinex.dev/articles/dev_guide/dev_tools.html)
* [BepInEx: patching game methods at runtime](https://docs.bepinex.dev/articles/dev_guide/runtime_patching.html)

## Issues, questions, etc.

At this moment, you can use the following channels to ask for help:
* [Thunderstore Discord](https://discord.com/invite/UWpWhjZken) -- **Primarily for when BepInEx is installed through Thunderstore Mod Manager**
* [BepInEx Discord](https://discord.gg/MpFEDAg) -- **Only for technical support for BepInEx itself. No support for mods / plugins.**
