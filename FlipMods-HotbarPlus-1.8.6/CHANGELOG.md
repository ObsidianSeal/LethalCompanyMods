# 1.8.6
+ Updated assembly references for v73.

# 1.8.5
+ Quick dropping should trigger for more actions, such as despawning/destroying.<br>
This should now trigger when storing items into the ship via the [ShipInventoryUpdated](https://thunderstore.io/c/lethal-company/p/LethalCompanyModding/ShipInventoryUpdated/) mod, for example.

# 1.8.4
+ Added a testing config that should fix a vanilla bug for non-host clients when placing items into a storage container and immediately picking that item up again.<br>
This option is disabled by default for now, but this will be enabled by default after a testing period, but this fix is not a complicated patch, so it *shouldn't* cause problems.<br>

<h4>Specific details that no one asked for</h4>

When dropping items onto the ground, the game will normally prevent you from picking up items from any source until after the host acknowledges to prevent desync.

This same behaviour does not occur, however, when placing items into a storage container for whatever reason, so if you place an item into a storage container, you can technically pick that same item up immediately and if you do so before the host acknowledges that you even placed it in there, de-sync will occur, and cause you to drop all items you're holding, and they may not be able to be grabbed again.

# 1.8.3
+ Fixed issue with the lightning warning icon for metallic objects not appearing for non-host clients.

# 1.8.2
+ The item quick drop feature now has a priority system. The highest item priority will be swapped to. Scrap will be prioritised first. Scrap that are not weapons will be even higher priority. Each priority will then be slightly offset by item weight to prioritize the heaviest items.

# 1.8.1
+ Fixed an issue where the lightning warning icon wouldn't disappear from the hotbar slot if you entered the factory before the lightning struck.

# 1.8.0
+ Added the option to purchase item slots!
+ You can set how many slots you want to be purchasable. (host-only)
+ You can specify the price for additional hotbar slots, as well as the price increase for each additional item slot purchased after the first.<br>
Example: First purchase: 200 credits, Second: 300 credits, Third: 400 credits, etc.
+ Added more code for syncing already held objects to ensure held objects past inventory slot 4 will be synced with all players, as well as each player's currently selected inventory slot. The vanilla game only syncs the first 4 inventory slots.
+ Fixed bug where *sometimes* quick swapping inventory slots with hotkeys (1, 2, 3, etc) wouldn't always swap to the correct slot for other players.

# 1.7.6
+ Disabled the center UI fix, as it's not needed anymore in V64.

# 1.7.5
+ Updated mod description for latest update compatibility.

# 1.7.4
+ Added project to github.
+ Added the github link to the website/manifest.

# 1.7.3
+ Optimized some code to help reduce lag in the lightning indicator patch.

# 1.7.2
+ Slight tweaks to potentially help prevent conflicts with the renamed asset bundle conflicting with cached files from the previous asset bundle.

# 1.7.1
+ Renamed asset bundle to be more unique, and hopefully prevent some issues.

# 1.7.0
+ Added lightning warning indicators for item icons when a held metal object is about to be struck by lightning.<br>
This can be disabled in the config.

# 1.6.8
+ Added config option to enable/disable verbose logs.
+ If verbose logs are enabled, the mod will log when it blocks the user from swapping items to help determine if issues related to not being able to swap items are caused by this mod or not.<br>
This will not spam more than once per second.

# 1.6.7
+ The UI will again, update after closing the menu while in game. This will apply any changes made to the UI settings in the config, if editing the config in game via a mod, such as LethalConfig.<br>
The error(s) caused by doing this in 1.6.5 has been fixed.

# 1.6.6
+ The UI will (temporarily) no longer update to after closing the menu to prevent errors spamming in the console when setting a custom amount of item slots.<br>
This will remain until I can fix the error.<br>
In the meantime, to manually update your UI settings in the config, I suggest leaving the lobby and rejoining.

# 1.6.5
+ Added extra checks to *maybe* prevent some errors. Added more logs.
+ The energy bar should now automatically scale in size with the hotbar size.
+ Tweaked the UI scaling to be more consistent, and probably more friendly with other mods, such as the ReservedItemSlot mods.

# 1.6.4
+ Fixed copied item slot frames not animating.
+ Added fixes to recenter the inventory UI, and maintain the position through all window sizes. This can be disabled in the config in case of mod conflicts.<br>
Previously, the inventory UI elements were not guaranteed to be centered, and may be shifted left (or right) on certain window sizes/aspect ratios. This should keep the UI centered now.

# 1.6.3
+ Added extra checks to ensure that copied item slots in the HUD copy the texture and material as well, in case they do not.<br>
This should resolve some issues with mods who have custom textures for the item slot frames.

# 1.6.2
+ Can now swap hotbar slots while emoting (even with TooManyEmotes) by using the quick item swap hotkeys.

# 1.6.1
+ Fix for incorrect rotations on some energy bars.
+ Fix for UI elements not adjusting correctly when changing the config UI settings in-game.

# 1.6.0
+ Added energy bars for each item slot which displays the current battery level for the item in that slot. These will be hidden if the slot is empty, or if the item in the slot does not require a battery.
+ Upon closing the quick menu, any changes made to the HUD config entries will be applied to the UI automatically without needing to restart the game.

# 1.5.11
+ Revised an old section of code to prevent potential lock-ups.

# 1.5.10
+ You can now quick swap hotbar slots with the number keys while emoting, except when emoting with TooManyEmotes, unless the config in TooManyEmotes allows moving while emoting.

# 1.5.9
+ Added extra check to when you can swap item slots with the number keys. You cannot swap while emoting, or if you're dead.

# 1.5.8
+ Disabled item quick swapping when General Improvements is enabled because this causes some issues.
+ Fixed quick switching with the number keys to be compatible with clients without this mod.

# 1.5.7
+ Config sync should now regenerate correctly every time you load into a game, rather than only the first time.

# 1.5.6
+ Forgot to add to the previous changelog that quick item swapping now won't work while typing.

# 1.5.5
+ Fixed issue with quick drop not working again. (this feature will haunt me, I swear)

# 1.5.4
+ Added checks if currently dropping an object on the server before allowing the quick item swapping hotkeys.

# 1.5.3
+ Fixed quick drop delay bug that was making items disappear on non-host clients when they dropped items. (sometimes) Sorry for the recent de-sync issues!

# 1.5.2
+ Re-enabling quick item drop. Still may cause de-sync if the host doesn't have the mod.

# 1.5.1
+ Disabling the numeric hotbar shortcuts in the config should now work correctly, even with InputUtils enabled.

# 1.5.0
+ Added support for InputUtils, as a soft dependency. If this mod is enabled, you will be able to access any relevant hotkeys within the game's keybind menu.

# 1.4.8
+ Fixed issue with custom keybinds for the default emotes not working.

# 1.4.7
+ Improved stability and fixed some potential issues of desync.

# 1.4.6
+ Accidentally broke numerical hotkeys for swapping hotbar slots. Fixed now.

# 1.4.5
+ Reverting quick item drop again until I can fix the de-sync issues it's causing.

# 1.4.3
+ Picking up two handed items will now unfade your inventory hud.
+ Added configs to disable the faster item swapping, faster item dropping, and faster item activating. The intervals between these actions will be set to vanilla.

# 1.4.2
+ Fixed issue with non-host clients using their set amount of hotbar slots in the config when host does not have the mod.

# 1.4.1
+ Forgot to update the README.

# 1.4.0
+ Re-added quick item drop (chain dropping)
+ Added option to override the alpha for inventory hud fade. Can be set to 0 to fade all the way, or 1 to never fade. Vanilla is 0.13
+ Added the option to override the hotbar slot spacing to make the icons further apart, or closer together. Vanilla value is 10.
+ Added the option to override the hotbar slots size/scale. This option will automatically adjust the vertical position and spacing.

# 1.3.5
+ Re-added the reversing hotbar swapping in the config since the new vanilla setting for this also reverses the terminal scrolling.

# 1.3.4
+ Adjusted config to allow not using this mod's rebinds for the default emotes.

# 1.3.3
+ Various fixes.
+ Removed setting for reversing hotbar swapping since it's in the game now.

# 1.3.2
+ Fixed bug with "fixed" emote rebinds not working.

# 1.3.1
+ Updated to support new game update

# 1.3.0
+ Forgot to update the dll.

# 1.2.9
+ Fixed the issue preventing players from using their hotkeys to swap hotbar slots, or emoting with the rebound keys.

# 1.2.8
+ Fixed an issue where the mod would complain about reloading the config before it was created.

# 1.2.7
+ Disabling item quick drop until I fix the desync issues.

# 1.2.6
+ Old configs shouldn't persist anymore.
+ Selecting a lower amount of hotbar slots than the default 4, in the config, should now work without issues.
+ You shouldn't be able to use the numerical hotkeys to swap hotbar slots while carrying a two-handed object.

# 1.2.5
+ All clients will now sync the number of hotbar slots with the host.<br>
If the host has the number of hotbar slots set to 4 in their config, then other clients with the mod will also have 4 hotbar slots, regardless of their config settings.

# 1.2.4
+ Fix some sync issues.
+ Fixed a bug that caused pressing escape to tab in the terminal to open the menu.

# 1.2.3
+ The sync was previously only syncing to the host. It should sync between everyone properly now.

# 1.2.2
+ Synced hotbar swap slots with all clients. This will work with any hotbar size.

# 1.2.1
+ Minor fixes

# 1.2.0
+ First attempt at chain dropping items. Will tweak animation a bit to look smoother soon.

# 1.1.2
+ Emotes weren't rebinding correctly. Should be good now.

# 1.1.1
+ Fixed BepInEx dependency

# 1.1.0
+ Initial release