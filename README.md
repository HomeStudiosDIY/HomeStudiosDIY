<a id="readme_top"></a>
# Welcome to my channel! 👋

If you're looking to build your own locally hosted Smart Home, you're in the right place. The key focus will be on Home Assistant as the heart of the smart home—making automation simple, powerful, and private.

My goal is to keep things as beginner-friendly as possible, so you don’t have to waste hours digging through countless videos. I’ll provide step-by-step written guides to help you get started, along with more advanced tips for when you're ready to dive deeper.

All the code and guides I share are from my actual working system not just demos so feel free to use and adapt them for your own home.



https://www.youtube.com/@homestudios_diy


If any of my content helped you please buy me a Coffee or a Beer!! This will help me expand and add more guides.

https://paypal.me/HomeStudiosDIY

https://github.com/sponsors/HomeStudiosDIY



I have listed all the software I use.

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#Proxmox">Proxmox</a>  

+ <a href="#Home_Assitant">Home Assitant</a>

+ <a href="#Frigate">Frigate</a>

+ <a href="#Tools">Tools</a>
	+ <a href="#Portainer">Portainer</a>
	+ <a href="#Portainer_Agent">Portainer Agent</a>
	+ <a href="#Watchtower">Watchtower</a>


+ <a href="#OPNsense">OPNsense</a>

+ <a href="#Unifi">Unifi</a>
	
+ <a href="#Vaultwarden">Vaultwarden</a>
	
+ <a href="#immich">immich</a>
		
+ <a href="#Jellyfin">Jellyfin</a>
		
+ <a href="#Plex">Plex</a>
		
+ <a href="#Media">Media</a>
	+ <a href="#Jellystat">Jellystat</a>
	+ <a href="#Tautulli">Tautulli</a>
	+ <a href="#jellyplex_watched">jellyplex-watched</a>
	
+ <a href="#Ollama">Ollama</a>

+ <a href="#tdarr">tdarr</a>

+ <a href="#n8n">n8n</a>

	
</details>  
  
  

<a id="Proxmox"></a>
## Proxmox

Proxmox delivers powerful, enterprise-grade solutions with full access to all functionality for everyone - highly reliable and secure.
The software-defined and open platforms are easy to deploy, manage and budget for.  
https://www.proxmox.com/en/


In this section I will guide you to install Proxmox and dependency depending on your system and hardware setup. 

Please click on the link to get all the guides.
https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/01%20-%20Proxmox




<p align="right"><a href="#readme_top">back to top</a></p>

<a id="Home_Assistant"></a>
## Home Assitant

# Coming Soon!!


installing Home Assistant on Proxmox also all the diffrent integrations and Add-ons I Have plust all my automations and config 




https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/03%20-%20HomeAssistant%20Prod

Optional
NodeRed
https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/05%20-%20HomeAssistant%20NodeRed

Optional
A Dev Installation to test new stuff
https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/04%20-%20HomeAssistant%20Dev



<p align="right"><a href="#readme_top">back to top</a></p>

<a id="Frigate"></a>
## Frigate

# Coming Soon!!


Frigate is a free, open-source NVR (Network Video Recorder) system designed specifically for real-time AI-powered object detection. It’s commonly used in home automation setups, especially when privacy, performance, and local processing are a priority.
https://frigate.video/




Install and config

https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/08%20-%20Frigate


<p align="right"><a href="#readme_top">back to top</a></p>




<a id="Tools"></a>
## Tools

# Coming Soon!!

If you follow my setup guides you will not need to install this. This will be install under ever application that requers it


<a id="Portainer"></a>
+ Portainer


https://community-scripts.github.io/ProxmoxVE/scripts?id=docker


bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"


<a id="Portainer_Agent"></a>
+ Portainer Agent

https://community-scripts.github.io/ProxmoxVE/scripts?id=docker


bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"

<a id="Watchtower"></a>
+ Watchtower

<p align="right"><a href="#readme_top">back to top</a></p>










<a id="OPNsense"></a>
## OPNsense

# Coming Soon!!


OPNsense® is an open source, feature rich firewall and routing platform, offering cutting-edge network protection.  
https://opnsense.org/

If you want to have you own FireWall and not use your ISP route. This will allow you more reflexibility and also more security. 
This will guide you yo install OPNsense on Proxmox and I will also show you how to configure all the different plug-ins I use.
https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/02%20-%20OPNsense


<p align="right"><a href="#readme_top">back to top</a></p>




<a id="UniFi"></a>
## UniFi

# Coming Soon!!

https://www.ui.com/





https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/06%20-%20UniFi



<p align="right"><a href="#readme_top">back to top</a></p>

<a id="Vaultwarden"></a>
## Vaultwarden

# Coming Soon!!

An alternative server implementation of the Bitwarden Client API, written in Rust and compatible with official Bitwarden clients [disclaimer], perfect for self-hosted deployment where running the official resource-heavy service might not be ideal.

https://github.com/dani-garcia/vaultwarden



Installing and config
https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/07%20-%20Vaultwarden



<p align="right"><a href="#readme_top">back to top</a></p>



<a id="immich"></a>
## immich

# Coming Soon!!


Immich is a free, open-source, self-hosted photo and video management platform designed as a privacy-focused alternative to cloud services like Google Photos and iCloud. It allows you to back up, organize, and browse your media entirely on your own server, giving you full control over your data.



https://immich.app/





Install and config


https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/09%20-%20immich



<p align="right"><a href="#readme_top">back to top</a></p>

<a id="Jellyfin"></a>
## Jellyfin

# Coming Soon!!


Jellyfin is the volunteer-built media solution that puts you in control of your media. Stream to any device from your own server, with no strings attached. Your media, your server, your way.

https://jellyfin.org/

Optional
Install and config
https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/10%20-%20Jellyfin

<p align="right"><a href="#readme_top">back to top</a></p>

## Plex

# Coming Soon!!
Plex is a media server and streaming platform that allows you to organize, stream, and access your personal media library—such as movies, TV shows, music, and photos—from virtually any device.



Install and config

https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/11%20-%20Plex


<p align="right"><a href="#readme_top">back to top</a></p>

<a id="Media"></a>
## Media

# Coming Soon!!



+ Jellystat

Jellystat is a self-hosted analytics dashboard for monitoring your Jellyfin media server. It provides detailed usage statistics, visualizations, and insights about your media consumption and server activity — similar to how you might use analytics in services like Plex Dashboard or Tautulli (for Plex), but made specifically for Jellyfin.

+ Tautulli

Tautulli is a powerful, self-hosted monitoring and analytics tool for Plex Media Server. It tracks what’s being watched, by whom, when, and how — giving you detailed insights into Plex usage with an attractive web-based dashboard.

+ jellyplex-watched








https://github.com/HomeStudiosDIY/HomeStudiosDIY/tree/main/12%20-%20media


<p align="right"><a href="#readme_top">back to top</a></p>




<a id="Ollama"></a>
## Ollama

# Coming Soon!!

Ollama is a tool that lets you run large language models (LLMs) like LLaMA, Mistral, Gemma, and others directly on your own computer — locally, with no internet or cloud dependency.

https://ollama.com/



<p align="right"><a href="#readme_top">back to top</a></p>


<a id="tdarr"></a>
## tdarr

# Coming Soon!!


Tdarr is a powerful, self-hosted, automated media transcoding and library management tool, often used alongside Plex or Jellyfin to optimize media files.


<p align="right"><a href="#readme_top">back to top</a></p>


## n8n

# Coming Soon!!




<!--
**HomeStudiosDIY/HomeStudiosDIY** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

