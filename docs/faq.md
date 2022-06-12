---
layout: default
title: Frequently Asked Questions
nav_order: 3
---

# Frequently Asked Questions

### What is the current state of development?
> Project development is stopped and no more new features are planned. Bug fixes are possible, and pull requests are welcome.

# Mods

### What mods are incompatible?
> All AI mods are incompatible, for instance VCOM AI, LAMBS danger.fsm, etc. Only exception is mods which do not make bots steal vehicles and do not change their weaypoints (for instance, LAMBS suppression). Anyway we didn't test all AI mod combinations, so if you play with any AI mods, AI behaviour can break, for instance patrols might become alerted at enemies multiple kilometers away and run away from outposts, and so on.

### What mods do I need to play with a specific faction?
> [All build in factions are listed here](https://vindicta-team.github.io/Vindicta-Docs/factions/factions-list.html)

> [Addon factions are listed here](https://vindicta-team.github.io/Vindicta-Docs/factions/addon-factions-list.html)

# Gameplay and current features

### How do we claim a location?
> Press U, strategic tab, there should be 'claim' button.

### I can not enter military vehicles, why?
> You must lockpick them first. It is done through ACE interaction menu, with `Lockpick vehicle` action. You must have a lockpick item in your inventory, but it is always added to uniform at respawn.

### How do I open build menu?
> You must be at an owned location, indicated at the top of the screen, then use mouse wheel (action) menu option.

### What is "attach to garrison" for? 
> Use it to manually take "ownership" of a vehicle. It must be used at an owned location. Use it on crates that contain building resources to gain access to them in the build menu. Normally all items will be automatically attached to the nearest garrison.

### Are there any air units in the mission?
> There are only attack helicopters. No transport helicopters, drones, or airplanes.

### Can I fly helicopters?
> Yes you can, in version 0.55 anti-air vehicles were added and aircraft access restrictions were removed.

### Can I unlock items in the Arsenal?
> You can't, it is fully limited. However if you want to have more loot in ammo crates, you can increase it through addon options.

### How do I get building resources? 
> From ammoboxes found in enemy [police](guide/police) stations and [military locations](guide/military-locations), and from [supply convoys](guide/military#supply-convoy). Also civilians can give you the build resources through dialogue in cities with high enough influence.

### How do I play the mission in singleplayer?
> You can play it in singleplayer through SP Scenarios tab in the main menu. But it is not well tested. Dedicated MP is best, self hosted MP is second best.

### How can I holster my pistol?
> Press 0 (zero key) to use the ACE holster weapon action.

### Do enemy crates respawn after I steal them?
> No.

### Where are the APCs/Tanks/MRAPs?
> Heavier vehicles appear as you make more campaign progress. When this happens is also dependant on difficulty settings: at high difficulty tanks appear almost immediately, and low they will not appear until much later.

# Zeus

### How can I open Zeus interface?
> You can use ACE Zeus feature. Make sure it is setup correctly, for that go to eskape/Addon Options/ACE Zeus and enable it there. After that you can access Zeus by using ACE self interaction/Create Zeus button, and pressing Y after that.  Northen made a handy video:  
> <iframe width="560" height="315" src="https://www.youtube.com/embed/O_BB7hcIsJ8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen> </iframe>

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
> No now because it would require large scale code changes.

### Where are the saved games stored?
> If you are not using FileXT addon, they are stored in the `vars.arma3profile` file (see [reporting-a-problem](reporting-a-problem))

### Where do I find the .RPT file?
> Paste in explorer: `%LOCALAPPDATA%/Arma 3` (see [reporting-a-problem](reporting-a-problem))

# Common issues

### Why do my vehicles, cargo boxes or static weapons get teleported when I reload the game or come back to my camp?

> We cant have all objects present at all times for performance reasons.

> So we spawn/despawn (cache/unchace) them based on if there is a player in the area 

> However due to how arma itself works objects can easily glitch into each other and get destroyed if the are placed too close together.
 
> That is why we have a script that detects possible problems and solves them by moving the objects in question away from each other (and it usually places them on the nearest free space/road) 

> So objects will move when they were placed too close together before you leave the area but thats a lot better than having your stuff glitch around and blow up randomly which is very common in most arma missions and extremely annoying.

### How do I prevent vehicles, cargo boxes and static weapons from teleporting around at my camp?

> Don't put your vehicles, cargo boxes or static weapons close to other objects, including houses, fortifications, or anything at all.

### I can't find the mission in game
> Host a MP game:
> ![Screenshot](https://cdn.discordapp.com/attachments/553300822583279616/666270214983254044/unknown.png)
> If it's not there, make sure you've loaded CBA and ACE.
> See [troubleshooting](troubleshooting).

### Friendly or enemy AIs are misbehaving or stuck
> If you want to report AI errors, you need to use the built-in AI debugging interface. To do that, open Zeus interface, and find 'AI debug UI' button at the top-right. It is only available to admins. See the screenshots below for further instructions. Send us screenshots of the situation with the debugging menu enabled with as much data as possible.

[Screenshot 1](https://raw.githubusercontent.com/Vindicta-Team/Vindicta-Docs/master/images/ai_debug_0.jpg)  [Screenshot 2](https://raw.githubusercontent.com/Vindicta-Team/Vindicta-Docs/master/images/ai_debug_1.jpg)  [Screenshot 3](https://raw.githubusercontent.com/Vindicta-Team/Vindicta-Docs/master/images/ai_debug_2.jpg)  [Screenshot 4](https://raw.githubusercontent.com/Vindicta-Team/Vindicta-Docs/master/images/ai_debug_3.jpg)

### How can I help prevent my server from becoming overloaded?
> To see if your server is struggling to keep up, we can view the server's FPS (not the same as a client's FPS) using `#monitor 1`.  To use this command, you must be logged in as admin.  If a server FPS is > 45, you will not notice any overloading side effects.  When this value is < 45, you may start to see some side effects, and if it is < 20, you may notice significant side effects. 

> These side effects can range from a variety of symptoms.  Some common symptoms are: not being teleported off the initial spawn point for some time, AI spawning in front of you when you arrive at a location, AI not registering being hit for a few seconds after being shot, or your cars/objects placed at your camp not spawning in for significant periods of time.

> Thankfully, there are a few different ways to mitigate this issue.  Firstly, if you are playing with a group of people, try to keep everyone together in one or two groups.  When people are spread out, the server needs to load in more AI so everyone can see the types of people around them.  (Civilians, Police, Enemy Forces, Friendly Forces).  If you are already doing that, you may need to turn the spawning radius of AI down.  To do this, go to `Configure > Addon Options > Vindicta` and search for AI-to-AI spawn distance and Player-to-AI spawn distance.  Turn these values down to what you believe is reasonable; a recommended value is 800 for Player-to-AI and 500 for AI-to-AI.  This will allow players to see enemy AI from a fair distance out (although it may be too close to snipe AI with), and it allows AI to spawn far enough away to allow for more realistic firefights.

> If the server still faces severe overloading issues, then the player can also be strategic with where they send AI.  Trying to attack Enemy Forces on two fronts means two-times the number of AI is likely to be spawned at once.  Keeping the offensive focused on one front helps prevent too many AI from being spawned at one time.  In addition, it is also possible that the server itself is insufficient to run a game of Vindicita.  Arma is a very CPU-intensive game, with a preference for running off of a single-core on a processor, and even some modern cores cannot handle Arma's large requirements.

# Other questions

### When?
> When it's done

### How often?
> As often as it's done
