# Work in Progress!!

<a id="readme_top"></a>
# Plex Setup

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#Plex">Plex</a>

</details> 

<a href="https://github.com/HomeStudiosDIY/HomeStudiosDIY/blob/main/README.md">Back to Home Page</a>







bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"



4 CPU
8GB Mem

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