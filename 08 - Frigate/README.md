# Work in progress

<a id="readme_top"></a>
## Frigate
Frigate is a free, open-source NVR (Network Video Recorder) system designed specifically for real-time AI-powered object detection. It’s commonly used in home automation setups, especially when privacy, performance, and local processing are a priority.  
https://frigate.video/

<details>
<summary><u>Table of Contents</u></summary>

+ <a href="#Frigate">Frigate</a>
	
</details> 

<a href="https://github.com/HomeStudiosDIY/HomeStudiosDIY/blob/main/README.md">Back to Home Page</a>



Installation



Config





bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/docker.sh)"


Privileged


 To update Frigate, create a new container and transfer your configuration.


	mkdir /data/
	mkdir /data/config/
	mkdir /data/cctv/




pct set 104 -mp0 /mnt/pve/disk4tb/frigate,mp=/data/cctv/


from Proxmox Shell

nano /etc/pve/lxc/104.conf

	lxc.mount.entry: /dev/bus/usb/002/ dev/bus/usb/002/ none bind,optional,create=dir 0,0







<p align="right"><a href="#readme_top">back to top</a></p>