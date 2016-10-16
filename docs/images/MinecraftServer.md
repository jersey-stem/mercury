| > [ReadMe](../../README.md) > [Table of Contents](../TOC.md) |
|:---:|

# Minecraft Server Image
This image is used to create Minecraft servers.

## Basic Usage
```bash
docker run -it stormymcstorm/mercury-mc-server
```

## Enviorment
* `-e MINECRAFT_MEM=` set the amount of memory the server can use. Default: 1024M

## Volumes
The server files are stored in `/data`. Use `-v /path/to/directory:/data`.

## Resources
* [Minecraft Wikia](http://minecraft.gamepedia.com/Minecraft_Wiki)
* [Minecraft Server commands](http://minecraft.gamepedia.com/Commands)

## Server Folder Structure
```
data
├─ banned-ips.json
├─ banned-players.json
├─ eula.txt
├─ ops.json
├─ server.jar
├─ server.properties
├─ usercache.json
├─ whitelist.json
├─ logs
│  └─ ...  
└─ world
   └─ ...
```
