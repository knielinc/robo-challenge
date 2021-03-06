# FAQ

## Windows (General)

### docker doesn't work on Windows

We recommend using [Docker Toolbox](https://www.docker.com/products/docker-toolbox)

## Windows (Docker Toolbox)

## I cannot connect to localhost:8080
There are two ways to solve this:
* You can either set port forwarding on the NAT network adapter in the Virtual Box Settings for the docker machine (typically called "default"). See https://www.howtogeek.com/122641/how-to-forward-ports-to-a-virtual-machine-and-use-it-as-a-server/ You need to forward the following ports
** 1883 (mqtt)
** 8080 (web)
** 9001 (websocket)
- Use the IP address of the docker machine instead of "localhost". You can find out the IP address of your docker machine using Kitematic (part of the Docker Toolbox).

## Docker cannot find files when running `docker-compose ... up`
There are two possible causes for this:
* This happens, when the shared folders cannot be properly mounted in VirtualBox. The easiest fix is to reinstall the newest version of VirtualBox and Docker Toolbox.
* You are using a different drive than C: While this is possible (see http://stackoverflow.com/questions/33245036/docker-toolbox-is-there-a-way-to-mount-other-folders-than-from-c-users-windows ) the easiest solutions probably to move things into a folder on the C: drive into a subfolder of the `Users` folder.
