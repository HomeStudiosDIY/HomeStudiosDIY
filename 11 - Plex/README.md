# Work in progress

<a id="readme_top"></a>
# Plex Setup and Config
<a id="about-the-project"></a>

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