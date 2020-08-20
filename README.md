
# Introduction

Dockerfile to build a Subsonic media server

# Installation

Pull the latest version of the image from the docker.

```
docker pull zveronline/subsonic
```

Alternately you can build the image yourself.

```
docker build -t zveronline/subsonic https://github.com/zveronline/docker-subsonic.git
```

# Quick Start

Run the image

```
docker run --name subsonic -d \
   --volume /mnt/storage/Music:/var/music \
   --publish 4040:4040 \
   zveronline/subsonic
```

This will start the subsonic media server and you should now be able to browse the content on port 4040.

# Environments

SUBSONIC_UID=1000
SUBSONIC_GID=1000

To change id and gid of username.

```
docker run --name subsonic -d \
   --volume /mnt/storage/Music:/var/music \
   --publish 4040:4040 \
   --env SUBSONIC_UID=1000 --env SUBSONIC_GID=1000 \
   zveronline/subsonic
```
