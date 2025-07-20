# Work in progress

<a id="readme_top"></a>
## IMMICH:

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



Immich is a free, open-source, self-hosted photo and video management platform designed as a privacy-focused alternative to cloud services like Google Photos and iCloud. It allows you to back up, organize, and browse your media entirely on your own server, giving you full control over your data.



Self-hosted photo and
video management solution

Easily back up, organize, and manage your photos on your own server. Immich helps you
browse, search and organize your photos and videos with ease, without sacrificing your privacy.

https://immich.app/





Immich is a free, open-source, self-hosted photo and video management platform designed as a privacy-focused alternative to cloud services like Google Photos and iCloud. It allows you to back up, organize, and browse your media entirely on your own server, giving you full control over your data.




bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"

immich

	mkdir /data
	mkdir /data/immich
	mkdir /data/photos

pct set 106 -mp0 /mnt/data/photos,mp=/data/photos/




<p align="right"><a href="#readme_top">back to top</a></p>



