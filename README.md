##Direwolf20 Server Dockerfile

## What the purpose of this image is:
The purpose of this image is to provide a means of quickly creating a Minecraft Direwolf20 server.

## What this Docker Build does:
1. Sets environment variables for:
	Downloaded version of FTB Server
	The Launch Wrapper version

2. It then downloads the required version of Direwolf20 via curl. To change the version downloaded, simply replace DIREWOLF20_URL with the link to the version you want.

3. The image then unzips and installs, confirms the EULA and starts the server.

## Using this Image:

This image inherits usage features from dlord/minecraft. For full instructions, head to [the parent repository](https://github.com/dlord/minecraft-docker)

To create an instance of the server running in a container:
```
docker run \
    --name direwolf20 \
    -p 25565:25565 \
    -d \
    4lexnz/direwolf20
```

Seriously, there's a bunch more useful features that are inherited from the base image. Go check it out.