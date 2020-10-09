---
layout: default
title: Dedicated Server Setup Guide
nav_order: 2
---

# Setup Guide

## Dedicated Server

Most important thing to understand is that **the files you get through workshop are an arma mod, not a plain mission.**

**There is no file which you must put into mpmissions folder in order for your server to run it.**

**Instead you just need to load Vindicta as a mod through -mod command line parameter, and that's it!**

**Clients need the addon to play on your server too! DO NOT load it as sever-side mod.**

If you absolutely need the mission pbo files and the way above does not work for you, you can get the mission files at our [github releases page](https://github.com/Sparker95/Vindicta/releases). **But you and all clients must load the addon anyway**.

**Don't just blindly copy this, make sure your paths, mod, config names, and version numbers are correct. This is just an example!**  
For automatic loading and starting of the mission you need to enable persistent battle field (`persistent = 1;`) in the config file, and pass `-autoInit` on the command line.  
You should also enable `Auto Load`, `Auto Save`, and `Suspend when empty` in Addon Options (make sure you set them in the Server section):  
![image](https://user-images.githubusercontent.com/1453936/80655533-d145ad80-8a76-11ea-8064-a8aebc92fbac.png)  
![image](https://user-images.githubusercontent.com/1453936/80655245-13baba80-8a76-11ea-880f-beeb5fab635b.png)  
![image](https://user-images.githubusercontent.com/1453936/80655274-2503c700-8a76-11ea-830f-2622e718bbc3.png)  

### Command line
An example command line with -mod and -servermod values:
```"-mod=@CBA_A3;@ace;@Vindicta (alpha)" "-servermod=@filext"
```

### FileXT addon
FileXT is an optional addon which lets your server store saved games in separate files. It must be launched with -servermod command. Please read more on it here:
[FileXT addon](https://vindicta-team.github.io/Vindicta-Docs/alt-save-game-storage.html)

### server.cfg example

**Check FOR_DEDICATED_SERVER_CFG.TXT file in Vindicta mod folder for examples for `class Missions` for server.cfg.**
**It has auto generated template= values for all map variants. This should be your main reference for these values.**

Change the map name to the map you want to play.
The template format is like this: `Vindicta_(map).(map)` (but again, consult the file mentioned above).

```
passwordAdmin = "windicta";
password = "";
serverCommandPassword = "";
hostname = "vindicta";
maxPlayers = 32;
kickduplicate = 0;
upnp = 0;
allowedFilePatching = 0;
verifySignatures = 2;
disableVoN = 0;
vonCodecQuality = 3;
vonCodec = 1;
BattlEye = 0;
persistent = 1;
motd[]= {
	""
};
motdInterval = 5;
allowedVoteCmds[] = {};
allowedVotedAdminCmds[] = {};
voteMissionPlayers = 1;
voteThreshold = 0;
logFile = "server_console.log";
doubleIdDetected = "";
onUserConnected = "";
onUserDisconnected = "";
onHackedData = "";
onDifferentData = "";
onUnsignedData = "";
regularCheck = "";
admins[]= {
	""
};
timeStampFormat = "none";

class Missions
{
  class vindicta_altis
  {
    template = vindicta_altis.altis;
    difficulty = "veteran";
    class Params {};
  };
};
```

