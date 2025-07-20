# Work in progress

<a id="readme_top"></a>
## Jellefin

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#Proxmox">Proxmox</a>

+ <a href="#NVIDIA_Drivers">NVIDIA Drivers</a>


+ <a href="#Home_Assitant">Home Assitant</a>


+ <a href="#Unifi">Unifi</a>

	
+ <a href="#Vaultwarden">Vaultwarden</a>

	
+ <a href="#Frigate">Frigate</a>

	
+ <a href="#immich">immich</a>

		
+ <a href="#Jellyfin">Jellyfin</a>

		
+ <a href="#Plex">Plex</a>

		
+ <a href="#Media">Media</a>

	+ <a href="#Ombi">Ombi</a>
	+ <a href="#Jellystat">Jellystat</a>
	+ <a href="#Tautulli">Tautulli</a>
	+ <a href="#jellyplex_watched">jellyplex-watched</a>
	
+ <a href="#Downloaders">Downloaders</a>

	+ <a href="#flaresolverr">flaresolverr</a>
	+ <a href="#prowlarr">prowlarr</a>
	+ <a href="#Radarr">Radarr</a>
	+ <a href="#Sonarr">Sonarr</a>
	+ <a href="#qbittorrent">qbittorrent</a>
	+ <a href="#huntarr">huntarr</a>
	
+ <a href="#ollama">ollama</a>

+ <a href="#tdarr">tdarr</a>

	
</details> 



<a href="https://github.com/HomeStudiosDIY">Back to the Home Page</a>	










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





<p align="right"><a href="#readme_top">back to top</a></p>