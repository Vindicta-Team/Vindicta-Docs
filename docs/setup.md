---
layout: default
title: Setup Guide
nav_order: 7
---

# Setup Guide

## Dedicated Server

**Don't just blindly copy this, make sure your paths, mod, config names, and version numbers are correct. This is just an example!**  
For automatic loading and starting of the mission you need to enable persistent battle field (`persistent = 1;`) in the config file, and pass `-autoInit` on the command line.  

### Command line

An example command line when using [FASTER Arma Server Tool](https://github.com/Foxlider/Fox-s-Arma-Server-Tool-Extended-Rewrite):  
```"C:\FASTER\Arma3\arma3server_x64.exe" -port=2302 "-config=C:\FASTER\Arma3\Servers\vindicta\vindicta_config.cfg" "-profiles=C:\FASTER\Arma3\Servers\vindicta" -name=vindicta "-mod=@ace;@vindicta;" "-serverMod=@ace;@CBA_A3;@vindicta;" -autoInit```

### Example config file (`vindicta_config.cfg`)

Note: you may need to modify the template below (`Vindicta_Altis_v0_37_11.Altis`) for your own purposes.
Change the version number to match the version you are using. Look at the file names in the mod `addons` directory to determine what version you are using.  
Change the map name to the map you want to play.
The template format is like this: `Vindicta_(map)_(version).(map)`

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
		template = Vindicta_Altis_v0_37_11.Altis;
		difficulty = "recruit";
		class Params {};
	};
};
```
