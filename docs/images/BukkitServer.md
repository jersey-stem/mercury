| > [ReadMe](../../README.md) > [Table of Contents](../TOC.md)|
|-|

# Bukkit Server Image
This image is used to create Bukkit servers.

## Basic Usage
```bash
docker run -it stormymcstorm/mercury-bukkit-server
```

## Enviorment
* `-e MINECRAFT_MEM=` set the amount of memory the server can use. Default: 1024M

## Volumes
The server files are stored in `/data`. Use `-v /path/to/directory:/data`.

## Resources
* [Minecraft Bukkit](https://bukkit.org/)
* [Minecraft Spigot](https://www.spigotmc.org/)
* [Minecraft Wikia](http://minecraft.gamepedia.com/Minecraft_Wiki)
* [Minecraft Server commands](http://minecraft.gamepedia.com/Commands)

## Server Folder Structure
```
data
├─ banned-ips.json
├─ banned-players.json
├─ bukkit.yml
├─ commands.yml
├─ eula.txt
├─ help.yml
├─ ops.json
├─ permissions
├─ server.jar
├─ server.properties
├─ spigot.yml
├─ usercache.json
├─ whitelist.json
├─ plugins
│  └─ ...
├─ logs
│  └─ ...
├─ world_nether
│  └─ ...
├─ world_the_end
│  └─ ...  
└─ world
   └─ ...
```
