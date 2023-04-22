# Setting up Minecraft Server

Assuming Docker Desktop has been installed via `winget install Docker.DockerDesktop`, run the following command to start a server:

```ps1
docker run -d -it -e EULA=TRUE -e GAMEMODE=creative -e DIFFICULTY=easy -e VIEW_DISTANCE=1000 -p 19132:19132/udp -v mc-bedrock-data:/data itzg/minecraft-bedrock-server
```
