# Setting up Minecraft Server

Assuming Docker Desktop has been installed via `winget install Docker.DockerDesktop`, run the following command to start a server:

```ps1
docker run -d -it -e EULA=TRUE -e GAMEMODE=creative -e DEFAULT_PLAYER_PERMISSION_LEVEL=operator -e DIFFICULTY=peaceful -e ALLOW_CHEATS=true -e VIEW_DISTANCE=1000 -p 19132:19132/udp -v mc-bedrock-data:/data itzg/minecraft-bedrock-server
```

To go to the volume where the container is located, go to the following directory.

```ps1
cd \\wsl$\docker-desktop-data\data\docker\volumes
```

If you need to change the game mode, you may need to remove the docker volume:

```ps1
docker volume rm mc-bedrock-data
```
