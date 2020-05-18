---
layout: default
title: Setup Guide
nav_order: 2
---

# Setup Guide

## Dedicated Server

**Don't just blindly copy this, make sure your paths, mod, config names, and version numbers are correct. This is just an example!**  
For automatic loading and starting of the mission you need to enable persistent battle field (`persistent = 1;`) in the config file, and pass `-autoInit` on the command line.  
You should also enable `Auto Load`, `Auto Save`, and `Suspend when empty` in Addon Options (make sure you set them in the Server section):  
![image](https://user-images.githubusercontent.com/1453936/80655533-d145ad80-8a76-11ea-8064-a8aebc92fbac.png)  
![image](https://user-images.githubusercontent.com/1453936/80655245-13baba80-8a76-11ea-880f-beeb5fab635b.png)  
![image](https://user-images.githubusercontent.com/1453936/80655274-2503c700-8a76-11ea-830f-2622e718bbc3.png)  

### Command line

An example command line when using [FASTER Arma Server Tool](https://github.com/Foxlider/Fox-s-Arma-Server-Tool-Extended-Rewrite):  
```"C:\FASTER\Arma3\arma3server_x64.exe" -port=2302 "-config=C:\FASTER\Arma3\Servers\vindicta\vindicta_config.cfg" "-profiles=C:\FASTER\Arma3\Servers\vindicta" -name=vindicta "-mod=@ace;@vindicta;" "-serverMod=@ace;@CBA_A3;@vindicta;" -autoInit```

### Example config file (`vindicta_config.cfg`)

Note: you may need to modify the template below (`Vindicta_Altis_v0_37_11.Altis`) for your own purposes.
Change the version number to match the version you are using. Look at the file names in the mod `addons` directory to determine what version you are using.  
Change the map name to the map you want to play.
The template format is like this: `Vindicta_(map)_v(version).(map)`

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
	class Vindicta
	{
		template = Vindicta_Altis_v0_42_16.Altis;
		difficulty = "recruit";
	};
};
```

