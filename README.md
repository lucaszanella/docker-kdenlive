# docker-kdenlive

A container for [kdenlive](https://kdenlive.org/), a free and open-source video editor for GNU/Linux.

Based on https://github.com/lvm/docker-kdenlive

# how to 

## install

```
git clone https://github.com/lucaszanella/docker-kdenlive && \
cd docker-kdenlive && \
docker build -t kdenlive .
```

## run

```
docker run --rm -it -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/Videos:/videos -e DISPLAY=unix$DISPLAY --name knl kdenlive
```
  

`-v $HOME/videos:/videos` is used to mount the container's `/videos` directory to the host `$HOME/kdenlive` directory, you can choose other directory.    
Note: probably you *might* also need to execute `xhost local:root` or `xhost +my-computer-hostname.local`.
