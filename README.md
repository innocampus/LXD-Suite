# LXD-Suite
LXD Management Scripts

### Installing
put the scripts somewhere in your $PATH (e.g. /usr/local/bin) and make them executable.

### lxc-ip
script for adding a network with public ip (using an ipvlan interface) to a container and automatically configuring the network inside the container.

```
lxc-ip [options] set <container> <ip>
lxc-ip [options] unset <container>

OPTIONS
-h, -?, --help
	print a help message and exit.

-l, --host-only
	only configure the host, assume an interface by the name lxd-guest21 is already assigned to the container.
```

### lxc-quota
quota script for lxd containers using lvm storage backend and xfs / ext4 filesystems. 

```
lxc-quota [options] <size> <container>

OPTIONS
-h, -?, --help
	print a help message and exit.

-t, --type
	default "xfs", also supports "ext4". Filesystem used by the container

-o, --online
	two modes are supported. default uses lxd's quota implementation, which requires the container to restart. 
	online mode does not require the container to restart but might be more risky.
```
