# LXD-Suite
LXD Management Scripts

### Installing
put the scripts somewhere in your $PATH (e.g. /usr/local/bin) and make them executable.

### lxc-ip
script for adding a network with public ip to a container and automatically configuring the network inside the container.

```
lxc-ip set [remote:]<container> <ip>
lxc-ip unset [remote:]<container>
```

### lxc-migrate
script for moving a container from or to a remote server and restoring network settings if set up using the lxc-ip script.

```
lxc-migrate [remote:]<container> [remote:]<container> [options]
```
lxc-migrate depends on lxc-ip.

### lxc-quota
quota script for lxd containers with lvm storage

```
lxc-quota <size> <container>
```
