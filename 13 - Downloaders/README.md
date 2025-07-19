# Work in progress

<a id="readme_top"></a>


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


<p align="right">(<a href="#readme_top">back to top</a>)</p>

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

<p align="right">(<a href="#readme_top">back to top</a>)</p>

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

