# Work in progress

<a id="readme_top"></a>
## Downloaders

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




## Radar:
<a id="about-the-project"></a>



Radarr is an open-source tool designed to automate the downloading, organizing, and tracking of movies.



https://radarr.video/#home




	mkdir /data
	mkdir /data/stream
	mkdir /data/usb
	mkdir /data/downloads
	mkdir /data/radarr
	mkdir /data/sonarr




nano /etc/pve/lxc/110.conf

	pct set 109 -mp0 /mnt/data/stream/,mp=/data/stream
	pct set 109 -mp1 /mnt/data/usb/,mp=/data/usb
	pct set 109 -mp1 /mnt/dve/disk4tb/movies,mp=/data/usb
	pct set 109 -mp2 /mnt/pve/disk4tb/downloads,mp=/data/downloads


pct set 108 -mp0 /mnt/data/stream/,mp=/data/stream



      - /data/radarr/:/config
      - /data:/movies #optional
      - /data/downloads:/downloads #optional



<p align="right"><a href="#readme_top">back to top</a></p>

##  Sonarr:
<a id="about-the-project"></a>

Sonarr is an open-source application used to manage and automate the downloading, organizing, and tracking of TV series. It's popular among media enthusiasts who run home media servers

https://sonarr.tv/


	mkdir /data
	mkdir /data/stream
	mkdir /data/usb
	mkdir /data/downloads
	mkdir /data/sonarr




nano /etc/pve/lxc/110.conf

	pct set 109 -mp0 /mnt/data/stream/,mp=/data/stream
	pct set 109 -mp1 /mnt/data/usb/,mp=/data/usb
	pct set 109 -mp1 /mnt/dve/disk4tb/movies,mp=/data/usb
	pct set 109 -mp2 /mnt/pve/disk4tb/downloads,mp=/data/downloads


pct set 108 -mp0 /mnt/data/stream/,mp=/data/stream


<p align="right"><a href="#readme_top">back to top</a></p>


## Downloader
<a id="about-the-project"></a>






	mkdir /data
	mkdir /data/stream
	mkdir /data/usb
	mkdir /data/downloads
	mkdir /data/
	mkdir /data/radarr
	mkdir /data/sonarr



run

	nano /etc/pve/lxc/110.conf

data

	pct set 109 -mp0 /mnt/data/stream/,mp=/data/stream
	pct set 109 -mp1 /mnt/data/usb/,mp=/data/usb
	pct set 109 -mp1 /mnt/dve/disk4tb/movies,mp=/data/usb
	pct set 109 -mp2 /mnt/pve/disk4tb/downloads,mp=/data/downloads


pct set 108 -mp0 /mnt/data/stream/,mp=/data/stream


apt install resolvconf

<p align="right">(<a href="#readme_top">back to top</a>)</p>





Overview



Setup Requirements



Setup Guides


<p align="right"><a href="#readme_top">back to top</a></p>