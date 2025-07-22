# Work in Progress!!

<a id="readme_top"></a>
## Downloaders
If you follow my setup I have 

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#flaresolverr">flaresolverr</a>
+ <a href="#Prowlarr">Prowlarr</a>
+ <a href="#Radarr">Radarr</a>
+ <a href="#Sonarr">Sonarr</a>
+ <a href="#qbittorrent">qbittorrent</a>
+ <a href="#huntarr">huntarr</a>
	
</details> 

<a href="https://github.com/HomeStudiosDIY/HomeStudiosDIY/blob/main/README.md">Back to Home Page</a>




<a id=""></a>
## flaresolverr





<p align="right"><a href="#readme_top">back to top</a></p>

<a id=""></a>
## Prowlarr








<p align="right"><a href="#readme_top">back to top</a></p>

<a id=""></a>
## Radar:

Radarr is an open-source tool designed to automate the downloading, organizing, and tracking of movies.


https://radarr.video/#home



Installation

route folders has to be done first

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

<a id="about-the-project"></a>
##  Sonarr:

Sonarr is an open-source application used to manage and automate the downloading, organizing, and tracking of TV series. It's popular among media enthusiasts who run home media servers

https://sonarr.tv/


Installation

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


Config





<p align="right"><a href="#readme_top">back to top</a></p>

<a id="about-the-project"></a>
## qbittorrent



Installation


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



<p align="right"><a href="#readme_top">back to top</a></p>