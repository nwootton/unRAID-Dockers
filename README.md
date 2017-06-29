# unRAID-Magic-Mirror-Docker
The XML file required to run the MagicMirror Docker under unRAID.

This uses the Docker image created by bastilimbach and referenced in the MagicMirror docs here https://github.com/MichMich/MagicMirror


## Installation
The my-MagicMirror.xml file needs to be copied to

```
/boot/config/plugins/dockerMan/templates-user
```

on the unRAID server. It should then appear in the available Docker modules and allow you to configure it to point to the location of your config and modules.
