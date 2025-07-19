# Work in progress

<a id="readme_top"></a>

## Jellefin Setup and Config
<a id="about-the-project"></a>




Overview

Jellyfin is the volunteer-built media solution that puts you in control of your media. Stream to any device from your own server, with no strings attached. Your media, your server, your way.

https://jellyfin.org/

Setup Requirements

Setup Guide



bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"


JELLYFIN:



mkdir /data
mkdir /data/stream
mkdir /data/usb

pct set 106 -mp0 /mnt/data/stream/,mp=/data/stream
pct set 106 -mp1 /mnt/data/usb/,mp=/data/usb

RamDisk:
lxc.mount.entry: tmpfs dev/shm tmpfs size=4G,nosuid,nodev,noexec,create=dir 0 0
