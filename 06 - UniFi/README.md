# Work in progress

<a id="readme_top"></a>
# UniFi

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


  
https://www.ui.com/



https://community-scripts.github.io/ProxmoxVE/scripts?id=docker


bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"



	
mkdir /data
mkdir /data/unifi	





nano /data/unifi/init-mongo.sh


```
#!/bin/bash

if which mongosh > /dev/null 2>&1; then
  mongo_init_bin='mongosh'
else
  mongo_init_bin='mongo'
fi
"${mongo_init_bin}" <<EOF
use ${MONGO_AUTHSOURCE}
db.auth("${MONGO_INITDB_ROOT_USERNAME}", "${MONGO_INITDB_ROOT_PASSWORD}")
db.createUser({
  user: "${MONGO_USER}",
  pwd: "${MONGO_PASS}",
  roles: [
    { db: "${MONGO_DBNAME}", role: "dbOwner" },
    { db: "${MONGO_DBNAME}_stat", role: "dbOwner" }
  ]
})
EOF	
```	
	
## UniFi
<a id="about-the-project"></a>

bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"
	

<a href="https://github.com/HomeStudiosDIY/ProxMox-Config/blob/main/Docker%20Compose%20Files/Unifi/init-mongo.sh/" target="_blank">file</a>




<a href="https://github.com/HomeStudiosDIY/ProxMox-Config/blob/main/Docker%20Compose%20Files/Unifi/Unifi.yaml/" target="_blank" rel="noopener noreferrer">file Docker</a>



<p align="right"><a href="#readme_top">back to top</a></p>	