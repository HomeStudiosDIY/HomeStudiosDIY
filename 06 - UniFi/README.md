# Coming Soon!!

<a id="readme_top"></a>
# UniFi
https://www.ui.com/

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#Installation">Installation</a>
	
</details> 

<a href="https://github.com/HomeStudiosDIY/HomeStudiosDIY/blob/main/README.md">Back to Home Page</a>


  

Installation


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
<a id="about-the-project"></a>
## UniFi


bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"
	

<a href="https://github.com/HomeStudiosDIY/ProxMox-Config/blob/main/Docker%20Compose%20Files/Unifi/init-mongo.sh/" target="_blank">file</a>




<a href="https://github.com/HomeStudiosDIY/ProxMox-Config/blob/main/Docker%20Compose%20Files/Unifi/Unifi.yaml/" target="_blank" rel="noopener noreferrer">file Docker</a>



<p align="right"><a href="#readme_top">back to top</a></p>	