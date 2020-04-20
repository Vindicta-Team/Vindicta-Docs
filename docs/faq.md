---
layout: default
title: Frequently Asked Questions
nav_order: 3
---

# Frequently Asked Questions

# Mods

### What mods are compatible?
> Those which are ran on the dev server are officially supported, all others are not (even though they may work without problems). 

### What mods are incompatible?
> All AI mods are incompatible, for instance VCOM AI. Only exception is mods which do not make bots steal vehicles and do not change their weaypoints (for instance, LAMBS danger.fsm). If you play with any AI mods, do not report any AI related problem.

### What mods do I need to play with a specific faction?
> [All are listed here](https://vindicta-team.github.io/Vindicta-Docs/factions.html)

# Gameplay and current features

### How do we claim a location?
> Press U, strategic tab, there should be 'claim' button.

### How do I open build menu?
> You must be at an owned location, indicated at the top of the screen, then use mouse wheel (action) menu option.

### What is "attach to garrison" for? 
> Use it to manually take "ownership" of a vehicle. It must be used at an owned location. Use it on crates that contain building resources to gain access to them in the build menu. Normally all items will be automatically attached to the nearest garrison.

### Are there any air units in the mission?
> Not yet

### How do I unlock items in the Arsenal?
> You can't, it is fully limited.

### How do I skip time?
> This isn't officially supported as it can screw with the enemy commander somewhat. However `skipTime 8` will skip 8 hours for you. The enemy commander will immediately dispatch all pending actions, other weird things might happen.

### How do I get building resources? 
> From ammoboxes found in enemy [police](guide/police) stations and [military locations](guide/military-locations), and from [supply convoys](guide/military#supply-convoy).

### How do I play the mission in singleplayer?
> It is implemented already, you can play it in singleplayer through SP Scenarios tab in the main menu. But it is not well tested. Dedicated MP is best, self hosted MP is second best.

### How can I holster my pistol?
> Press 0 (zero key) to use the ACE holster weapon action.

# Zeus

### How can I open Zeus interface?
> You can use ACE Zeus feature. Make sure it is setup correctly, for that go to eskape/Addon Options/ACE Zeus and enable it there. After that you can access Zeus by using ACE self interaction/Create Zeus button, and pressing Y after that.

### Are vehicles created with Zeus saved?
> No they are not saved.

### Is it possible to save vehicles created with Zeus by running extra code in console or other methods?
> No, because our framework is based on strict enumeration of unit types, therefore it can only operate with units created by our own framework.

### Is it likely that this problem will be solved in the future versions?
> No, it is very unlikely.

# Future features

### Will there be money, economics, or factories to build vehicles or weapons?
> No, features of this kind are totally not in our plan.

### But another mod/scenario has a feature ...
> We don't aim to have as many features as possible. Our main focus is the military part of the game.

# Technical

### Is there Headless Client Support?
> Not now because it would require large scale code changes. Maybe later.

### Where are the saved games stored?
> In the `vars.arma3profile` file (see [reporting-a-problem](reporting-a-problem))

### How do I run it on a dedicated server?
> If you have got the files from Workshop, then you have addon-type .pbo files, not user-mission-type .pbo files.  
> You DO NOT need to put them into mpmissions folder.  
> Make sure the addon is loaded! Treat the workshop download as an addon, it must be loaded with -mod parameters, clients need it to play on your server!  
> If you want your dedicated server to automatically select the mission when first player joins, you can use the `class Missions` below. It is only needed if you want automatic mission selection. If you do not add `class Missions` to server.cfg, you will see a usual mission selection screen. When doing a dedicated server setup, try it without `class Missions` first to see if all mods are loaded, then, if you want, you can try to do `class Missions` setup.
> See the server.cfg setup below: note that versions might be different! Ensure that versions are correct! To see the version which must be specified, go to `!Workshop\Vindicta (Alpha)\addons` folder and locate the .pbo file which has the version name in it.
> Ensure that specified `template` is correct, note that the map name is listed twice!
> ```cpp
> class Missions
> {
>     class vin001
>     {
>         template = "Vindicta_Altis_v0_37_11.Altis";
>         difficulty = "veteran";
>         class Params {};
>     };
>     class vin002
>     {
>         template = "Vindicta_Enoch_v0_37_11.Enoch";
>         difficulty = "veteran";
>         class Params {};
>     };
> };
> ```  

### Where do I find the .RPT file?
> Paste in explorer: `%LOCALAPPDATA%/Arma 3` (see [reporting-a-problem](reporting-a-problem))

# Common issues

### I can't find the mission in game
> Host a MP game:
> ![Screenshot](https://cdn.discordapp.com/attachments/553300822583279616/666270214983254044/unknown.png)
> If it's not there, make sure you've loaded CBA and ACE.
> See [troubleshooting](troubleshooting).

# Other questions

### When?
> When it's done

### How often?
> As often as it's done
