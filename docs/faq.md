---
layout: default
title: Frequently Asked Questions
nav_order: 3
---

# Frequently Asked Questions

### How do we claim a location?
> Press U, strategic tab, there should be 'claim' button.

### How do I open build menu?
> You must be at an owned location, indicated at the top of the screen, then use mouse wheel (action) menu option.

### What is "attach to garrison" for? 
> Use it to manually take "ownership" of a vehicle. It must be used at an owned location. Use it on crates that contain building resources to gain access to them in the build menu. Normally all items will be automatically attached to the nearest garrison.

### Are there any air units in the mission?
> Not yet

### What mods do I need to play this faction?
> [All are listed here](https://vindicta-team.github.io/Vindicta-Docs/factions.html)

### How do I unlock items in the Arsenal?
> You can't, it is fully limited.

### How do I skip time?
> This isn't officially supported as it can screw with the enemy commander somewhat. However `skipTime 8` will skip 8 hours for you. The enemy commander will immediately dispatch all pending actions, other weird things might happen.

### How do I get building resources? 
> From ammoboxes found in enemy [police](guide/police) stations and [military locations](guide/military-locations), and from [supply convoys](guide/military#supply-convoy).

### What mods are compatible?
> Those which are ran on the dev server are officially supported, all others are not (even though they may work without problems). 

### Where do I find the .RPT file?
> Paste in explorer: `%LOCALAPPDATA%/Arma 3` (see [reporting-a-problem](reporting-a-problem))

### Will there be singleplayer mode?
> It is implemented already, but not well tested. Dedicated MP is best, self hosted MP is second best.

### I can't find the mission in game??
> Host a MP game:
> ![Screenshot](https://cdn.discordapp.com/attachments/553300822583279616/666270214983254044/unknown.png)
> If it's not there, make sure you've loaded CBA and ACE.
> See [troubleshooting](troubleshooting).

### How can I holster my pistol?
> Press 0 (zero key) to use the ACE holster weapon action.

### How can I skip time?
> This isn't recommended as the delayed actions and intel timestamps the AI uses will be invalidated, however you can use server `skipTime` command if necessary (expect interesting results).

### How do I run it on a dedicated server?
> If you have got the files from Workshop, then you have addon-type .pbo files, not user-mission-type .pbo files.  
> You DO NOT need to put them into mpmissions folder.  
> Make sure the addon is loaded! Treat the workshop download as an addon, it must be loaded with -mod parameters, clients need it to play on your server!  
> See the server.cfg setup below: note that versions might be different!  
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

### Headless Client Support?
> Not now because it would require large scale code changes. Maybe later.

### Where are the saved games stored?
> In the `vars.arma3profile` file (see [reporting-a-problem](reporting-a-problem))

### When?
> When it's done

### How often?
> As often as it's done
