# Work in progress

<a id="readme_top"></a>
# Plex Setup

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










bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"
PLEX:

mkdir /data
mkdir /data/stream
mkdir /data/usb




pct set 108 -mp0 /mnt/data/stream/,mp=/data/stream
pct set 108 -mp1 /mnt/pve/disk4tb/movies/,mp=/data/usb/Movies

pct set 108 -mp1 /mnt/data/usb/,mp=/data/usb


pct set 108 -mp1 /mnt/pve/disk4tb/movies/,mp=/data/usb/movies



Web:   plex.tv/claim

curl -X POST 'http://IP-Address:32400/myplex/claim?token=claim-XXXXXXXXXXXX'

systemctl restart plexmediaserver.service 


curl -X POST -s -H "X-Plex-Client-Identifier: {XXXXXXXXX}" "https://plex.tv/api/claim/exchange?token={claim-xxxxxxxxxx}"




<p align="right"><a href="#readme_top">back to top</a></p>