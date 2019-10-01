```

███████╗██████╗█████╗ ███╗   ███╗██╗███╗   ██╗██╗  ██╗██████╗
╚═██╔══╝██╔═══╝██══██╗████╗ ████║██║████╗  ██║██║  ██║██╔═══╝
  ██║   ████╗  █████╔╝██╔████╔██║██║██╔██╗ ██║██║  ██║██████╗
  ██║   ██╔═╝  ██══██╗██║╚██╔╝██║██║██║╚██╗██║██║  ██║╚═══██║
  ██║   ██████╗██  ██║██║ ╚═╝ ██║██║██║ ╚████║╚█████╔╝██████║
  ╚═╝   ╚═════╝╚═  ╚═╝╚═╝     ╚═╝╚═╝╚═╝  ╚═══╝ ╚═════╝ ╚════╝
                                                                                  
```

# TerminusDB Server Container Control

This is a simple convenience script to run terminus-server as a docker container. These instructions are for linux or similar

What the heck is TerminusDB? See here: https://terminusdb.com

## Prerequisites

- docker

Obvs, you need to have docker running.

- sudo

Since letting unprivileged users run docker is like insecure and all, this script uses sudo, so get your sudoers on.

## Get this this script and cd to it

```
$ git clone https://github.com/dmytri/terminus-container
$ cd terminus-container
```

## Pull the image

```
$ ./terminus-container pull

latest: Pulling from terminusdb/terminus-server
8f91359f1fff: Pull complete 
939634dec138: Pull complete 
f30474226dd6: Pull complete 
32a63113e3ae: Pull complete 
ae35de9092ce: Pull complete 
023c02983955: Pull complete 
d9fa4a1acf93: Pull complete 
Digest: sha256:f416b12f21d66a4adc6e74552d57e0a8d559a8fdeef07b8ac9a045e4ab58a4d6
Status: Downloaded newer image for terminusdb/terminus-server:latest
docker.io/terminusdb/terminus-server:latest
```

## Create a container
```
$ ./terminus-container create

9f9363c83108c0a412a0b81f309ecaec3b85e29eac230b56198995acb9014e19
terminus-server container created
```

## Start the container
```
$ ./terminus-container start

terminus-server container started
```
Ready to terminate? Go here: http://localhost:6363/dashboard

## To remove and stop, see usage
```
$ ./terminus-container 

USAGE:
  terminus-container [COMMAND]

  pull    pull from dockerhub
  create  create container
  rm      remove container
  start   start container
  stop    stop container
```
Oh, and flattery motivates us, please give us a star here: https://github.com/terminusdb/terminus-server



