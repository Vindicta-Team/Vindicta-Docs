---
layout: default
title: Troubleshooting
nav_order: 2
---

# Troubleshooting

## In-game

### Threads Crash

This is reported by a red Critical notification, followed immediately by the creation of a recovery save.  
It represents a serious problem:

- Report it to us in discord so we can fix it for the next release.
- Restart your game from either the recovery save, or your last save. Your last save will be probably be 
  more reliable, as the data in the recovery one may already be corrupt.

### Server Under Heavy Load

This is reported by a System notification. It indicates that your server is having preformance problems, 
and is unable to keep up with the actions it is being asked to perform.  
There is no real solution to this other than improving the server, or reducing how much it is being asked to do:

- Somehow reduce how many units are spawned -- units spawn when other units they consider enemies, or players, 
  are within 1km range.
- Playing on a smaller map, e.g. Malden.
- Run a dedicated server -- if you are using self hosted MP, try and set up a dedicated server, even on the
  same machine as your client it will be an improvement.
- Save and reload won't help -- all messages that are waiting are saved as well, so you just get the same number 
  once you load again. But now it includes all the initialization and spawn requests added by loading code.

## Hosting

### Mission doesn't show up

- Check you installed as a mod *only*, nothing should go in the `mpmissions` directory.
- Check you installed the dependencies `ace` and `cba`.
- Check you enabled the dependencies.
- Check you don't have custom missions only displayed -- press the `Custom Missions` button.

## Dedicated Server

### It shows mission splash screen forever

- It won't start automatically unless you set up your server config file correctly -- instead 
  you can login as admin on the splash screen (`#login <password>`) and then open the missions screen
  (`#missions`).

### Saves disappeared

- Check your server doesn't clean your vars file.
- Check you didn't change profile.
