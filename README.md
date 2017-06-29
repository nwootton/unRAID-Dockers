# unRAID-Magic-Mirror-Docker
The XML file required to run the MagicMirror Docker under unRAID.

This uses the Docker image created by bastilimbach and referenced in the MagicMirror docs here https://github.com/MichMich/MagicMirror


## Installation
The my-MagicMirror.xml file needs to be copied to

```
/boot/config/plugins/dockerMan/templates-user
```

on the unRAID server. It should then appear in the available Docker modules and allow you to configure it to point to the location of your config and modules.

This is just a XML template based around the following Docker run command

```
docker run -d -p 8099:8080 --restart always \
-v /where/is/your/MagicMirror/config:/opt/magic_mirror/config \
-v /where/are/your/MagicMirror/modules:/opt/magic_mirror/modules \
--name magic_mirror bastilimbach/docker-magicmirror:latest
```
The config and modules are stored on the unRAID server and mapped across to the /opt/magic_mirror/*something* directories. Personally my unRAID is setup to use /mnt/cache/.app/docker/MagicMirror/ which is where all my Docker related stuff is stored. It also maps the default port of 8080 out to 8099, but that can be changed via the UI.

Icon made by RoundIcons from www.flaticon.com 
