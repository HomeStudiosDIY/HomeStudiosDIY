# Work in progress

<a id="readme_top"></a>
## Frigate

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


Monitor your security cameras with locally processed AI

Frigate is an open source NVR built around real-time AI object detection. All processing is performed locally on your own hardware, and your camera feeds never leave your home.


https://frigate.video/






Frigate is a free, open-source NVR (Network Video Recorder) system designed specifically for real-time AI-powered object detection. It’s commonly used in home automation setups, especially when privacy, performance, and local processing are a priority.


bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"


Privileged


 To update Frigate, create a new container and transfer your configuration.


	mkdir /data/
	mkdir /data/config/
	mkdir /data/cctv/


pct set 104 -mp0 /mnt/pve/disk4tb/frigate,mp=/data/cctv/




nano /etc/pve/lxc/104.conf

	lxc.mount.entry: /dev/bus/usb/002/ dev/bus/usb/002/ none bind,optional,create=dir 0,0







<p align="right"><a href="#readme_top">back to top</a></p>