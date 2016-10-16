| > [ReadMe](../../README.md) > [Table of Contents](../TOC.md)|
|-|

# MinecraftEdu Server Image
This image is used to create MinecraftEdu servers.

## Basic Usage
```bash
docker run -it stormymcstorm/mercury-edu-server
```

## Enviorment
* `-e MINECRAFT_MEM=` set the amount of memory the server can use. Default: 1024M
* `-e ALIAS_PROTECTION=` When students are joining the server, should they have the possibility to password protect their aliases. Default: false
* `-e KICK_IDLE_OPS=` Should we also kick idle ops (teachers) out from the server. Default: false
* `-e KICK_IDLE_PLAYERS=` Should we kick players who are idle for certain time in the server. Default: false
* `-e KICK_IDLE_PLAYERS=` Should we kick players who are idle for certain time in the server. Default: false
* `-e KICK_IDLE_PLAYERS_INTERVAL=` Time (in minutes) how long user needs to be idle before he is kicked from the server. Default: 5
* `-e LOADED_SAVED_MAP=` Used by server launcher to determine the map to load. Default: ""
* `-e LOG_IDLE_PLAYERS=` Should we log a entry in server log file if a player is idle. Default: false
* `-e RESTRICT_NEW_USERS=` When student is joining, should we also check that the user's alias is already known in the server. Any new users could then not join the server if enabled. Links to alias-protection setting. Default: false
* `-e SAVED_MAP_NAME=` Used by Server Launcher to name the world
* `-e SERVER_LANGUAGE=` Server Launcher and Server language. Set from the application, do not modify. Default: en_US
* `-e STORE_PLAYERS_WITH_ALIAS=` If true, user data is being stored in the server using usernames. Otherwise with user aliases. Default: false
* `-e TAKE_BACKUPS=` Should we take backups of the worlds launched using the Server Launcher in folder servertool/worlds/backups. Default: true
* `-e TEACHER_PASSWORD=` The teachers password this is automatically hashed on store. Default: "password"
* `-e WRITE_DEBUG_LOG_TO_FILE=` If true, all console messages will be written in minecraftedu/debug folder. Default: true

## Volumes
The server files are stored in `/data`. Use `-v /path/to/directory:/data`.

## Resources
* [MinecraftEdu ](http://services.minecraftedu.com/wiki/Main_Page)
* [MinecraftEdu Server Doc](http://services.minecraftedu.com/wiki/Server)
* [Minecraft Wikia](http://minecraft.gamepedia.com/Minecraft_Wiki)
* [Minecraft Server commands](http://minecraft.gamepedia.com/Commands)

## Server Folder Structure
```
data
├─ ServerWizard.jar
├─ launcher_res
│  └─ settings
│     ├─ edukeybindings.ini
│     └─ launchersettings.ini      
├─ server
│  ├─ banned-ips.json
│  ├─ banned-players.json
│  ├─ eula.txt
│  ├─ minecraft_server.1.7.10.jar
│  ├─ minecraft_server.jar
│  ├─ minecraftedusettings.ini
│  ├─ ops.json
│  ├─ server-icon.png
│  ├─ server.properties
│  ├─ usercache.json
│  ├─ usernamecache.json
│  ├─ whitelist.json
│  ├─ config (mod config files)
│  │  └  ...
│  ├─ mods
│  │  └─── 1.7.10
│  │       └  ...
│  ├─ logs
│  │  └  ...
│  └─ libraries
│     └  ...
├─ settings
│  ├─ allowedstudentscommands.txt
│  ├─ bannedservercommands.txt
│  ├─ reserved_aliases.ini
│  └─ serverwizardsettings.ini
├─ backups (world backups)
│  └   ...
├─ debug (debug logs)
│  └   ...
├─ lib
│  └   ...
└───worlds
```
